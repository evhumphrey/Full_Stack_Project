# Schema Information

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
username        | string    | not null, indexed, unique
email           | string    | not null, indexed, unique
password_digest | string    | not null
session_token   | string    | not null, indexed, unique

## books
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
title       | string    | not null
blurb        | text      | not null
author_id   | integer   | not null, foreign key (references users), indexed


## reviews
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
author_id   | integer   | not null, foreign key (references users), indexed
book_id   | integer   | not null, foreign key (references users), indexed
title       | string    | not null
rating       | integer    | not null
description | string    |

## tags
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
name        | string    | not null
book_id        | string    | not null

## authors
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
name    | string   | not null, foreign key (references notes), indexed, unique [tag_id]
