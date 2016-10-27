# scim-filtering
SCIM query filter parser

##Usage
`todo`

##SCIM Filtering documentations
`SCIM version 1.1`
###Attribute operators
|Operator|Description|Behavior|
|--------|-----------|--------|
|`eq`|_equal_|The attribute and operator values must be identical for a match.|
|`co`|_contains_|The entire operator value must be a substring of the attribute value for a match.|
|`sw`|_starts with_|The entire operator value must be a substring of the attribute value, starting at the beginning of the attribute value. This criterion is satisfied if the two strings are identical.|
|`pr`|_present (has value)_|If the attribute has a non-empty value, or if it contains a non-empty node for complex attributes there is a match.|
|`gt`|_greater than_|If the attribute value is greater than operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison and for DateTime types, it is a chronological comparison.|
|`ge`|_greater than or equal_|If the attribute value is greater than or equal to the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison and for DateTime types, it is a chronological comparison.|
|`lt`|_less than_|If the attribute value is less than operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison and for DateTime types, it is a chronological comparison.|
|`le`|_less than or equal_|If the attribute value is less than or equal to the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison and for DateTime types, it is a chronological comparison.|

###Logical operators
|Operator|Description|Behavior|
|--------|-----------|--------|
|`and`|Logical And|The filter is only a match if both expressions evaluate to true.|
|`or`|Logical Or|The filter is a match if either expression evaluates to true.|

###Grouping operators
|Operator|Description|Behavior|
|--------|-----------|--------|
|`()`|Precedence grouping|Boolean expressions may be grouped using parentheses to change the standard order of operations; i.e., evaluate OR logical operators before logical AND operators.|