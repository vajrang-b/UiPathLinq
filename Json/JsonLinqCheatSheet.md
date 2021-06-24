#jsonLinqCheatSheet


Question |Function Method  | Query Method
-------|------------- | -------------
Get List of all country Names   |   jArrayCountries.Select(function(c) c("name"))   |   from c in jArrayCountries select c("name")
Get List of all country Names that starts with A   |   jArrayCountries.Where(function(c) c("name").ToString.StartsWith("A")).   |    (from country in jArrayCountries Where country("name").ToString.StartsWith("A"))
Get List of all country Names that Contains A   |   jArrayCountries.Where(function(c) c("name").ToString.Contains("A")).   |    (from country in jArrayCountries Where country("name").ToString.Contains("A"))
Get List of all countries whose name length is greater than 10   |   jArrayCountries.Where(function(c) c("name").toString.Length > 10 ).   |   (From country in jArrayCountries where country("name").toString.Length > 10)
Get List of all country flag urls   |   jArrayCountries.select(function(c) c("flag"))   |   (from country in jArrayCountries Select country("flag"))
Countries which have 1 border   |   jArrayCountries.Where(function(c) c("borders").Count.Equals(1) ).Select(function(c) c("name"))   |   (From country in jArrayCountries where country("borders").count = 1 ).Count
Countries with more than 5 borders   |   jArrayCountries.Where(function(c) c("borders").Count > 5).Select(function(c) c("name"))   |   (From country in jArrayCountries where country("borders").count > 5  select country("name"))
countries with transalations more than 9   |   jArrayCountries.Where(function(c) c("translations").Count > 9).Select(function(c) c("name"))   |   (from country in jArrayCountries where country("translations").Count > 9 select country("translations"))
