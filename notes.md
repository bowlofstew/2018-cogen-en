Abstract:

# Einführung & Praxisreport: Coroutinen als Generatoren

Wie komplexe Zustandsautomaten mit Hilfe von Co-Routinen zu einfach wartbaren und testbaren Funktionen werden können.
Mit C++17 ist auch der Coroutine TS (Technical Specification) verabschiedet worden. Auf verschiedenen Konferenzen wurden die Vorzüge von Co-Routinen für bessere asynchrone Programmierung erklärt. Die C++ Co-Routinen können aber noch viel mehr.

Goals:

* Einsatz von Co-Generatoren zeigen
* Lesbarkeit vs. Speed

Papers:
2004 "Revisiting Coroutines" Rio/Brazil: http://www.inf.puc-rio.br/~roberto/docs/MCC15-04.pdf 

Story:
* Rebuild Compiler
* Rewrite with C++17
* C# Enumerator - yield
* CoRoutines TS

Ideen:

classic function
  Request -> Response
  Rest

co-routine
  Call + Resume

co-routine

co-ncurrency
co-ntinue

keywords:
co_yield
co_await
co_return


```cpp
auto numbers() {
    return std::vector{23, 42};
}
```

```cpp
auto numbers() {
  
}
```

```cpp
auto numbers() {
    co_yield 23;
    co_yield 42;
}
```


```cpp
auto numbers() -> Generator<int> {
    std::cout << "before!\n";
    co_yield 42;
    std::cout << "between!\n";
    co_return 23;
    std::cout << "after!\n";
}
```

=> Realer Code!

UTF8 Decoder

Scanner

---

Error handling

///// remarks

-- complex examples

// switch context (hard to follow)

++ mark generated code
