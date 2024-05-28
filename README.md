Beispiele erklärt an PHP
Nur grundlegendes

# Datentypen

Programmiersprachen bauen auf Datentypen auf. Datentypen beschreiben die Art eines Wertes, also unterscheiden in Zahlen, Wörtern/Sätze, wahr/falsch.

Die wichtigsten Datentypen sind:
> **String**: Wörter/Sätze immer in "" angegeben.

> **Integer**: Einzelne Zahlen. Keine Kommazahlen.

> **Float**: Kommazahlen.

> **Boolean**: Festgelegte Werte auf true oder false. Kann keine anderen Werte haben.

> **Array**: Eine Liste. Meistens mit [] angegeben. Arrays haben immer wie eine Art Inhaltsverzeichnis durch ein Index sortiert ab 0 oder 1 (abhängig von der Sprache) aufwärts.

# Operatoren

**+** -> Addition

**-** -> Subtraktion

**\*** -> Multiplikation

**/** -> Division

**&** -> UND (möglicherweise Abweichender Operator in anderen Sprachen)

**?** -> NULL-Shift (Abfrage ob ein Wert = NULL ist.)

**<** -> Geringer als [...]

**>** -> Größer als [...]

**++** -> +1

**--** -> -1

# Variablen

Variablen geben Flexibilität in den Code. Abhängig vom Zugänglichkeitsstatus veränderbar und zugänglich. Eine festgelegte Art Variablen festzulegen gibt es nicht, in den meisten Sprachen gibst du es aber nach einem der beiden Schemen an:

> [Datentyp] [(evtl. Vorzeichen)Variablen Name] = [Wert]
> [(evtl. Vorzeichen)Variablen Name] [Datentyp] = [Wert]

```php
// String
$str = "Hallo";

// Integer
$int = 1;

// Float
$float = 0.1;

// Boolean
$tbool = true;
$fbool = false;

// Array
$ar = [
    $str,
    $int,
    $float,
    $tbool,
    $fbool
];
```

# Funktionen

Funktionen sind Code-Abfolgen. Funktionen laufen chronologisch ab, also von oben nach unten, müssen allerdings nicht in der Reihenfolge fertig sein, in der sie gestartet werden. Abhängig von Computer Resourcen wie z.B. RAM könnten Informationen erst verzögert aus den Funktionen ausgegeben werden. Passiert selten und in nur wenigen Fällen und auch meistens nur in synchronen Abläufen. Ein festes Schema gibt es hier auch nicht, ist also abhängig von der Sprache. Beispiel Funktion (PHP):

```php
final public function example(string $str, int $int = 3) :?array {
    if ($str == "example") return null;
    if ($int == 3) return null;
    return [$str, $int]; 
}
```
`final` -> Optional, verhindert das überarbeiten der Funktion

`public` -> Funktionszugänglichkeit über andere Klassen

`"example"` -> Funktionsname, frei wählbar, sollte keine Zahlen oder Sonderzeichen enthalten

`"string $str, int $int"` -> Funktionsparameter. Müssen, wenn kein Standardwert angegeben wurde, beim Aufrufen der Funktion angegeben werden, damit die Funktion ordnungsgemäß funktionieren kann.

`":?array"` -> Return Type. Funktionen geben Werte zurück, der ":" markiert den Return Type, der Null Shift Operator markiert einen möglichen NULL Wert als zurückgegebenen Wert und "array" sagt aus, dass ansonsten definitiv ein Array zurück gegeben wird.

`"{...}"` -> Funktionsinhalt. Der Code der ausgeführt werden soll, wenn die Funktion aufgerufen wird. 

`"return [...]"` -> Return Value. Das was nach dem "return" angegeben wird, ist der Wert, den die Funktion zurückgibt, sobald die Funktion endet.


# Klassen

Klassen sind Funktionssammlungen, sie bringen Ordnung in den Code und machen das Sortieren von Funktionen nach Sinn und Logik einfacher.

# Imports

Um Funktionen aus anderen Klassen nutzen zu können, muss die Klasse, wo sich die Funktion drin befindet, in die Klasse wo du sie nutzen willst importiert werden. Imports werden meistens über der Klasse selber angegeben.

# Statements

Statements werden meistens für Abfragen oder Abfolgen genutzt. Statements werden die Funktionen angewendet.

`"if"` -> Eine einfache "Wenn"-Abfrage. Bsp.:

```php
if ($str == "example") return null;
```

Erklärung: Wenn die Variable "str" gleich dem String "example" ist, wird NULL zurückgegeben.

`"else"` -> Gegenstück zum "if"-Statement. Bsp.:

```php
if ($str == "example") {
    return null;
} else {
    return $str;
}
```

Erklärung: Wenn die Variable "str" gleich dem String "example" ist, wird NULL zurückgegeben, ansonsten wird der Wert der Variable "str" zurückgegeben.

`"for"` -> Eine Unendliche Schleife, solange die Bedingung der Schleife erfüllt wird. Bsp.:

```php
for ($x = 0; $x < 100; $x++) {
    echo $x;
}
```

Erklärung: Es wird eine Schleife erstellt. Dazu erstellen wir eine neue Variable,"x" gleich 0, Zweckgebunden an die Schleife. Solange die neu erstellte Variable "x" geringer als 100 ist, wird immer mit jeder abgeschlossenen Codeabfolge der Schleife, die Variable "x" um eine ganze Zahl höher. Sollte die Bedingung erfüllt sein, wird die Codeabfolge `{...}` weiter ausgeführt, bis sie nicht mehr erfüllt wird. Damit endet die Schleife und der Code läuft nach der Schleife weiter. Eine FOR-Schleife wird öfter für Zahlengebundene Schleifen verwendet.

`"while"` -> Eine Unendliche Schleife, solange die Bedingung der Schleife erfüllt wird. Bsp.:

```php
$x = true;
$y = 1;
while ($x === true) {
    $y++;
    if ($y == 30) $x = false;
}
```

Erklärung: Wir erstellen eine Variable "x" mit dem Wert "Wahr" und eine Variable "y" mit dem Wert 1. Anschließend folgt eine WHILE-Schleife, mit der Bedingung, dass die Variable "x" gleich "Wahr" sein muss und immernoch ein Boolean sein muss. Innerhalb der Schleife wird der Variable "y" immer eine Zahl hinzugefügt, und anschließend abgefragt, ob die Variable "y" gleich 30 ist. Sollte die Variable "y" gleich 30 sein, wird die Variable "x" auf Falsch gesetzt und die Schleifen Bedingung gebrochen. Die Schleife läuft nach 30 Versuchen demnach nicht mehr weiter und der Code läuft nach der WHILE-Schleife weiter.

`"switch"` -> Alternative zu vielen IF-ELSE-Statements. Kann in eine Abfrage viele Szenarien einbauen für die Abfrage. Bsp.:

```php
$type = null;
switch (gettype($x)) {
   
    case "string":
        $type = "string";
    break;

    case "integer":
        $type = "integer";
    break;
    
    case "boolean":
        $type = "boolean";
    break;

}
```

Erklärung: Wir erstellen eine Variable "type" mit dem Standard Wert NULL. Anschließend folgt ein SWITCH-Statement, welches mehrere Fälle für das Return Value der Funktion `gettype($x)` enthält. Ein Fall beginnt mit `case` und dem anschließendem Fall-Wert in "" angegeben. Nach dem ein `:` den nachfolgenden Code für den Fall markiert, folgt der besagte Code für den Fall, und anschließend ein `break` welches das Ende des Falls markiert.