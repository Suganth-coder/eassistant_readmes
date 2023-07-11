Task APIS

## Adding the Task

API Path : `Mobile APIs > Task APIs > Adding the Task`

* Input Type: `HTML Form` 
* Parmeters 
    - attachment files (Multiple Files)
    - task_data (Json Task Data)

`Note`: Intial Attachments files will be passed while creating the task api

## Adding new attachments to existing tasks

API PATH : `Mobile APIs > Task APIs > Attachments Updations > Adding new attachments`

* Input Type: `HTML Form`
* Parameters
    - attachment_files (Multiple Files)
    - task_id 

## Deleting existing attachments from the tasks

API PATH : `Mobile APIs > Task APIs > Attachments Updations > Deleting attachments`

* Input Type:  `Json`
* Parameters
    - attachment_names: [array]
    - task_id

## Updating the Tasks

Note: `Here attachments cant be updated. Attachments can be only updated using above APIs`

API PATH: `Mobile APIs > Task APIs > Updating the Task`

* Input Type: `Json`

Here, for assign_to and share_with Params, If you want to add new assignes pass the old assignes too

Example,

Old data
```
    "assign_to": [
        {"user_id":id1}
    ]
```
If i need to add new assign member with user id `id2`. Then i need to pass like below,

New data for updation
```
    "assign_to": [
        {"user_id":id1},
        {"user_id":id2}
    ]
```

Here, you have two new parameters for updations,

```
    * status
    * completion_status
```

These, parameters are set default status=inprogress, completion_status = 0, at the time of creation of tasks. You can update this params, in this update API

## Deleting the Tasks

API PATH: `Mobile APIs > Task APIs > Deleting the Task`

* Input Type: Json
* Paramters
    - task_id

## Recurring Task Formats

### For Days
* [InDefinite Recurring Day Task Format](./recurring%20task%20formats/indefinite_day.json)
* [End Date Recurring Day Task Format](./recurring%20task%20formats/enddate_day.json)

### For Weeks
* [InDefinite Recurring Week Task Format](./recurring%20task%20formats/indefinite_week.json)
* [End Date Recurring Week Task Format](./recurring%20task%20formats/enddate_week.json)

### For Month
* [InDefinite Recurring Month Task Format](./recurring%20task%20formats/indefinite_month.json)
* [End Date Recurring Month Task Format](./recurring%20task%20formats/enddate_month.json)

