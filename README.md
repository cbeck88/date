This is actually three separate C++11/C++14 libraries:

1.  `"date.h"` is a header-only library which builds upon `<chrono>`.  It adds some new `duration` types, and new `time_point` types.  It also adds "field" types such as `year_month_day` which is a struct `{year, month, day}`.  And it provides convenient means to convert between the "field" types and the `time_point` types.  See http://howardhinnant.github.io/date_v2.html for more details.

    Here is the Cppcon 2015 presentation on date.h: https://www.youtube.com/watch?v=tzyGjOm8AKo

    Here are the Cppcon 2015 slides on date.h: http://schd.ws/hosted_files/cppcon2015/43/hinnant_dates.pdf

2. `"tz.h"` / `"tz.cpp"`  are a timezone library built on top of the `"date.h"` library.  This timezone library is a complete parser of the IANA timezone database.  It provides for an easy way to access all of the data in this database, using the types from `"date.h"` and `<chrono>`.  The IANA database also includes data on leap seconds, and this library provides utilities to compute with that information as well.  See http://howardhinnant.github.io/tz.html for more details.

3. `"iso_week.h"` is a header-only library built on top of the `"date.h"` library which implements the ISO week date calendar.  See http://howardhinnant.github.io/iso_week.html for more details.
