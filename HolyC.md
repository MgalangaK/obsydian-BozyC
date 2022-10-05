HolyC został stworzony do napisania [[TempleOS]] przez [[Terrence Andrew Davis]].

HolyC ("Święty C"/"C Boży") jak sama nazwa wskazuje, jest niczym język [C](https://en.wikipedia.org/wiki/C_(programming_language)) z kilkoma różnicami jak kompilowanie w assembly,

```
TempleOS uses nonstandard opcodes. Asm is kind-of a bonus and I made changes to make the assembler simpler.
```

***FUNKCJE***
Większe zmiany można zauważyć w funkcjach, by wywołac funkcję bez argumentów wystarczy tylko wpiseć jej imie.``
```C
x = Foo(); // C
d = Foo; // Holy C
```
HolyC zezwala na podstawowe argumenty
```C
I32 Foo(I32 i=2, I32 j)
{
	return(i+j);
}

I32 x;
x = Foo(,6)
```

***SWITCH***
Według autora switch jest najbardziej wydajnym rzeczą w jego języku, switch w HolyC pozwala zutylizowac jump tables w assembly.
```C
I34 i;

switch (i) {
	case: "0"; break;
	case: "1"; break;
	case: "2"; break;
	case 3: "3" break;
	case 4...8: "x"; break; //dla case od 4 do 8 wypisuje "x"
}
```