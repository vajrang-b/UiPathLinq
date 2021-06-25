
# **if row value starts with a word**


Function Method  | Query Method
------------- | -------------
dt.AsEnumerable.Where(Function(row) row("Name").toString.StartsWith("bajaj")) | (From row In dt.Select() Where row("Name").ToString.StartsWith("bajaj") Select row).ToArray




