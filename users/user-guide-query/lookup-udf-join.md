# Lookup UDF Join

Lookup UDF is used to get dimension data via primary key from a dimension table allowing a decoration join functionality. Lookup UDF can only be used with [a dimension table](../../basics/data-import/batch-ingestion/dim-table.md) in Pinot. The UDF signature is as below:

```
lookUp('dimTableName', 'dimColToLookUp', 'dimJoinKey1', factJoinKeyVal1, 'dimJoinKey2', factJoinKeyVal2 ... )
```

* `dimTableName` Name of the dim table to perform the lookup on.&#x20;
* `dimColToLookUp` The column name of the dim table to be retrieved to decorate our result.
* `dimJoinKey` The column name on which we want to perform the lookup i.e. the join column name for dim table.&#x20;
* `factJoinKeyVal` The value of the dim table join column for which we will retrieve the dimColToLookUp for the scope and invocation.&#x20;

Return type of the UDF will be that of the dimColToLookUp column type. There can also be multiple primary keys and corresponding values.

{% hint style="warning" %}
**Note**: If the dimension table uses a composite primary key i.e multiple primary keys, then ensure that the order of keys appearing in the lookup() UDF is same as the order defined for **"primaryKeyColumns"** in the dimension table schema.
{% endhint %}
