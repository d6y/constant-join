#  Example of a constant query in Slick

```
val ids: Query[Rep[Long], Long, Seq] = 
  Query(1L) ++ Query(3L) ++ Query(15L)

// Use it as in...
val q = ids.joinLeft(messages).on(_ === _.id)
```

Prompted by: https://gitter.im/slick/slick?at=5f916eadea6bfb0a9a4f0a32