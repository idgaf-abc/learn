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
final public function example(string $str, int $int) :?array {
    if ($str == "example") return null;
    if ($int == 3) return null;
    return [$str, $int]; 
}
```

`public` -> Funktionszugänglichkeit über andere Klassen
``

# Klassen

Klassen sind Funktionssammlungen, sie bringen Ordnung in den Code und machen das Sortieren von Funktionen nach Sinn und Logik einfacher.

# Imports

Um Funktionen aus anderen Klassen nutzen zu können, muss die Klasse, wo sich die Funktion drin befindet, in die Klasse wo du sie nutzen willst importiert werden. Imports werden meistens über der Klasse selber angegeben.

# Statements

