# MY_Form_validation-for-CI
Custom form validation

datetime - checks if the format of input is of DATETIME format

phone_number - checks if the input has at least 11 numerical values by eliminating '+', '-', '.', ' ', '(', ')' from the string.

is_unique_except - checks if the input is unique in a table, and the value is not in the row that is analysed. A good rule for when you need to edit a field of a row but want to make sure that if the value is changed that value is unique inside the table:

```php
$this->form_validation->set_rules('username','Username','trim|required|is_unique_except[users.username.id.'.$id.']';
```
You pass it the table name, the field name, the primary key name and the value of the primary key.

not_in_list - makes sure the input value is not the same as the elements passed to the rule (same as in_list but the other way around)
