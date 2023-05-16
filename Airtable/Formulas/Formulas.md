### Template
```js
// here comment
const var = 'value'
```

### Adding 1 from button press
```js
// Change this name to use a different table
let table = base.getTable("TABLE_NAME");

// Prompt the user to pick a record 
// If this script is run from a button field, this will use the button's record instead.
let record = await input.recordAsync('Pick a record', table);


// Change this name to use a different field
let value = record.getCellValue("VALUE_FIELD_NAME")

// Adding 1 (change field name too)
await table.updateRecordAsync(record, {"VALUE_FIELD_NAME": value + 1});
```

### Currency field to number with thousands comma: X,XXX
```js
IF(LEN(Price&"")>3,LEFT(Price&"",LEN(Price&"")-3)&","&RIGHT(Price&"",3),Price&"")
```


### Switch date to next 1st
```js
DATETIME_PARSE(SWITCH(DATETIME_FORMAT({Date}, 'MM'), "01", "01/02", "02", "01/03", "03", "01/04", "04", "01/05", "05", "01/06", "06", "01/07", "07", "01/08", "08", "01/09", "09", "01/10", "10", "01/11", "11", "01/12", "12", "01/01") & "/" & IF(DATETIME_FORMAT({Date}, 'MM') = '12', YEAR({Date}) + 1, YEAR({Date})),'DD/MM/YYYY')
```

### Switch date to quarter
```js
SWITCH(DATETIME_FORMAT({Date Field},'MM'),"01","Q1","02","Q1","03","Q1","04","Q2","05","Q2","06","Q2","07","Q3","08","Q3","09","Q3","10","Q4","11","Q4","12","Q4") 
```

### Template
```js
// here comment
const var = 'value'
```

### Template
```js
// here comment
const var = 'value'
```


