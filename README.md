# tableToCSV

This tool converts an HTML table to CSV file

## Getting Started

If you like me, have a problem when you want to convert an HTML table to some excel format (CSV for example) and you don't want to create a backend service to create that file, you can use this tool.
I didn't found a library that I liked to do this (December 2017), that's why I decided to make my own tool.
This tool is a pure Javascript, you don't need any other dependencies.

### Installing

All you have to do, is to add the tableToCSV.js file into your main HTML (maybe index.html)

```html
<script src="tableToCSV.js"></script>
```

And then, call the function (you can add the action in a button for example):

```javascript
tableToCSV.convertToTable(idOfTheTable);
```

At the end of the execution, you will see a window just to save your file in CSV format

Or you can install via bower:
```vctreestatus
bower install table-to-csv
```

## Full example

HTML file (angularJS example)

```html
<div>
    <table id="idOfTheTable">
      <thead>
        <tr>
          <th>Title1</th>
          <th>Second title</th>
	      <th>Third title</th>
	      <th>More titles</th>
	      <th>More titles</th>
	    </tr>
	  </thead>
	  <tbody>
	    <tr>
	      <td>row1-1</td>
	      <td>row1-2</td>
	      <td>row1-3</td>
	      <td>test</td>
	      <th>child</th>
	    </tr>
	    <tr>
	      <td>row2-1</td>
	      <td>row2-2</td>
	      <td>row2-3</td>
	      <td>test</td>
	      <th>child</th>
	    </tr>
	    <tr>
	      <td>row3-1</td>
	      <td>row3-2</td>
	      <td>row3-3</td>
	      <td>test</td>
	      <th>child</th>
	  </tbody>
    </table>
    <button ng-click="exportData()">Generate</button>
</div>
```

Controller function
```javascript
$scope.exportData = function(){
    tableToCSV.convertToTable(document.getElementById("idOfTheTable"));
};
```

This will generate a file with CSV format like this:

```vctreestatus
Title1, Second title, Third title, More titles, More titles
row1-1, row1-2, row1-3, test, child
row2-1, row2-2, row2-3, test, child
row2-1, row2-2, row2-3, test, child
```


## Contributing

Please read [CONTRIBUTING.md](https://github.com/snake404/tableToCSV/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.



We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/snake404/tableToCSV/tags). 

## Authors

* **Cristian Alanis** - *Initial work*

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](https://github.com/snake404/tableToCSV/blob/master/LICENSE) file for details