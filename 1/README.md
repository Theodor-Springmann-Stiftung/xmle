# Einfüḧrung XML

## TOC
1. XML - Wohlgeformtheit & Gültigkeit
    - Exkurs: Git
2. XSLT & Transformation

## 1. XML - Wohlgeformtheit & Gültigkeit
### 1.1 Wohlgeformtheit
- Es gibt *kein* nicht wohlgeformtes XML-Dokument
    - Strikte Sprache
- Was gehört zur Wohlgeformtheit
    - Zeichensatz
        - Zeichensätze insgesamt, CDATA (]]>), Kommentare(auf -- muss > folgen), PI (?>)
        - NameStartChar PI, elementnamen, attributnamen
        - Attribute values: " oder ', Entity & Char refs erlaubt
        - NameChar -- namensraum
        - CharData
            - Verbotene Zeichen? <, & (nicht: >, außer in ]]>)
            - Character Entities: &#[0-9]+; &#x[0-9a-fA-F]+;
                // keine external Entities in Attributen
                // external Entities zwar spezifiziert, aber nicht empfohlen
                // Recusive Entities verboten
            - Named entites: &lt; &gt; &amp; &apos; &quot;
        // DTD überspringen
    - Verschachtelung
        - prolog ghört nicht dazu!
        - Eindeutige Wurzel, gewurzelter, geordneter Baum
        - Vor/Nach der Wurzel: Comment, PI, S
    - Attributwerte in Anführungszeichen, whitespace in elementen (attribute nicht doppelt)
        // Sidenote: Whitespace in TEI


