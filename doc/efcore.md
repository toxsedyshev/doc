---
layout: doc
title: Entity Framework Core
redirect_from:
  - /doc/ef7.html
---

An experimental Npgsql Entity Framework Core provider is available for testing.
Note that like EFCore itself the provider is under heavy development, but most of the basic features work.
To use the provider, add the [Npgsql unstable feed](http://myget.org/gallery/npgsql-unstable) to your NuGet.Config.

The main provider package is
[Npgsql.EntityFrameworkCore.PostgreSQL](http://myget.org/feed/npgsql-unstable/package/nuget/Npgsql.EntityFrameworkCore.PostgreSQL).
Reverse-engineering (database-first) is also supported; the provider for that is
[Npgsql.EntityFrameworkCore.PostgreSQL.Design](http://myget.org/feed/npgsql-unstable/package/nuget/Npgsql.EntityFrameworkCore.PostgreSQL.Design).
The database-first instructions in the EFCore getting started work, just change the provider name and the connection string.

Development happens in [this github repo](https://github.com/npgsql/Npgsql.EntityFrameworkCore.PostgreSQL), issues should be opened there.

Please let us know of any bugs you run across!

Features not yet implemented:

* Optimistic concurrency ([#19](https://github.com/npgsql/Npgsql.EntityFrameworkCore.PostgreSQL/issues/19)).
* It's not possible to use PostgreSQL-specific types inside where clauses
  (https://github.com/aspnet/EntityFramework/issues/5365).
* Composite types aren't supported yet ([#22](https://github.com/npgsql/Npgsql.EntityFrameworkCore.PostgreSQL/issues/22)).