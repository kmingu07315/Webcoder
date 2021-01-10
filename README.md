# Webcoder
```kotlin
package com.example.myapp.Kotlin
import java.util.Scanner

fun main(args: Array<String>) {
	var i: Int = 1
  var value: Int
  var mList = mutableListOf<Int>(0)
  val scan: Scanner = Scanner(System.`in`)
  print("size is ")
  val size = scan.nextInt()

  mList[0] = (1 + Math.random() * size).toInt()

  while (i < size) {
    value = (1 + Math.random() * size).toInt()

    if (duple(mList, value)) {
      mList.add(value)
      i++
    }	else {
      continue
    }
  }
  println(mList)
}

fun duple(mList: MutableList<Int>, value: Int): Boolean {
  for (item in mList) {
    if (item == value)
      return false
  }
  return true
}
```
