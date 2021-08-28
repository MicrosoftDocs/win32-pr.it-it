---
title: Tipi VML di base
description: Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (VML), tipi di base
- VML (Vector Markup Language),tipi di base
- grafica vettoriale, tipi VML di base
- Vector Markup Language (VML), tipi
- VML (Vector Markup Language), tipi
- grafica vettoriale, tipi VML
- tipi VML di base
- tipo booleano
- tipo frazione
- tipo ordinate
- tipo di lunghezza
- Tipo di misura
- tipo di angolo
- tipo di colore
- tipo di carattere
- tipo bitmap
- Tipo vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a640dbacf875284008714ae404ba462b61652067
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883273"
---
# <a name="basic-vml-types"></a>Tipi VML di base

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introduzione](#introduction)
-   [boolean](#boolean)
-   [Frazione](#fraction)
-   [Ordinata](#ordinate)
-   [length](#length)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [Misura](#measure)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [Angolo](#angle)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [color](#color)
    -   [Unità di colore](#color-units)
    -   [Colori HTML](#html-colors)
    -   [Colori dello schema](#scheme-colors)
    -   [Colori di sistema](#system-colors)
    -   [Colori puri](#pure-colors)
    -   [Regolazioni del colore](#color-adjustments)
-   [Carattere](#font)
-   [bitmap](#bitmap)
    -   [Formati di file di immagine](#picture-file-formats)
-   [Vettore](#vector)

## <a name="introduction"></a>Introduzione

Questa proposta usa un numero ridotto di tipi di base, elencati nella tabella seguente.



| Tipo                  | Elemento           | Rappresentazione fondamentale | Descrizione                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 bit                      | Valore booleano: true o false.                                                                      |
| [Frazione](#fraction) |                   | numero 2 6                 | Valore numerico, ridimensionato di 2 6 (65536) e archiviato come intero con segno.                               |
| [Ordinata](#ordinate) |                   | Segno più intero a 30 bit   | Parte di una coordinata (ad esempio, in un percorso ), i valori definiti da coord.                                |
| [length](#length)     |                   | [EMU](#length)             | Lunghezza fisica, ad esempio la larghezza di una riga o la dimensione di un tipo di carattere.                                |
| [Misura](#measure)   |                   | EMU o numero 2 6          | Lunghezza fisica, incluso un numero di pixel del dispositivo, o una frazione di un'altra quantità. |
| [Angolo](#angle)       |                   | gradi 2 6                | Angolo; positive è in senso orario.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Elemento che consente di derivare un colore.                                                        |
| [Carattere](#font)         | [Carattere](#font)     | complex                    | Descrizione di un tipo di carattere.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Riferimento a un file di immagine esterno.                                                             |
| [Vettore](#vector)     | [v](#vector)      | complex                    | Descrizione di un percorso vettoriale                                                                       |



 

La "rappresentazione fondamentale" è la rappresentazione di precisione più elevata che la proposta richiede un'implementazione conforme da mantenere; I dati andranno persi se l'implementazione non è in grado di rappresentare i dati con la precisione richiesta. I tipi di colore, carattere e vettore corrispondono agli elementi che hanno struttura. In un certo senso, non sono tipi di base; Tuttavia, è utile considerarli come tali all'interno di questa proposta.

A ogni tipo di base non complesso è associato un elemento con lo stesso nome. Questi nomi di elemento sono riservati e non possono essere usati per altri scopi all'interno delle estensioni, anche se l'uso si trova all'interno di un elemento di estensione onview="skip". Per questo motivo, un'implementazione che rileva codice XML sconosciuto può fornire un'archiviazione interna efficiente del codice XML sconosciuto, purché i valori siano racchiusi tra gli elementi "type".


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



Nel primo esempio precedente, la stringa "1.578" deve essere archiviata come sequenza di caratteri (l'implementazione non sa se si tratta di una stringa o di un numero); Nel secondo esempio, l'elemento fraction indica che il contenuto è un numero, quindi può essere convertito nella rappresentazione frazionaria a precisione elevata.

Ai tipi complessi (inclusa la bitmap) sono associati nomi di elementi usati per delimitare il valore. Ciò semplifica l'analisi assicurando che le attività di analisi più complesse siano associate a tag di elemento univoci.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Un valore booleano è rappresentato come parola chiave che indica lo stato del flag. Vengono definite le parole chiave seguenti.



| Valore true | Valore per false |
|----------------|-----------------|
| true           | false           |
| sì            | no              |
| in             | spento             |
| t              | f               |
| 1              | 0               |



 

Un'implementazione può scrivere qualsiasi valore e deve riconoscere tutti i valori. Un'implementazione è libera di modificare i valori da una rappresentazione a un'altra.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="fraction"></a>frazione


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Tutti i valori numerici (ad esempio, i valori delle quantità senza dimensione) all'interno di questa proposta possono essere archiviati come numeri interi ridimensionandoli di 2 6 (65536). Un numero può essere specificato in questo formato, con il suffisso f o come numero decimale senza suffisso. Di conseguenza, gli elementi ipotetici seguenti rappresentano lo stesso valore.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Una quantità con il suffisso f deve essere un numero intero. I numeri frazionari non sono consentiti. L'intero risultante deve essere rappresentabile come numero con segno del complemento a 32 bit a 2; Pertanto, l'intervallo effettivo della rappresentazione è 32768 (in realtà, minore di 32768 e maggiore o uguale a -32768).

Un'implementazione conforme è necessaria per mantenere i valori espressi come valori f. I valori rappresentati come numeri decimali possono essere convertiti in un valore f e archiviati in questo modo. Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata. tuttavia, un valore letto da un documento esistente deve essere mantenuto con la precisione originale completa o deve essere convertito in un valore f.

Se l'implementazione non è in grado di eseguire questa operazione, deve avvisare l'utente che i dati potrebbero andare persi. È accettabile generare un avviso di questo tipo una volta quando vengono rilevati dati generati esternamente per la prima volta.

Quando un valore decimale viene convertito in formato f, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetico. Tuttavia, un numero intero deve essere convertito esattamente nel formato f. È consigliabile che le implementazioni esecutori esecutivano la conversione arrotondando in meno infinito e che la conversione sia sempre esatta.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="ordinate"></a>Ordinata


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Le unità del sistema di coordinate stabilite da coord sono di qualche tipo nominale, che viene definito ordinata. Si tratta di una misura di lunghezza, ma viene usata solo in relazione al rettangolo stabilito da coord. Qualsiasi valore di tipo ordinate verrà ridimensionato in base ai valori *w* e *h* del coord e al rapporto risultante usato per stabilire una misura reale nel dispositivo di output.

Un'implementazione conforme deve essere in grado di gestire valori ordinati fino a 30 bit più segno (ad esempio, un intero con segno a 31 bit, non un intero con segno a 32 bit). È tuttavia consigliabile che le implementazioni tentino di produrre coordinate per il percorso e elementi simili con circa 16 bit di precisione. In questo modo si riduce al minimo la possibilità di un underflow o di un overflow in un'implementazione non conforme.

I valori ordinati sono sempre integrali. Un separatore decimale non può essere visualizzato in un valore di tipo ordinate. Non è possibile aggiungere identificatori di unità a valori di tipo ordinate.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Una lunghezza è una misura reale o, talvolta, una misura in pixel del dispositivo. È consigliabile che le implementazioni evitino l'uso di pixel del dispositivo (px).

Tutti i qualificatori [di unità CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) standard sono consentiti per una lunghezza. È anche possibile usare il qualificatore emu. Questo qualificatore si riferisce a un'unità, ovvero l'EMU (English Metric Unit), che è un denominatore comune delle quantità di misura in uso diffuso nella grafica computerizzata. L'EMU <sup></sup> è pollici/914400, ad esempio sono presenti 914400 EMU per pollice. La tabella seguente elenca il numero di EMUL in un numero ridotto di unità comunemente incontrate.



| Numero di EMUL | Numero per pollice | Numero per millimetro | Descrizione             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0.01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | "point"                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Stampante ad alta risoluzione |



 

I numeri frazionari di EMUL non sono consentiti. Qualsiasi misura deve essere rappresentabile come numero integrale integrale con segno a 32 bit, limitando la grandezza di una misura a 2348 pollici, circa 59 metri o 65 metri. Poiché le misurazioni fanno sempre riferimento alle dimensioni di un rendering in un dispositivo di output nominalmente a schermo o a pagina, saranno sempre all'interno di questo intervallo.

Si noti, tuttavia, che la rappresentazione non è appropriata per le misurazioni reali e che in cui vengono registrate (ad esempio, per registrare le dimensioni reali di un percorso) è necessario usare un'altra rappresentazione.

Un'implementazione conforme è necessaria per mantenere valori che sono numeri esatti di EMUL. I valori rappresentati in qualsiasi altro modo possono essere convertiti in un valore EMU e archiviati in questo modo. Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata. tuttavia, un valore letto da un documento esistente deve essere mantenuto con la precisione originale completa o deve essere convertito in un valore EMU.

Se l'implementazione non è in grado di eseguire questa operazione, deve avvisare l'utente che i dati potrebbero andare persi. È accettabile generare un avviso di questo tipo una volta quando vengono rilevati dati generati esternamente per la prima volta.

In pratica, le lunghezze fisiche vengono usate per relativamente poche misurazioni in questa proposta. I dati che in genere sono più importanti sono i dati del percorso e sono codificati nel sistema di coordinate definito, per ogni forma, da coord.

### <a name="alternative-representations"></a>Rappresentazioni alternative

Le rappresentazioni di lunghezza standard del codice HTML sono definite da [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) Le unità relative, ad eccezione del pixel, non sono significative nel contesto in cui le lunghezze vengono usate nella proposta e non devono essere usate. Se il documento registra le dimensioni in pixel (destinazione) desiderate, definisce la traslazione dei pixel in EMU; In caso contrario, deve essere usato il valore predefinito di 90 dpi definito da [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units)

Ad eccezione di emu, qualsiasi valore può essere specificato come frazione decimale. Quando un valore decimale viene convertito in EMU, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetico. L'unico modo per un'applicazione di creazione per garantire un risultato specifico è specificarlo in emu.

Se non viene specificato alcun identificatore di unità in un valore di lunghezza, l'implementazione deve presupporre emu.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="measure"></a>Misura


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Una misura è una quantità che può essere una [lunghezza](#length) o una [frazione.](#fraction) Ciò è molto simile alle misurazioni della lunghezza HTML e CSS, che in molti casi possono essere misurazioni fisiche o percentuali di un'altra quantità. Se non viene specificato alcun identificatore di unità, il valore deve essere considerato una frazione decimale, pertanto questo comportamento viene ereditato dalla frazione e non dalla lunghezza.

A differenza della lunghezza, un valore in pixel ha un significato definito dal contesto, pertanto la conversione in emu è in genere inappropriata. Esistono tre possibili rappresentazioni fondamentali che l'implementazione deve mantenere( ad esempio, una rappresentazione non può essere convertita in un'altra senza perdita di informazioni).

1.  Un valore frazionario deve essere mantenuto nel formato [frazionario](#fraction) (un valore " f ").
2.  Una lunghezza fisica deve essere mantenuta in EMU.
3.  Un valore in pixel deve essere mantenuto come numero intero di pixel.

I numeri frazionari di pixel non sono consentiti.

### <a name="alternative-representations"></a>Rappresentazioni alternative

Sono consentite tutte le rappresentazioni alternative di [frazione](#fraction) [e](#length) lunghezza.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



La rappresentazione fondamentale di un angolo è un numero di gradi multiplo di 2 6 (65536) e archiviato come numero intero. Poiché lo spazio delle coordinate è invertito (l'asse y positivo è in basso), un angolo in senso orario è positivo. Un'implementazione conforme è necessaria per mantenere la precisione completa di tale valore.

Un'implementazione può usare qualsiasi intervallo per gli angoli e può normalizzare un angolo (ad esempio da -180 a +180 o da 0 a 360). Non è necessario che le implementazioni siano coerenti. Tuttavia, la rappresentazione integrale di un angolo non deve superare l'intervallo di un intero con segno a 32 bit.

Il suffisso fd viene usato per identificare questa rappresentazione di un angolo (grado frazionario). Si noti che si distingue dal suffisso f per una frazione senza dimensione, anche se è possibile usare un'aritmetica identica per supportarla. Il valore predefinito per un valore angolare è i gradi semplici, ad esempio un valore non ridimensionato. Può anche essere segnalato con il suffisso " " (simbolo di grado); Tuttavia, l'uso di questo valore dipende dalla presenza di una codifica del documento appropriata. Di conseguenza, anche il suffisso deg viene definito per indicare i gradi. Di seguito è riportato il set completo di possibili funzionalità.



| Suffisso       | Fattore di conversione | Commenti                               |
|--------------|-------------------|----------------------------------------|
| Fd           | 1                 | Rappresentazione interna ad alta precisione |
| none, deg,   | 65536             | Degrees                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Rappresentazioni alternative

La trasformazione del ridimensionamento presenta discontinuità in multipli dispari di 45 . È quindi estremamente importante che la conversione di qualsiasi quantità inesatta sia ben definita. Per questo motivo, l'aritmetica della conversione viene definita per arrotondare verso meno infinito.

Poiché ciò può essere difficile o impossibile da garantire in alcune implementazioni, l'uso di quanto segue è definito come una funzionalità di livello 3:

1.  Qualsiasi valore di grado frazionario.
2.  Qualsiasi valore in radianti

Pertanto, i valori completi fd e valori integrali non qualificati o i valori integrali qualificati deg o devono essere gestiti esattamente da un'implementazione di livello 0 conforme; gli altri valori non devono essere necessari. È consigliabile che qualsiasi implementazione gestirà esattamente la conversione da un valore di grado frazionario a un valore di grado ridimensionato (fd). Questa operazione può essere eseguita senza supporto a virgola mobile.

I requisiti più precisi per la conversione distinguono fd da f.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



I colori sono una parte essenziale della grafica moderna. La proposta usa i metodi stabiliti per specificare i colori fissi. Tuttavia, i colori nei diagrammi sono raramente semplici colori statici. spesso derivano da altri elementi del diagramma. Gran parte di queste informazioni è molto specifica dell'applicazione, quindi questa proposta fornisce due meccanismi molto semplici per specificare tale comportamento:

1.  Un colore può essere derivato da un altro colore nella stessa forma.
2.  Un numero ridotto di operazioni aritmetiche viene definito per la derivazione o la modifica di un colore.

Il meccanismo di forma del prototipo integra questo meccanismo, in modo da consentire la definizione dei prototipi da cui è possibile ereditare i colori.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Un valore di colore è un superset della [definizione di colore CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) Le estensioni consentono di determinare il valore del colore RGB da altri colori all'interno della forma o da una combinazione colori complessiva definita tramite CSS1.

Se il valore di un elemento è definito  come colore, il contenuto di un elemento definisce il valore del colore tramite un token di colore singolo modificato facoltativamente da un'operazione aritmetica sul colore RGB corrispondente.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="color-units"></a>Unità colore

Il set completo di token di colore deriva da diverse origini: HTML, CSS1 e questa proposta. Vengono definiti come segue usando la notazione [css1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notazione XPointer definita per il collegamento XML.

Nelle definizioni XPointer l'origine della posizione è l'elemento contenente il valore del colore e l'espressione fa riferimento all'intero set di elementi della forma come se tutti gli elementi del prototipo di base fossero stati uniti alla forma. Quando l'elemento corrispondente non esiste, al suo posto viene usato il valore predefinito per tale elemento.



| Color            | Definizione                                                                                                  | Level | Descrizione                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Vedere di seguito                                                                                                   | 0     | Nome del colore HTML, come elencato nella tabella seguente.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Rappresentazione dei colori CSS1/sRGB standard usando valori nell'intervallo 0..255 rappresentati usando 2 cifre esadecimali ciascuna.                                                     |
| \#Rgb            | \#rrggbb                                                                                                    | 1     | Formato CSS1 abbreviato con solo tre cifre esadecimali.                                                                                                                   |
| rgb(r,g,b)       | \#(r) (g) (b)                                                                                                 | 1     | Formato rgb CSS1; Gli elementi del valore rgb vengono convertiti come definito in [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units)                                      |
| fill             | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, color)<br/>                           | 1     | Colore di riempimento in primo piano della forma.                                                                                                                                   |
| fillBack         | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, back)<br/> child(1, color)<br/> | 1     | Colore di sfondo del riempimento della forma.                                                                                                                                   |
| line             | ancestor(1,shape)<br/> child(1, line)<br/> child(1, color)<br/>                           | 1     | Colore della linea di primo piano della forma.                                                                                                                                   |
| lineBack         | ancestor(1,shape)<br/> child(1, line)<br/> child(1,back) <br/> child(1, color)<br/> | 1     | Colore della linea di sfondo della forma.                                                                                                                                   |
| lineOrFill       | line, fill                                                                                                  | 1     | Valore della riga se non è impostato sul valore predefinito; in caso contrario, il valore di riempimento. In questo modo viene restituito in modo efficace il colore che si trova sul bordo della forma.                                           |
| fillThenLine     | riempimento, riga                                                                                                  | 1     | Valore di riempimento se non è predefinito, in caso contrario il valore della riga. In questo modo viene restituito il colore principale della forma (se la forma non è riempita, il risultato sarà il colore della linea).   |
| shadow           | predecessore(1,forma)<br/> child(1, shadow)<br/> child(1, color)<br/>                         | 2     | Colore dell'ombreggiatura (si tratta di una funzionalità di livello 2).                                                                                                                      |
| scheme           | Vedere di seguito                                                                                                   | 1     | Colore dello schema dello schema definito per il documento. vedere di seguito.                                                                                                       |
| scheme(*index*)  | Vedere di seguito                                                                                                   | 1     | Indice dei *colori dello schema,* a partire da 0; vedere di seguito.                                                                                                                         |
| this             | Implicita                                                                                                     | 2     | L'operazione (riempimento o disegno di un tracciato) è definita in altro modo (ad esempio, come bitmap) e il colore specifica una "modifica" ai colori così implicita. |
| palette(*index*) | Implicita                                                                                                     | 3     | Si comporta come questo, ad eccezione del fatto che viene identificata esattamente una voce in una tabella dei colori bitmap. Consentito solo se dichiarato in modo esplicito.                             |
| Nessuno             | \-                                                                                                          | 2     | Indica l'assenza di un colore. può essere usato per annullare un'operazione di disegno che usa il colore.                                                                          |
| sistema           | Vedere di seguito                                                                                                   | 3     | Colore definito dall'interfaccia utente di sistema.                                                                                                                             |



 

Questo colore consente a un valore di colore di specificare una modifica a un colore derivato in altro modo; in particolare, è possibile che venga specificata una singola operazione per tutti i colori di una bitmap. Il colore della tavolozza(*index*) identifica una voce specifica in una bitmap mappata alla tavolozza. L'uso di questo oggetto viene definito solo per la registrazione di una voce della tabella dei colori che deve essere considerata trasparente in una bitmap di questo tipo.

La definizione di un valore di colore non deve fare riferimento a se stessa, né direttamente né indirettamente. Se viene rilevata una definizione di questo tipo, è consigliabile, ma non obbligatorio, che l'implementazione tratti il valore non definito come nero.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="html-colors"></a>Colori HTML

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definisce i sedici nomi di colore seguenti:



Nomi dei colori e valori sRGB

![Esempio di colore nero.](images/black.gif)

Nero = " \# 000000"

![Esempio di colore verde.](images/green.gif)

Verde = " \# 008000"

![Esempio di colore argento.](images/silver.gif)

Silver = " \# C0C0C0"

![Esempio di colore calce.](images/lime.gif)

Lime = " \# 00FF00"

![Esempio di colore grigio.](images/gray.gif)

Grigio = " \# 808080"

![Esempio di colore dell'ulivo.](images/olive.gif)

Olive = " \# 808000"

![Esempio di colore bianco.](images/white.gif)

White = \# "FFFFFF"

![Esempio di colore ywllow.](images/yellow.gif)

Giallo = " \# FFFF00"

![Esempio di colore di maroon.](images/maroon.gif)

Maroon = " \# 800000"

![Esempio di colore della flotta.](images/navy.gif)

Navy = \# "000080"

![Esempio di colore rosso.](images/red.gif)

Red = " \# FF0000"

![Esempio di colore blu.](images/blue.gif)

Blu = " \# 0000FF"

![Esempio di colore viola.](images/purple.gif)

Viola = " \# 800080"

![Esempio di colore verde verde verde.](images/teal.gif)

Teal = " \# 008080"

![Esempio di colore fucsia.](images/fuchsia.gif)

Fucsia = \# "FF00FF"

![Esempio di colore acqua.](images/aqua.gif)

Aqua = " \# 00FFFF"



 

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="scheme-colors"></a>Colori dello schema

I colori dello schema a cui fa riferimento schema vengono definiti a livello di documento usando il metatag con un attributo name di "Schema colori tema".


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Questo tag consente di definire fino a otto colori dello schema. I colori non definiti devono essere il nero per impostazione predefinita. I colori della combinazione consentono di modificare la combinazione di colori usata per un documento completo modificando semplicemente il contenuto della combinazione colori del tema. Per garantire che la grafica importata da diverse applicazioni di creazione usi in modo coerente i colori dello schema, vengono definite le interpretazioni seguenti. "usage" è una breve descrizione dello scopo e la colonna "description" fornisce dettagli aggiuntivi.



| Indice | Nome              | Utilizzo                         | Descrizione                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | scheme.background | Sfondo                    | Colore usato per lo sfondo di un elemento grafico (e, spesso, per l'intera pagina).                                    |
| 1     | scheme.text       | Testo e righe                | Colore del testo associato a una forma e del colore della linea standard.                                                      |
| 2     | scheme.shadow     | Ombreggiature                       | Colore ombreggiatura standard: il colore usato in genere per le ombreggiature delle forme.                                                     |
| 3     | scheme.title      | Testo titolo                    | Colore da utilizzare per il testo dell'intestazione o del titolo.                                                                              |
| 4     | scheme.fill       | Riempie                         | Colore di riempimento standard: il colore usato in genere per riempire le forme.                                                          |
| 5     | scheme.accent     | Accento                        | Colore "evidenziazione" normale usato per evidenziare un elemento importante di un elemento grafico.                                             |
| 6     | scheme.hyperlink  | Carattere principale e collegamento ipertestuale          | Colore di evidenziazione usato per i collegamenti ipertestuali. Può essere usato per altri scopi in cui il colore indica un collegamento ad altre informazioni. |
| 7     | scheme.followed   | Collegamento ipertestuale con caratteri accentati e seguiti | Colore di evidenziazione per i collegamenti ipertestuali seguiti; appropriato anche per i collegamenti "indietro".                                         |



 

È possibile fare riferimento a un colore dello schema in base al nome o all'indice, pertanto scheme.fill e scheme(4) sono dello stesso colore.

I colori dello schema non partecipano alla combinazione predefinita se non viene specificato un colore. Un colore di riempimento non specificato deve sempre essere interpretato come bianco, indipendentemente dal colore dello schema 4. I colori "accentati" devono essere in contrasto con i colori di sfondo (0) e di riempimento (4) e i colori del testo e del testo del titolo devono avere la stessa proprietà. Una tecnica standard consiste nel colorare gli accenti e il testo standard senza colori (in genere nero o bianco).

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="system-colors"></a>Colori di sistema

Le applicazioni talvolta registrano i colori in base alle impostazioni del sistema operativo all'interno della grafica. In genere sono temporanei e non devono essere scritti; Le definizioni systemcolor esistono esclusivamente per supportare questa operazione. Un colore di sistema viene introdotto definendo un tag appropriato in un nuovo spazio dei nomi e inserendo le informazioni appropriate nel contenuto dell'elemento.

Questa proposta definisce un tag di questo tipo per codificare Windows colori dell'interfaccia utente definiti nel file di intestazione winuser.h.


```HTML
win.color
<!element win.color #pcdata>
```



Il contenuto dell'elemento è un singolo numero intero che contiene il valore della definizione COLOR \_ pertinente da winuser.h. Una tecnica simile può essere adottata per qualsiasi specifica di colore specifica del sistema o dell'applicazione. È consigliabile usare questa funzionalità solo per la compatibilità con le versioni precedenti.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="pure-colors"></a>Colori puri


```HTML
pure
<!elementpure empty>
```



Se l'elemento pure/ viene visualizzato in un valore di colore, è un suggerimento che il colore non deve essere approssimato &lt; &gt; da un motivo dithering. Si tratta di una funzionalità di livello 1 e un'implementazione conforme non deve rispettarla. La designazione è importante per la grafica visualizzata su dispositivi a media risoluzione, ad esempio schermi video, in cui piccole funzionalità (ad esempio linee) possono causare aliasing non valido con colori con dithering. Nei dispositivi come le stampanti, che in genere dithering di tutti i colori tranne i pochi colori completamente saturati, il dithering è in genere sufficientemente fine per evitare questo problema.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="color-adjustments"></a>Regolazioni del colore

Il colore di base può essere regolato da operazioni aritmetiche sul valore RGB. Queste operazioni vengono definite usando elementi aggiuntivi all'interno del valore del colore. Tali regolazioni sono utili solo se applicate ai colori derivati da altri elementi. È possibile specificare tale regolazione su un valore di colore fisso. Tuttavia, un'implementazione può ridurre questo valore al valore RGB corrispondente e archiviare tale valore anziché l'originale.

Tutte le funzionalità di regolazione del colore descritte in questa sezione sono funzionalità di livello 1.


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



Il parametro delle prime sei operazioni è un singolo valore numerico integrale compreso nell'intervallo da 0 a 255. La regolazione viene eseguita sul valore RGB a 3 x 8 bit come segue:

1.  Se viene specificato gray/, il valore RGB viene sostituito da yyy, dove y è il valore di luminance (y') calcolato dal valore &lt; &gt; sRGB in seguendo itU-r BT.709. Il calcolo è il seguente:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Se viene apportata una modifica a color.op, ogni componente viene regolato separatamente in base alla tabella seguente. c è il valore del componente e p è il valore color.parameter.

    | Operazione       | Formula                            |
    |-----------------|------------------------------------|
    | Darken          | c := cxp/255                       |
    | Alleggerire         | c := 255 - (255-c)xp/255           |
    | add             | c := c + p                         |
    | sottrarre        | c := c - p                         |
    | reversesubtract | c := p - c                         |
    | blackwhite      | se c < p thenc := 0elsec := 255 |

    

     

    In ogni caso, se il valore del componente calcolato, c, supera 255, viene usato 255 e, se è minore di 0, viene usato 0.

3.  Se si specifica INVERT128/, il valore 128 viene sottratto o aggiunto a ogni componente a seconda che il componente sia minore o meno &lt; &gt; di 128.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Se &lt; viene specificato invert/, &gt; ogni componente viene sostituito da 255 meno il valore del componente.
    ```HTML
    c := 255-c
    ```

    

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="font"></a>Carattere


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Un tipo di carattere viene identificato usando un attributo di stile come definito nella sezione [CSS1 5.2 (proprietà del tipo di carattere).](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) Il corpo dell'elemento del tipo di carattere non è attualmente definito, ma può essere usato in futuro per codificare le informazioni standard sul tipo di carattere. Le implementazioni iniziali di questa proposta devono mantenere ma non interpretare le informazioni.

È possibile che in futuro verrà aggiunto il supporto per le informazioni sui tipi di carattere out-of-line (tipi di carattere scaricabili o risorse dei tipi di carattere condivise). Questa operazione verrà eseguita da un elemento di collegamento XML all'interno del contenuto dell'elemento del tipo di carattere, garantendo la compatibilità con le versioni precedenti con le implementazioni iniziali.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="bitmap"></a>bitmap


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



L'elemento bitmap consente di includere un riferimento a una risorsa immagine out-of-line (in genere una bitmap) in un elemento grafico.

bitmap è una funzionalità di livello 1.

L'attributo di comportamento può essere usato per indicare come la bitmap deve essere gestita da un'applicazione di modifica. Il valore può essere uno o entrambi i token seguenti.



| token    | Descrizione                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Separato | Contrassegna la bitmap come entità separata, che non deve essere considerata parte integrante del documento. La bitmap non deve essere mantenuta con il documento. Se il documento viene copiato, la bitmap non deve essere copiata; Se il documento viene spostato, la bitmap non deve essere spostata con esso. |
| originale | L'attributo title identifica la posizione originale della bitmap come URL. In caso contrario, il significato del titolo non è specificato.                                                                                                                                                          |



 

Questi valori sono entrambi hint per il comportamento previsto. L'opzione separata fa riferimento al comportamento dei dati a cui fa riferimento href. Se vengono specificati sia l'uri separato che quello originale, l'applicazione deve ignorare l'URI href e rigenerare la bitmap dai dati originali. Se viene specificato solo originale, è previsto che l'applicazione usi l'URI href per trovare la bitmap, ma può offrire all'utente la possibilità di rigenerarla.

È possibile impostare l'URI href e l'attributo title sullo stesso valore (lessicale). Questa operazione è appropriata se la bitmap a cui si fa riferimento non viene "archiviata con" il documento. È previsto (anche se non obbligatorio) che href venga usato per la copia del documento della bitmap , che può essere eliminata se le forme di riferimento vengono eliminate, e tale titolo viene usato per indicare una copia condivisa. Pertanto, se entrambi contengono lo stesso valore, non esiste alcuna copia specifica del documento.

Le applicazioni possono ignorare l'hint se non rientra nel modello di archiviazione effettivo dei dati XML.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="picture-file-formats"></a>Formati di file di immagine

Nel contesto di questa proposta, i dati esterni sono invariabilmente una bitmap o un file usato per produrre una bitmap. Al livello di rendering 0 non è necessario il formato bitmap esterno. I percorsi possono essere riempiti solo con colori a tinta unita. Per eseguire il rendering del set completo di riempimenti del livello di rendering 1, è necessario che le bitmap siano supportate. Il livello di rendering 1 include (solo) i formati seguenti:

1.  JFIF, ovvero i dati in formato ISO/IEC 10918 incorporati all'interno di un file con l'intestazione JFIF (che può essere considerata come un marcatore APP0 specifico dopo SOI Maker) e includendo (solo) l'intervallo di formati JPEG supportati dal codice IJG v6.
2.  PNG, come definito dalla specifica PNG versione 1.0.

Il livello di rendering 2 include anche il supporto per gli elementi seguenti:

-   GIF, come definito dalla specifica GIF pubblicata da CompuServ nel 1987 (in genere denominata "GIF87a"). Anche GIF89a deve essere supportato a questo livello, soggetto alla restrizione che i dati non devono contenere blocchi di estensione che necessitano di interpretazione per visualizzare la bitmap diversa da estensioni di controllo graficocon il requisito di input dell'utente o un ritardo. In questo modo è possibile includere i commenti, ma non l'estensione di testo normale. Un'applicazione può inserire estensioni dell'applicazione (0x21, 0xFF), ma, usando la terminologia di questa proposta, queste devono contenere solo dati di modifica, non di rendering.

Qualsiasi altro formato di dati usato nell'elemento grafico impone almeno il livello di modifica 3 ed eventualmente il livello di rendering 3 (se i dati sono necessari per il rendering dell'elemento grafico). Un'applicazione è invitata a pubblicare i formati supportati. Ad esempio, Microsoft Office supporta i formati aggiuntivi seguenti in modo nativo e pertanto può scrivere dati di modifica in questo formato:

1.  WMF : Windows metafile (formato Win 3.1)
2.  EMF : Windows metafile "avanzato" (formato Win32)
3.  PICT : Mac OS file PICT QuickDraw (tutte le versioni ma senza record QuickTime o altre estensioni)
4.  BMP: Windows formato di file bitmap, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 e BITMAPV5

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="vector"></a>vettore


```HTML
v
<!element v "( #pcdata | p )*">
```



Un percorso grafico vettoriale viene codificato come pcdata. Il contenuto dell'elemento v è misto e contiene una descrizione del percorso vettore facoltativamente parametrizzata con elementi p.

[Tornare alla panoramica di VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

