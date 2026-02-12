In redis you can use SET to store unique values in a collection.
 Here are some common commands for working with sets in Redis: SET `keyname` value1 value2 value3 .
.
.

Use getrange to retrieve a range of elements from a list stored at a specific key.
 The syntax is: LRANGE `keyname` start end
you can use KEYS \* to list all keys in the Redis database, but be cautious as it can be slow for large datasets.

Use mset to set multiple key-value pairs in a single command.
 The syntax is: MSET key1 value1 key2 value2 .
.
.

Use mget to retrieve multiple values for specified keys in a single command.
 The syntax is: MGET key1 key2 key3 .
.
.

To get the length of a string stored at a specific key, use strlen `keyname`.

use incr to increment the integer value of a key by one.
 The syntax is: INCR `keyname`
Use incrby to increment the integer value of a key by a specified amount.
 The syntax is: INCRBY `keyname` increment
Use decr to decrement the integer value of a key by one.
 The syntax is: DECR `keyname`
Use decrby to decrement the integer value of a key by a specified amount.
 The syntax is: DECRBY `keyname` decrement
Use del to delete a key from the Redis database.
 The syntax is: DEL `keyname`
Redis can autodelete keys after a specified time using the expire command.
 The syntax is: EXPIRE `keyname` seconds
Use ttl to check the remaining time to live of a key with an expiration.
 The syntax is: TTL `keyname`
You can do the short form of setting a key with expiration using setex.
 The syntax is: SETEX `keyname` seconds value

You can use lpush to add one or more elements to the beginning of a list.
 The syntax is: LPUSH `keyname` value1 value2 .
.
.

Use rpush to add one or more elements to the end of a list.
 The syntax is: RPUSH `keyname` value1 value2 .
.
.

Use lpop to remove and return the first element of a list.
 The syntax is: LPOP `keyname`
Use rpop to remove and return the last element of a list.
 The syntax is: RPOP `keyname`
Use llen to get the length of a list stored at a specific key.
 The syntax is: LLEN `keyname`
Use lrange to retrieve a range of elements from a list stored at a specific key.
 The syntax is: LRANGE `keyname` start end
Use lset to set the value of an element at a specific index in a list.
 The syntax is: LSET `keyname` index value
Use lrem to remove elements from a list that match a specified value.
 The syntax is: LREM `keyname` count value
Use linsert to insert an element before or after a pivot element in a list.
 The syntax is: LINSERT `keyname` BEFORE|AFTER pivot value
Use lindex to get the element at a specific index in a list.
 The syntax is: LINDEX `keyname` index
Use lpushx to add an element to the beginning of a list only if the list already exists.
 The syntax is: LPUSHX `keyname` value
Use rpushx to add an element to the end of a list only if the list already exists.
 The syntax is: RPUSHX `keyname` value
use sort to sort the elements in a list, set, or sorted set.
 The syntax is: SORT `keyname` [BY pattern] [LIMIT offset count] [GET pattern] [ASC|DESC] [ALPHA] [STORE destination]
use sort desc to sort the elements in descending order.
 The syntax is: SORT `keyname` DESC

We have 5 types of data structures in Redis: Strings, Lists, Sets, Hashes, and Sorted Sets.
 Each data structure has its own set of commands for manipulation and retrieval.
 Understanding these data structures and their associated commands is crucial for effectively using Redis as a database or caching solution.


Redis Set has the following structure: post:1:likes = {user1, user2, user3}
This represents a set of users who have liked post 1.
 You can add or remove users from this set using commands like SADD and SREM, and you can check membership with SISMEMBER.


Use sadd to add one or more members to a set.
 The syntax is: SADD `keyname` member1 member2 .
.
.

Use srem to remove one or more members from a set.
 The syntax is: SREM `keyname` member1 member2 .
.
.

Use smembers to retrieve all members of a set.
 The syntax is: SMEMBERS `keyname`
Use sismember to check if a member exists in a set.
 The syntax is: SISMEMBER `keyname` member
Use scard to get the number of members in a set.
 The syntax is: SCARD `keyname`
Use sunion to get the union of multiple sets.
 The syntax is: SUNION `keyname1` `keyname2` .
.
.

Use sinter to get the intersection of multiple sets ( mutual elements ).
 The syntax is: SINTER `keyname1` `keyname2` .
.
.

Use sdiff to get the difference between multiple sets.
 The syntax is: SDIFF `keyname1` `keyname2` .
.
.

You can not duplicate values in a Redis Set.
 Each value is unique within the set.

Use sdiffstore to store the difference between multiple sets into a new set.
 The syntax is: SDIFFSTORE `destination` `keyname1` `keyname2` .
.
.

Use sunionstore to store the union of multiple sets into a new set.
 The syntax is: SUNIONSTORE `destination` `keyname1` `keyname2` .
.
.

