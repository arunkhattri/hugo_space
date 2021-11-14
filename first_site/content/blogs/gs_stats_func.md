+++
title = "Summary functions in google sheet"
author = ["Arun Kr. Khattri"]
date = 2021-11-10
lastmod = 2021-11-13T20:06:27+05:30
tags = ["spreadsheet", "googlesheet", "summary", "functions", "sum", "count", "average", "mode", "max", "min"]
categories = ["googlesheet"]
draft = true
weight = 2001
foo = "bar"
baz = "zoo"
alpha = 1
beta = "two words"
gamma = 10
[menu.main]
  identifier = "summary-functions-in-google-sheet"
  weight = 2001
+++

## Summary Functions in Google Sheet {#summary-functions-in-google-sheet}

Quoting [OpenOffice.org 3.x Calc Guide](https://wiki.openoffice.org/w/images/b/b3/0300CS3-CalcGuide.pdf) "Formulas are equations using numbers and variables to get a result. In a spreadsheet, the variables are cell locations that hold the data needed for the equation to be completed. A function is a predefined calculation entered in a cell to help you analyze or manipulate data in a spreadsheet. All you have to do is add the arguments, and the calculation is automatically made for you."

Google sheet includes 494 functions in 16 types (categories). Common types are date, financial, logical, lookup, text, statistical and some google specific types like google which contains `GOOGLETRANSLATE` function to translate text from one language into another.

There are around 135 statistical built-in-functions available in google sheets, and if you think none is for you, you can create one (not the scope of this blog, may be some other time...). In this blog we are going to cover group of functions used in summarizing the data and one must be familiar while using spreadsheets. The group includes `SUM, COUNT, AVERAGE, MAX, MIN,  & MODE` applied on numerical data.

Before going for formulas, few words on entering formulas...

-   all formulas need to be started with one of the following symbols: =, + or -. Anything else will be treated like a text.
-   Each cell has the unique address and referred by its position in the grid (columns & rows). `A2` refers to column A, second row in the grid.
-   You can enter formula in two ways, either directly into the cell itself, or at the input line.
-   Depending upon the kind of person you are (in using the computer), while selecting range either you can use mouse or if you are like me which prefers keyboard, range can be written as `start:end` for e.g to select cell `A1` to cell `A10`, we can write `A1:A10` directly into formula.
-   When you start typing function, google sheet try to help you out by suggesting the appropriate name of the function, press &uarr; and &darr; to navigate and press **TAB** to accept. Also it will show you the arguments it takes to provide you the output.


### SUM {#sum}

The title for 'most used function' in spreadsheet category undoubtedly goes to `SUM` function.


#### Syntax {#syntax}

```nil
SUM(value1, [value2, ...])

value1 - The first number or range to add together.

value2, ... - [ OPTIONAL ] - Additional numbers or ranges to add to value1.
```

{{< figure src="/ox-hugo/sum.gif" alt="sum function" caption="Figure 1: SUM function" >}}


### COUNT {#count}


#### Syntax {#syntax}

```nil
COUNT(value1, [value2, ...])

value1 - The first value or range to consider when counting.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when counting.
```

`COUNT` function returns the number of numeric values in a dataset. It ignores the text values.

{{< figure src="/ox-hugo/count.gif" alt="count function" caption="Figure 2: COUNT function" >}}


### COUNTA {#counta}

To count all values including text, zero-length strings and whitespace, use `COUNTA` function.


#### Syntax {#syntax}

```nil
COUNTA(value1, [value2, ...])

value1 - The first value or range to consider when counting.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when counting.
```

{{< figure src="/ox-hugo/counta.gif" alt="counta function" caption="Figure 3: COUNTA function" >}}


### Other functions related to Count {#other-functions-related-to-count}


#### COUNTUNIQUE {#countunique}

Above mentioned count functions doesn't care about duplicate values, if you want to count unique values only, use `COUNTUNIQUE`...

<!--list-separator-->

-  Syntax

    ```nil
    COUNTUNIQUE(value1, [value2, ...])

    value1 - The first value or range to consider for uniqueness.

    value2, ... - [ OPTIONAL ] - Additional values or ranges to consider for uniqueness.
    ```


#### COUNTBLANK {#countblank}

returns the number of empty cells in a given range.

<!--list-separator-->

-  Syntax

    ```nil
    COUNTBLANK(value1, [value2,...])

    value1 - The first value or range in which to count the number of blanks.
    value2 - [OPTIONAL ] - Additional values or ranges in which to count the number of blanks.
    ```

    {{< figure src="/ox-hugo/other_count.gif" alt="other count function" caption="Figure 4: Other count functions" >}}


### AVERAGE {#average}

The average function returns the numerical average (arithmetic mean) value in a dataset, ignoring text.


#### Syntax {#syntax}

```nil
AVERAGE(value1, [value2, ...])

value1 - The first value or range to consider when calculating the average value.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when calculating the average value
```

To have text values considered as 0 values, use `AVERAGEA`

{{< figure src="/ox-hugo/average.gif" alt="average function" caption="Figure 5: AVERAGE function" >}}


### MEDIAN {#median}

The median function finds the median or middle value in a list/range of numbers.


#### Syntax {#syntax}

```nil
MEDIAN(value1, [value2, ...])

value1 - The first value or range to consider when calculating the median value.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when calculating the median value.
```

-   Any text encountered in the value arguments will be ignored.
-   `MEDIAN` returns the middle value if odd number of value arguments are given. With an even number of values, it gives average of two middle values.
-   It ignores empty cells but not ones containing the numeral 0.

{{< figure src="/ox-hugo/median.gif" alt="median function" caption="Figure 6: MEDIAN function" >}}


### MODE {#mode}

Returns the most commonly occurring value in a dataset.


#### Syntax {#syntax}

```nil
MODE(value1, [value2, ...])

value1 - The first value or range to consider when calculating mode.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when calculating mode.
```

{{< figure src="/ox-hugo/mode.gif" alt="mode function" caption="Figure 7: MODE function" >}}


### MAX {#max}

Returns the maximum value in a numeric dataset.


#### Syntax {#syntax}

```nil
Syntax
MAX(value1, [value2, ...])

value1 - The first value or range to consider when calculating the maximum value.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when calculating the maximum value.
```

{{< figure src="/ox-hugo/max.gif" alt="max function" caption="Figure 8: MAX Function" >}}


### MIN {#min}

Returns the minimum value in a numeric dataset.


#### Syntax {#syntax}

```nil
MIN(value1, [value2, ...])

value1 - The first value or range to consider when calculating the minimum value.

value2, ... - [ OPTIONAL ] - Additional values or ranges to consider when calculating the minimum value.
```

{{< figure src="/ox-hugo/min.gif" alt="max function" caption="Figure 9: MAX Function" >}}
