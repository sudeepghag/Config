# Salesforce Configuration

### Validation with VLOOKUP [Link](https://success.salesforce.com/answers?id=90630000000gyFzAAI)

> VLOOKUP(field_to_return, field_on_lookup_object, lookup_value)

```
(4) Name = VLOOKUP(
(1) $ObjectType.Employee__c.Fields.Name ,  
(2) $ObjectType.Employee__c.Fields.Name ,  
(3) Name)
``` 

compare the Name (4) on the Current Record and the Name on that Employee record that matched with the same Name as of the one that we are creating now. Hence we use the equality operator (=). 

You could express the VLOOKUP formula as below: "Look into the Name(2) field on all the Employee Records and return value in it's Name (1) field if the it happens to be same as the Name (3) on the Current Record." 

Searches an object for a record where the specified field matches the specified lookup_value. If a match is found, returns another specified field value.

Points to Remember:
1. VLOOKUP only available on Custom Objects. Vote for this idea: https://success.salesforce.com/ideaView?id=08730000000BqPs
2. VLOOKUP only available in Validation Rules.
3. VLOOKUP can only be done on the Name fields.
4. The field_to_return must be an auto number, roll-up summary, lookup relationship, master-detail relationship, checkbox, date, date/time, email, number, percent, phone, picklist, text, text area, or URL field type.
5. The field_on_lookup_object must be the Record Name field on a custom object.
6. The field_on_lookup_object and lookup_value must be the same data type.
