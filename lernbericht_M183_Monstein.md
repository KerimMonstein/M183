# Lern-Bericht
Kerim Monstein

## Einleitung

Dieser Lernbericht umfasst das Modul 183. Darin geht es um Applikationssicherheit.

## Was habe ich gelernt?

Ich habe gelernt wie Cross Site Scripting (XSS) funktioniert und wie man eine Seite davor schützt.

## Beschreibung

Die Grundidee von Cross Site Scripting ist JavaScript-Code auf eine Seite einzuschleusen. Dies kann über Eingabefelder geschehen. Wenn andere Seitenbesucher sich die Seite ansehen führt der Browser bei ihnen den Code des Angreifers aus, da dieser nicht als Inhalt, sondern als JavaScript interpretiert wird. 
Um sich davor zu schützen, gibt es die Varianten Escaping, Black- oder Whitelisting. Bei letzteren beiden werden bestimmte Eingaben nicht oder eben doch erlaubt. Bei der Escaping Variante werden bestimmte Symbole, welche für das Erstellen von Tags nötig sind, anders geschrieben z.B. `<` --> `&lt;`.

Wenn man es nicht Spezifisch deaktiviert betreibt JSF escaping automatisch. Man kann es aber auch explizit für ein Feld auf `true` setzen.

```java
<h:outputText value="#{newsitem.detail}" escape="true"/>
```

![XSS](https://user-images.githubusercontent.com/69577029/207854147-b584165b-62e7-49bc-8b20-6866031175e7.gif)

## Verifikation

Im GIF zeige ich ein simples XSS Beispiel. Im Text beschreibe ich genauer, wie diese funktioniert und wie man sich davor schützt, sieht man ebenfalls im Code-Snippet.

# Reflektion zum Arbeitsprozess

Das Konzept von Cross Site Scripting fand ich relativ gut verständlich. Dank der Aufgabe auf [Hacksplaining](https://www.hacksplaining.com/exercises/xss-stored) konnte ich es noch besser nachvollziehen.
Am Anfang war ich verwirrt wie ich XSS Angriffe escapen kann, danach ist mir jedoch aufgefallen das JSF dies bereits automatisch macht.

**VBV**: Ich sollte Aufgaben, mit denen ich im Unterricht nicht fertig werde, zu Hause fertig lösen.
