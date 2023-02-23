## Import Data from an Excel file

- Add an excel file in `lib` directory

  ```
  mkdir lib
  
  touch lib/products.xlsx
  ```

- **Note:** Excel file has two cols `Name` and `Price`.

- Change the Ruby object `Product` to match your object.

- Run the `rake` task.

- `bundle install`

```rb
rake import:data
```

