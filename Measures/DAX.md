- [Count Distinct By Joining Two Table](#count-distinct-two)  
<a id='count-distinct-two'></a>
employerscount = 
COUNTROWS (
    INTERSECT (
        VALUES ( dim_employers[Id] ),
        VALUES ( fact_enrollments[accountid] )
    )
)

