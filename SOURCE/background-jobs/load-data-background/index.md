> 编写:[kesenhoo](https://github.com/kesenhoo)，校对:

> 原文:<http://developer.android.com/training/load-data-background/index.html>

# 使用CursorLoader在后台加载数据

从[ContentProvider](http://developer.android.com/reference/android/content/ContentProvider.html)查询你需要显示的数据是比较耗时的。如果你在Activity中直接执行查询的操作，那么有可能导致Activity出现ANR的错误。即使没有发生ANR，用户也会看到一个令人烦恼的UI延迟。为了避免那些问题，你应该在另外一个线程中执行查询的操作，等待查询操作完成，然后再显示查询结果。

你可以通过使用[CursorLoader](http://developer.android.com/reference/android/support/v4/content/CursorLoader.html)来实现，它会在后台异步查询数据并在查询结束时和Activity重新进行连接。CursorLoader不仅仅能够实现在后台查询数据，还能够在查询数据发生变化时自动执行重新查询的操作。

这节课会介绍如何使用CursorLoader来执行一个后台查询数据的操作。在这节课中的演示代码使用的是[v4 Support Library](http://developer.android.com/tools/support-library/features.html#v4)中的类。

## 下载演示代码

** [ThreadSample](file:///Users/hook/Desktop/docs/shareables/training/ThreadSample.zip) **

## Lessons

* [使用CursorLoader执行查询任务：Running a Query with a CursorLoader](setup-loader.html)

  学习如何使用CursorLoader在后台执行查询操作。

* [处理查询的结果：Handling the Results](handle-result.html)

  学习如何处理从CursorLoader查询到的数据，以及在loader框架重置CursorLoader时如何解除当前Cursor的引用。
