# json2csv-converter

A lightweight utility package for converting JSON data to Excel (CSV) file.

## Installation

```shell
# with npm
npm install json2csv-converter

# with yarn
yarn add json2csv-converter
```

## Usage

```js
import { exportCSVFile } from "json2csv-converter";

function exportCarsData() {
  const headers = ["brandName", "model", "year"];
  const data = [
    { brandName: "Toyota", model: "Camry", year: "2006" },
    { brandName: "Honda", model: "Accord", year: "2012" },
    { brandName: "Hyundai", model: "Elantra", year: "2019" },
    { brandName: "Ford", model: "Mustang", year: "2002" },
    { brandName: "Bentley", model: "GT Continental", year: "2008" },
  ];
  const filename = "carsData";

  exportCSVFile(headers, data, filename);
}

exportCarsData(); //Invoking this function will download a carsData.csv document containing the above data
```

## Arguments

The `exportCSVFile` function accepts three arguments needed to generate and download a CSV file.

| Argument | Type   | Example                      | Notes                                                                                |
| -------- | ------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| headers  | array  | (See headers example above)  | Contains an array of data object keys that will be used as headers in the excel file |
| data     | array  | (See data example above)     | Contains a javascript array of object with keys (matching the headers) and values    |
| filename | string | (See filename example above) | Generated CSV file will be named using the filename or a default will be use instead |

## License

MIT
