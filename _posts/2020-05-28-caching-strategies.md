---
layout: post
title: "Caching Strategies"
categories: architect
---

### Lazy loading
- loads data into the cache only when necessary
- when application requests data, it first makes the request to the cache, if `cache hit`, it is retrieved.
- if it's not or expired `cache miss`, the the data is retrieved from the data store and then stored in the cache

#### Pros
- Only requested data is cached

#### Cons
cache miss penalty

### Write through
- adds data or updates in the cache whenever data is written to the database

#### Pros
- the data in the cache is never stale

#### Cons
- the data or information that is stored in the cache is never used
- cost for space
- overhead due to the duplicate data
- cache churn
