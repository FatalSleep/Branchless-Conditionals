# Branchless-Conditionals
IF branches are slow, so here are some solutions using GML, 'cuz I like GML.

```GML
//smaller(a,b)
//Returns the smaller value of A or B.
var c = a<b;
return (a*c) + (b*(1-c));
```
```GML
//smallerx(a,b,c,d)
//Returns the C if A<B or D if B<A.
var e = a<b;
return (c*e) + (d*(1-e));
```
```GML
//smaller(a,b,*sA,*sB,args)
//Returns the result of the executed script sA if A<B or sB if B<A using "var arg" or "array arg" or "ds_list args".
var e = a<b;
return script_execute((sA*e) + (sB*(1-e)), args);
```
