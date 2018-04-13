# react-bootstrap-table-plus

## [`react-bootstrap-table`](https://github.com/react-bootstrap-table/react-bootstrap-table) is the core of this. This is the same with some additional functionality.

It's a [react.js](http://facebook.github.io/react/) table for bootstrap, named react-bootstrap-table-plus. It's a configurable, functional table component and make you build a Bootstrap Table more efficiency and easy in your React application, However ```react-bootstrap-table-plus``` support these features:

### react-bootstrap-table features:
- Striped, borderless, condensed table
- Column align, hidden, width, sort, title, styling, customization
- Table scrolling
- Cell format
- Pagination
- Row selection
- Table Search, Column filter
- Cell editor
- Insert & delete Row
- Export to CSV
- Rich function hooks
- Header column span
- Remote mode
- Row expand
- Key board navigation

### react-bootstrap-table-plus unique features:
- Edit button

## Documentation for react-bootstrap-table
See more about [react-bootstrap-table](http://allenfang.github.io/react-bootstrap-table/index.html) and explore more examples on [examples](https://github.com/AllenFang/react-bootstrap-table/tree/master/examples/js) folder</br>
Check the <a href='https://github.com/AllenFang/react-bootstrap-table/blob/master/CHANGELOG.md'>CHANGELOG</a> for more detail release notes.

## To enable the Edit button:
Add ```editRow={ true }``` to the ```<BootstrapTable>``` just as you would with the ```addRow={ true }```

![Example](https://i.imgur.com/Btk74Xb.png)
![Example](https://i.imgur.com/VoFjKP3.png)

## Notes


***`v1.0.0` released, this release adds an Edit button to the toolbar***


## Usage
### a.Install
```bash
npm install react-bootstrap-table-plus --save
```

### b.Import Module
To use react-bootstrap-table-plus in your react app, you should import it first.

##### With a module bundler
With a module bundler like [webpack](https://webpack.github.io/) that supports either CommonJS or ES2015 modules, use as you would anything else.  
You can include source maps on your build system to debug on development. Don't forget to Uglify on production.

```js
// in ECMAScript 6
import { BootstrapTable, TableHeaderColumn } from 'react-bootstrap-table-plus';
// or in ECMAScript 5
var ReactBSTable = require('react-bootstrap-table-plus');  
var BootstrapTable = ReactBSTable.BootstrapTable;
var TableHeaderColumn = ReactBSTable.TableHeaderColumn;
```

### c.Import CSS
Finally, you need to import the css file to your app:
```html
<!-- we still need bootstrap css -->
<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">
<link rel="stylesheet" href="./dist/react-bootstrap-table.min.css">
```
The CSS files you can find in the css folder.

### Quick Demo
```js
// products will be presented by react-bootstrap-table
var products = [{
      id: 1,
      name: "Item name 1",
      price: 100
  },{
      id: 2,
      name: "Item name 2",
      price: 100
  },........];
// It's a data format example.
function priceFormatter(cell, row){
  return '<i class="glyphicon glyphicon-usd"></i> ' + cell;
}

React.render(
  <BootstrapTable data={products} striped={true} hover={true}>
      <TableHeaderColumn dataField="id" isKey={true} dataAlign="center" dataSort={true}>Product ID</TableHeaderColumn>
      <TableHeaderColumn dataField="name" dataSort={true}>Product Name</TableHeaderColumn>
      <TableHeaderColumn dataField="price" dataFormat={priceFormatter}>Product Price</TableHeaderColumn>
  </BootstrapTable>,
	document.getElementById("app")
);
```

### [Documentation](http://allenfang.github.io/react-bootstrap-table/docs.html)

### Thanks
**[AllenFang](https://github.com/allenfang)**  
Original creator of the base of this project.   