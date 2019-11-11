# Laravel snippets

### Filter for search
```php
if ($requestFilter = $request->query()){
    foreach ($requestFilter as $key => $filter){
        foreach ($filter as $value)
            $products->where('params->'.$key, $value);
    }
}
```	