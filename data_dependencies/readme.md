# Data Dependencies

## Module/Data Source Dependencies:
\[Insert opening statement\]
1. Attendance Data (e.g. SIS Module)
2. SIS Data (e.g. SIS Module)
3. Activity Data (e.g. Microsoft Education Insights Module)
4. Behavior Data (e.g. ) \[MIGHT REMOVE\]

## NOTES ON CURRENT ACTIVITY RELATIONSHIP TABLE:
Can we write all these tables to Delta vs. unstructured format of JSON.
<em> 3 Over-arching concepts: </em> 
1. Event Class/Table (THIS ONE):
    - Current idea is to use this as basic, fast first iteration
    1. id - (column SignalID from Insights Activity Table)
    2. type - ToolUseEvent class
    3. actor - AAD ID
    4. action - Used
    5. object - SoftwareApp class (AppNames column from Insights Activity table)
    6. eventTime - TimeStamp Type
    7. generated - AggregateMeasures class
    8. edApp - 
2. SoftwareApplication Class/Table (THIS ONE):
    1. type
    2. host
    3. ipAddress
    4. 
3. Tool Use Event Table \[IGNORE HERE FOR NOW\]:
    1. Event - ToolUseEvent
    2. Actor - StudentId
    3. Action - Used
    4. Object - SoftwareApplication
    5. Generated - AggregateMeasureCollection
4. AggregateMeasure

5. Action Table/Class (TO BE ADDED)
### References:
| Resource | Description |
| --- | --- |
| [ToolUseEvent Table](https://www.imsglobal.org/spec/caliper/v1p2#ToolUseEvent) | Information and specs on ToolUseEvent table. |
| [Event Class/Table](https://www.imsglobal.org/spec/caliper/v1p2#Event) | Information and specs on Event class. |
| [Microsoft Graph beta endpoint reference](https://docs.microsoft.com/en-us/graph/api/overview?view=graph-rest-beta) | API reference doc for Graph's beta version (used in this sample module). |
| [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) | Utility that allows you to easily try out Graph API endpoints. |

