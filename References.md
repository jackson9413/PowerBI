# Table Measure
## Create new table based on existing table with filter condition
TraineesLatestCompleteWithdrawal = 
CALCULATETABLE (
    TraineePrograms,
    FILTER (
        TraineePrograms,
        TraineePrograms[RowId] = 1
            && (
                CONTAINSSTRING ( TraineePrograms[Status__c], "complete" )
                    || CONTAINSSTRING ( TraineePrograms[Status__c], "withdraw" )
            )
    )
)
