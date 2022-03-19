# sum_calculate_jquery
jQuery: Calculate Sum Of all Textbox Values In a Table Column
<table id="myTable">
<tr>   <th width="100">Name </th>
    <th>Price</th>
</tr>
<tr>
    <td><span>Pen :</span></td>
    <td><input type="text" class='txtCal' /></td>
</tr>    
<tr>
    <td><span>Pencil :</span></td>
    <td><input type="text" class='txtCal' /></td>
</tr>  
<tr>
    <td><span>Eraser :</span></td>
    <td><input type="text" class='txtCal' /></td>
</tr>  
<tr>
    <td><span>Sharpner :</span></td>
    <td><input type="text" class='txtCal' /></td>
</tr>  
<tr>
    <td><span>Book :</span></td>
    <td><input type="text" class='txtCal' /></td>
</tr>
<tr>
    <td><span><b>TOTAL  :</b></span></td>
    <td><b><span id="total_sum_value"></span></b></td>
</tr>
</table>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script>
//*


 //*
$(document).ready(function () {
       
    $("#myTable").on('input', '.txtCal', function () {
       // code logic here
        var getValue=$(this).val();
        console.log(getValue);
    });

 });
 
 
 $(document).ready(function () {
       
    $("#myTable").on('input', '.txtCal', function () {
       var calculated_total_sum = 0;
     
       $("#myTable .txtCal").each(function () {
           var get_textbox_value = $(this).val();
           if ($.isNumeric(get_textbox_value)) {
              calculated_total_sum += parseFloat(get_textbox_value);
              }                  
            });
              $("#total_sum_value").html(calculated_total_sum);
       });
  });
//*
</script>
