1. [Count Distinct By Joining Two Table](#count-distinct-two)  
<a id='count-distinct-two'></a>
employerscount = 
COUNTROWS (
    INTERSECT (
        VALUES ( dim_employers[Id] ),
        VALUES ( fact_enrollments[accountid] )
    )
) <br>
2. [Create new table with column names](https://radacad.com/using-datatable-dax-function-for-creating-structured-table-in-power-bi)  
Year = 
DATATABLE (
    "Year", INTEGER,
    "Group", STRING,
    "Index", INTEGER,
    {
        { 2022, "This year", 1 },
        { 2021, "Last year", 2 },
        { 2020, "Two years ago", 3 },
        { 2019, "Three years ago", 4 },
        { 2018, "Four years ago",  5},
        { 2017, "Five years ago", 6 }
    }
) <br>  
3. [Creating a Table in Power BI Using DAX Table Constructor](https://radacad.com/creating-a-table-in-power-bi-using-dax-table-constructor)  
