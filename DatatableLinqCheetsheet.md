
if row value starts with a word

Function Method

"dt.AsEnumerable.Where(
Function(row) row(""Name"").toString.StartsWith(""bajaj"")
	)"

Query Method

  "(From row In dt.Select() 
Where row(""Name"").ToString.StartsWith(""bajaj"") 
Select row).ToArray"
  
