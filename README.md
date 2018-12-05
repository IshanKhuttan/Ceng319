# View Pager

## Introduction
The viewpager is the widget that helps us or allows the user to swipe right or left to see an entirely new screen. In other way, we can say that it is a great way to show the user multiple tabs. It has also the capability to strongly remove or add pages (tabs) anytime. We can think of an idea of grouping search results by certain classes, and showing each class in a separate list. With the use of viewpager, the user could swipe right or left to see the other categories lists or classes. For using the viewpager, it need some knowledge of both the Fragments and PageAdapters. In this case, the Fragments are the "pages". On each screen that the ViewPager let the user to scroll is a Fragment. With the use of Fragments instead of a view, there is much broad range of chances to show in each page. Then there is no limit to just list of items. There can be  any collections of views and widgets that we may need. We can believe of PageAdapters in the similar way of ListAdapters. The task of PageAdapters is to provide Fragments(instead of views) to the UI for drawing. So for working everything properly we need:
1. An Activity with a ViewPager on display as part of its main UI. 
2. A set of Fragments to be used as pages
3. A custom  FragmentPagerAdapter that returns the correct Fragment for each page number


## Example
In the case of ViewPager we cannot avoid the using of the support library because ViewPager is not firstly supported even in the latest Android , Lollipop. Also as the support library does not work properly with Fragments, in order to solve that we have to use the support library Fragment services. And for making the support library to work we have to navigate the project structure to Gradle Scripts and open the file build.gradle(app). And at the end of the file we have to include a line to dependencies(compile "com.android.support:support-v4:21.0.+"). Furthermore we can change the 21.0 to any version we want to use. And the "+" at the last will make sure that we will use the most up to date subversion. The end of file will look something like this:
dependencies {
  complie fileTree(dir: 'libs', include: ['* .jar']}
  compile "com.android.support:support-v4:21.0.+"
  }
After synchronize the project in android studio, it will be ready to use classes that are in the support library and will automatically add the import statements.
