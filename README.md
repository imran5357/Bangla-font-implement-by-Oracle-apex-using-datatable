# Bangla-font-implement-by-Oracle-apex-using-datatable


#Page Design Javascript File URLs
--------------------------------------------
<pre>
  #APP_IMAGES#jquery-3.5.1.js
  #APP_IMAGES#jquery.dataTables.min.js
  #APP_IMAGES#dataTables.buttons.min.js
  #APP_IMAGES#jszip.min.js
  #APP_IMAGES#pdfmake.min.js
  #APP_IMAGES#vfs_fonts.js
  #APP_IMAGES#buttons.html5.min.js
</pre>
#Function and Global Variable Declaration
---------------------------------------------
<pre>
/******* Customize Font ********/
pdfMake.fonts = {
    Roboto: {
        normal: 'Roboto-Regular.ttf',
        bold: 'Roboto-Medium.ttf',
        italics: 'Roboto-Italic.ttf',
        bolditalics: 'Roboto-MediumItalic.ttf'
    },
    nikosh: {
        normal: "NikoshBAN.ttf",
        bold: "NikoshBAN.ttf",
        italics: "NikoshBAN.ttf",
        bolditalics: "NikoshBAN.ttf"
    }
};


$(document).ready(function () {
    $('#report_table_example').DataTable( {
        dom: 'lBfrtip',
        lengthMenu: [[10, 20, 50, -1], [10, 20, 50, "All"]],
        //buttons: ['copy', 'csv', 'excel', 'pdf', 'print']
        buttons: ['csv', 'excel', 'pdf', 'print']
    } );
});

apex.jQuery("#example").on( "apexafterrefresh", function() {
    $('#report_table_example').DataTable( {
        dom: 'lBfrtip',
        lengthMenu: [[10, 20, 50, -1], [10, 20, 50, "All"]],
        buttons: ['csv', 'excel', 'pdf', 'print']
    } );
});
</pre>

#CSS File URLs
-------------------------------------------
<pre>
https://cdn.datatables.net/1.11.3/css/jquery.dataTables.min.css
https://cdn.datatables.net/buttons/2.0.1/css/buttons.dataTables.min.css
</pre>


#Inline CSS
-----------------------------------------
<pre>
#example input{
    background: #ffffff !important;
}

table.dataTable thead th {
    padding: 10px 16px;
}
table.dataTable thead td {
    padding: 3px 16px;
}

#btnSearch{
    margin-top: 35px;
}

</pre>
#Region Static ID
--------------------------
write: example
