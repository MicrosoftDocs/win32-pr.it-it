---
title: Tipi di la di base
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Eseguire la migrazione di pagine Web e applicazioni che si basano su la in SVG o su altri standard ampiamente supportati.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (la), tipi di base
- LA (Vector Markup Language), tipi di base
- grafica vettoriale, tipi la di base
- Vector Markup Language (la), tipi
- LA (Vector Markup Language), tipi
- grafica vettoriale, tipi la
- tipi di la di base
- tipo Boolean
- tipo di frazione
- tipo ordinata
- tipo lunghezza
- tipo di misura
- tipo di angolo
- tipo di colore
- tipo di carattere
- tipo di bitmap
- Tipo vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567100"
---
# <a name="basic-vml-types"></a>Tipi di la di base

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introduzione](#introduction)
-   [boolean](#boolean)
-   [frazione](#fraction)
-   [coordinare](#ordinate)
-   [length](#length)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [misura](#measure)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [angolo](#angle)
    -   [Rappresentazioni alternative](#alternative-representations)
-   [color](#color)
    -   [Unità colore](#color-units)
    -   [Colori HTML](#html-colors)
    -   [Colori dello schema](#scheme-colors)
    -   [Colori di sistema](#system-colors)
    -   [Colori puri](#pure-colors)
    -   [Regolazioni colori](#color-adjustments)
-   [carattere](#font)
-   [bitmap](#bitmap)
    -   [Formati di file immagine](#picture-file-formats)
-   [vettore](#vector)

## <a name="introduction"></a>Introduzione

Questa proposta usa un numero ridotto di tipi di base, elencati nella tabella seguente.



| Tipo                  | Elemento           | Rappresentazione fondamentale | Descrizione                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 bit                      | Valore booleano: true o false.                                                                      |
| [frazione](#fraction) |                   | numero 2 6                 | Un valore numerico, ridimensionato di 2 6 (65536) e archiviato come intero con segno.                               |
| [coordinare](#ordinate) |                   | segno più intero a 30 bit   | Parte di una coordinata (ad esempio, in un percorso), i valori definiti da Coord.                                |
| [length](#length)     |                   | [UEM](#length)             | Lunghezza fisica, ad esempio la larghezza di una riga o la dimensione di un tipo di carattere.                                |
| [misura](#measure)   |                   | EMU o numero 2 6          | Lunghezza fisica, incluso un numero di pixel del dispositivo o una frazione di un'altra quantità. |
| [angolo](#angle)       |                   | gradi 2 6                | Angolo; il positivo è in senso orario.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Elemento che consente la derivazione di un colore.                                                        |
| [carattere](#font)         | [carattere](#font)     | complex                    | Descrizione di un tipo di carattere.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Riferimento a un file di immagine esterno.                                                             |
| [vettore](#vector)     | [v](#vector)      | complex                    | Descrizione di un percorso vettoriale                                                                       |



 

La "rappresentazione fondamentale" è la rappresentazione di precisione più elevata che la proposta richiede un'implementazione conforme per la manutenzione; i dati andranno persi se l'implementazione non è in grado di rappresentare i dati alla precisione richiesta. I tipi di colore, tipo di carattere e vettore corrispondono agli elementi che a loro volta hanno una struttura, in un certo senso, non sono tipi di base; Tuttavia, è opportuno trattarle come tali in questa proposta.

A ogni tipo di base non complesso è associato un elemento con lo stesso nome. Questi nomi di elemento sono riservati e non possono essere usati per altri scopi all'interno di estensioni, anche se l'uso si trova all'interno di un elemento di estensione OnView = "Skip". Per questo motivo, è possibile che un'implementazione riscontri codice XML sconosciuto per fornire un'archiviazione interna efficiente del codice XML sconosciuto, a condizione che i valori siano racchiusi negli elementi "Type".


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



Nel primo esempio precedente, la stringa "1,578" deve essere archiviata come una sequenza di caratteri (l'implementazione non sa se si tratta di una stringa o di un numero). nel secondo esempio, l'elemento fraction indica che il contenuto è un numero, pertanto può essere convertito nella rappresentazione della frazione con precisione elevata.

Ai tipi complessi (incluse bitmap) sono associati nomi di elementi utilizzati per delimitare il valore. In questo modo si semplifica l'analisi assicurando che le attività di analisi più complesse siano associate ai tag degli elementi univoci.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Un valore booleano è rappresentato come una parola chiave che indica lo stato del flag. Sono definite le parole chiave seguenti.



| Valore per true | Valore per false |
|----------------|-----------------|
| true           | false           |
| sì            | no              |
| in             | spento             |
| u              | f               |
| 1              | 0               |



 

Un'implementazione può scrivere qualsiasi valore e deve riconoscere tutti i valori. Un'implementazione è gratuita per modificare i valori da una rappresentazione a un'altra.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="fraction"></a>frazione


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Tutti i valori numerici, ad esempio i valori di quantità non dimensionabili, all'interno di questa proposta possono essere archiviati come numeri interi scalando i valori di 2 6 (65536). Un numero può essere specificato in questo formato, con il suffisso f o come numero decimale senza suffisso. Pertanto, gli elementi ipotetici seguenti rappresentano lo stesso valore.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Una quantità con il suffisso f deve essere un numero intero; i numeri frazionari non sono consentiti. Il valore integer risultante deve essere rappresentabile come numero con segno di complemento a 32 bit 2. Pertanto, l'intervallo effettivo della rappresentazione è 32768 (in effetti, minore di 32768 e maggiore o uguale a-32768).

Un'implementazione conforme è necessaria per mantenere i valori espressi come valori f. I valori rappresentati come numeri decimali possono essere convertiti in un valore f e archiviati in questo modo. Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata; Tuttavia, un valore letto da un documento esistente deve essere mantenuto alla precisione originale completa oppure deve essere convertito in un valore f.

Se l'implementazione non è in grado di eseguire questa operazione, è necessario avvisare l'utente che i dati potrebbero andare persi. (È accettabile emettere tale avviso una volta quando vengono rilevati prima i dati generati dall'esterno).

Quando un valore decimale viene convertito in formato f, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetico; Tuttavia, un numero intero deve essere convertito esattamente nel formato f. È consigliabile che le implementazioni convertano con l'arrotondamento a meno infinito e che la conversione sia sempre esatta.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="ordinate"></a>coordinare


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Le unità del sistema di coordinate stabilito da Coord sono di tipo nominale, che viene definito ordinata. Si tratta di una misura di lunghezza, ma viene utilizzata solo in relazione al rettangolo stabilito da Coord. Qualsiasi valore di tipo ordinate verrà ridimensionato in base ai valori *w* e *h* del Coord e al rapporto risultante usato per stabilire una misura reale sul dispositivo di output.

Un'implementazione conforme deve essere in grado di gestire valori ordinati fino a 30 bit più segno, ovvero un intero con segno a 31 bit, non un intero con segno a 32 bit. Si consiglia, tuttavia, che le implementazioni tentino di produrre coordinate per il percorso e gli elementi simili con circa 16 bit di precisione. In questo modo è possibile ridurre al minimo la possibilità di underflow o overflow in un'implementazione non conforme.

i valori delle coordinate sono sempre integrali. Un separatore decimale non può essere visualizzato in un valore di tipo ordinata. Non è possibile aggiungere identificatori di unità a valori di tipo ordinate.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Una lunghezza è una misura reale o, a volte, una misura in pixel del dispositivo. È consigliabile evitare l'uso di Device pixel (px) per le implementazioni.

Tutti i qualificatori di unità [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) standard sono consentiti su lunghezza. Inoltre, è possibile utilizzare il qualificatore Emu. Questo qualificatore fa riferimento a un'unità, ovvero l'UEM (unità metrica inglese), che è un denominatore comune delle quantità di misura in uso generalizzato nella grafica del computer. Il EMU è in <sup>pollici</sup> /914400, ovvero sono presenti 914400 Emu per pollice. La tabella seguente elenca il numero di emù in un numero ridotto di unità rilevate di frequente.



| Numero di emù | Numero per pollice | Numero per millimetro | Descrizione             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0.01                  | HIMETRIC Win32          |
| 12700          | 72              |                       | punto                 |
| 635            | 1440            |                       | TWIP Win32              |
| 762            | 1200            |                       | Stampante ad alta risoluzione |



 

I numeri frazionari di emù non sono consentiti. Qualsiasi misurazione deve essere rappresentabile come numero integrale con segno a 32 bit di emù, che limita la grandezza di una misurazione a 2348 centimetri, circa 59 metri o 65 iarde. Poiché le misurazioni si riferiscono sempre alle dimensioni di un rendering in un dispositivo di output di dimensioni di schermo o di pagina nominalmente, saranno sempre comprese nell'intervallo.

Si noti, tuttavia, che la rappresentazione non è appropriata per le misurazioni reali e che dove vengono registrate, ad esempio per registrare le dimensioni reali di un percorso, è necessario usare un'altra rappresentazione.

Un'implementazione conforme è necessaria per mantenere i valori che sono numeri esatti di emù. I valori rappresentati in qualsiasi altro modo possono essere convertiti in un valore EMU e archiviati in questo modo. Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata; Tuttavia, un valore letto da un documento esistente deve essere mantenuto alla precisione originale completa oppure deve essere convertito in un valore EMU.

Se l'implementazione non è in grado di eseguire questa operazione, è necessario avvisare l'utente che i dati potrebbero andare persi. (È accettabile emettere tale avviso una volta quando vengono rilevati prima i dati generati dall'esterno).

In pratica, le lunghezze fisiche vengono usate per un numero relativamente ridotto di misure in questa proposta. I dati che sono in genere più importanti sono i dati del percorso e questo oggetto è codificato nel sistema di coordinate definito, in base alla forma, da Coord.

### <a name="alternative-representations"></a>Rappresentazioni alternative

Le rappresentazioni di lunghezza standard di HTML sono definite da [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) . Le unità relative, ad eccezione del pixel, non sono significative nel contesto in cui le lunghezze vengono utilizzate in questa proposta e non devono essere utilizzate. Se il documento registra le dimensioni del pixel previste (destinazione), definisce la conversione dei pixel in EMU; in caso contrario, deve essere usato il valore predefinito di 90 dpi definito da [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .

Fatta eccezione per EMU, qualsiasi valore può essere specificato come frazione decimale. Quando un valore decimale viene convertito in EMU, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetica. L'unico modo in cui un'applicazione di creazione può garantire un determinato risultato è specificarlo nell'UEM.

Se non viene specificato alcun identificatore di unità in un valore length, l'implementazione deve presupporre Emu.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="measure"></a>Misura


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Una misura è una quantità che può essere una [lunghezza](#length) o una [frazione](#fraction). Questo è molto simile alle misure di lunghezza HTML e CSS, che in molti casi possono essere misurazioni fisiche o percentuali di altre quantità. Se non viene specificato alcun identificatore di unità, il valore deve essere una frazione decimale (pertanto, questo comportamento viene ereditato dalla frazione, non dalla lunghezza).

A differenza della lunghezza, un valore in pixel ha un significato definito dal contesto, quindi la conversione in Emu non è normalmente appropriata. Esistono tre possibili rappresentazioni fondamentali che l'implementazione deve gestire (ovvero una rappresentazione non può essere convertita in un'altra senza perdita di informazioni).

1.  Un valore frazionario deve essere mantenuto nel formato della [frazione](#fraction) (valore "f").
2.  È necessario mantenere una lunghezza fisica nell'UEM.
3.  Il valore di un pixel deve essere mantenuto come un numero intero di pixel.

Non sono consentiti numeri frazionari di pixel.

### <a name="alternative-representations"></a>Rappresentazioni alternative

Sono consentite tutte le rappresentazioni alternative della [frazione](#fraction) e della [lunghezza](#length) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



La rappresentazione fondamentale di un angolo è un numero di gradi multipli di 2 6 (65536) e archiviati come Integer. Poiché lo spazio delle coordinate viene invertito (l'asse y positivo è inattivo), un angolo in senso orario è positivo. Un'implementazione conforme è necessaria per mantenere la precisione completa di tale valore.

Un'implementazione può usare qualsiasi intervallo per gli angoli ed è consentito normalizzare un angolo, ad esempio da-180 a + 180 o da 0 a 360. Non è necessario che le implementazioni siano coerenti. Tuttavia, la rappresentazione integrale di un angolo non deve superare l'intervallo di un intero con segno a 32 bit.

Il suffisso FD viene usato per identificare la rappresentazione di un angolo (grado frazionario). Si noti che questo si distingue dal suffisso f per una frazione con dimensione, sebbene sia possibile usarlo per supportare un'aritmetica identica. Il valore predefinito per un valore angolare è il grado semplice, ovvero un valore non scalato. Questa operazione può anche essere segnalata con il suffisso "" (simbolo del grado); Tuttavia, l'uso di questa operazione dipende dalla presenza di una codifica dei documenti adatta, di conseguenza il suffisso deg viene definito anche come valore medio. Il set completo di possibili sufficiente è il seguente.



| Suffisso       | Fattore di conversione | Commenti                               |
|--------------|-------------------|----------------------------------------|
| FD           | 1                 | Rappresentazione interna a precisione elevata |
| nessuno, deg,   | 65536             | Degrees                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Rappresentazioni alternative

La trasformazione ridimensionamento presenta discontinuità a multipli dispari di 45. È pertanto estremamente importante per la conversione di qualsiasi quantità inesatta per essere ben definita. Per questo motivo, l'aritmetica della conversione viene definita per essere arrotondata verso meno infinito.

Poiché questo potrebbe essere difficile o impossibile da garantire in alcune implementazioni, l'utilizzo dei seguenti elementi viene definito come una funzionalità di livello 3:

1.  Qualsiasi valore del grado frazionario.
2.  Qualsiasi valore radiante

Pertanto, i valori qualificati FD e i valori integrali non qualificati o i valori integrali qualificati deg o devono essere gestiti esattamente da un'implementazione di livello 0 conforme; non è necessario che altri valori. È vivamente consigliabile che qualsiasi implementazione gestisca esattamente la conversione da un valore Degree frazionario a un valore Degree (FD) scalato. Questa operazione può essere eseguita senza supporto a virgola mobile.

I requisiti più esatti per la conversione distinguono FD da f.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



I colori sono una parte essenziale della grafica moderna del computer. La proposta usa i metodi stabiliti per specificare i colori fissi. Tuttavia, i colori nei diagrammi sono raramente semplici colori statici; spesso derivano da altri elementi nel diagramma. Gran parte di queste informazioni è molto specifica dell'applicazione, pertanto questa proposta fornisce due meccanismi di base per specificare tale comportamento:

1.  Un colore può derivare da un altro colore nella stessa forma.
2.  Un numero ridotto di operazioni aritmetiche viene definito per la derivazione o la modifica di un colore.

Il meccanismo di forma del prototipo integra questo oggetto consentendo la definizione dei prototipi da cui è possibile ereditare i colori.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Un valore di colore è un superset della [definizione di colore CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . Le estensioni consentono di determinare il valore di colore RGB da altri colori all'interno della forma o da una combinazione di colori complessiva definita utilizzando CSS1.

Se il valore di un elemento è definito come un colore, il *contenuto* di un elemento definisce il valore del colore per mezzo di un singolo token di colore modificato facoltativamente da un'operazione aritmetica sul colore RGB corrispondente.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="color-units"></a>Unità colore

Il set completo di token di colore proviene da un'ampia gamma di origini: HTML, CSS1 e questa proposta. Sono definite come segue usando la notazione di [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notazione XPointer definita per il collegamento XML.

Nelle definizioni XPointer l'origine del percorso è l'elemento contenente il valore del colore e l'espressione fa riferimento all'intero set di elementi della forma come se tutti gli elementi del prototipo di base fossero stati Uniti con la forma. Quando l'elemento corrispondente non esiste, al suo posto viene utilizzato il valore predefinito di tale elemento.



| Colore            | Definizione                                                                                                  | Level | Descrizione                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Vedere di seguito                                                                                                   | 0     | Nome del colore HTML, come elencato nella tabella seguente.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Rappresentazione del colore CSS1/sRGB standard con valori compresi nell'intervallo 0.. 255 rappresentati con 2 cifre esadecimali ciascuna.                                                     |
| \#RGB            | \#RRGGBB                                                                                                    | 1     | Formato CSS1 abbreviato con solo tre cifre esadecimali.                                                                                                                   |
| RGB (r, g, b)       | \#r g b                                                                                                 | 1     | CSS1 formato RGB; gli elementi del valore RGB vengono convertiti come definito in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .                                      |
| fill             | predecessore (1, forma)<br/> figlio (1, riempimento)<br/> figlio (1, colore)<br/>                           | 1     | Colore di riempimento in primo piano della forma.                                                                                                                                   |
| fillBack         | predecessore (1, forma)<br/> figlio (1, riempimento)<br/> figlio (1, indietro)<br/> figlio (1, colore)<br/> | 1     | Colore di sfondo del riempimento della forma.                                                                                                                                   |
| line             | predecessore (1, forma)<br/> figlio (1, riga)<br/> figlio (1, colore)<br/>                           | 1     | Colore della linea di primo piano della forma.                                                                                                                                   |
| lineBack         | predecessore (1, forma)<br/> figlio (1, riga)<br/> figlio (1, indietro) <br/> figlio (1, colore)<br/> | 1     | Colore della linea di sfondo della forma.                                                                                                                                   |
| lineOrFill       | riga, riempimento                                                                                                  | 1     | Il valore della linea se non è impostato come predefinito; in caso contrario, il valore di riempimento. In questo modo viene restituito il colore che si trova al bordo della forma.                                           |
| fillThenLine     | riempimento, riga                                                                                                  | 1     | Il valore di riempimento se non è impostato come predefinito; in caso contrario, il valore della riga. In questo modo viene restituito il colore della forma principale (se la forma non è riempita, il risultato sarà il colore della linea).   |
| shadow           | predecessore (1, forma)<br/> figlio (1, ombreggiatura)<br/> figlio (1, colore)<br/>                         | 2     | Il colore dell'ombreggiatura (si tratta di una funzionalità di livello 2).                                                                                                                      |
| scheme           | Vedere di seguito                                                                                                   | 1     | Colore dello schema dello schema definito per il documento; vedere di seguito.                                                                                                       |
| Schema (*Indice*)  | Vedere di seguito                                                                                                   | 1     | *Indice* dei colori dello schema, a partire da 0; vedere di seguito.                                                                                                                         |
| this             | Implicita                                                                                                     | 2     | L'operazione (riempimento di un percorso o disegno) viene definita in un altro modo (ad esempio, come bitmap) e il colore specifica una "modifica" ai colori in modo implicito. |
| tavolozza (*Indice*) | Implicita                                                                                                     | 3     | Si comporta in modo analogo a, ad eccezione del fatto che viene identificata esattamente una voce in una tabella dei colori bitmap. Consentito solo se dichiarato in modo esplicito.                             |
| Nessuno             | \-                                                                                                          | 2     | Indica l'assenza di un colore. può essere usato per annullare un'operazione di disegno che usa il colore.                                                                          |
| sistema           | Vedere di seguito                                                                                                   | 3     | Colore definito dall'interfaccia utente del sistema.                                                                                                                             |



 

Questo colore consente a un valore di colore di specificare una modifica a un colore derivato in altro modo; in particolare, è possibile specificare una singola operazione per tutti i colori di una bitmap. Il colore della tavolozza (*Indice*) identifica una voce specifica in una bitmap mappata alla tavolozza. L'utilizzo di questa proprietà viene definito solo per la registrazione di una voce di tabella dei colori da considerare trasparente in una bitmap di questo tipo.

La definizione di un valore di colore non deve fare riferimento a se stessa, direttamente o indirettamente. Se viene rilevata una definizione di questo tipo, è consigliabile, ma non obbligatorio, che l'implementazione consideri come nero il valore non definito.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="html-colors"></a>Colori HTML

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definisce i seguenti sedici colori:



Nomi dei colori e valori sRGB

![Esempio di colore nero.](images/black.gif)

Nero = " \# 000000"

![Esempio di colore verde.](images/green.gif)

Verde = " \# 008000"

![Esempio di colore Silver.](images/silver.gif)

Silver = " \# C0C0C0"

![Esempio di colore lime.](images/lime.gif)

Lime = " \# 00FF00"

![Esempio di colore grigio.](images/gray.gif)

Grigio = " \# 808080"

![Esempio di colore oliva.](images/olive.gif)

Olive = " \# 808000"

![Esempio di colore bianco.](images/white.gif)

Bianco = " \# FFFFFF"

![Esempio di colore ywllow.](images/yellow.gif)

Yellow = " \# FFFF00"

![Esempio di colore marrone.](images/maroon.gif)

Maroon = " \# 800000"

![Esempio di colore navy.](images/navy.gif)

Navy = " \# 000080"

![Esempio di colore rosso.](images/red.gif)

Rosso = " \# FF0000"

![Esempio di colore blu.](images/blue.gif)

Blue = " \# 0000FF"

![Esempio di colore viola.](images/purple.gif)

Viola = " \# 800080"

![Esempio di colore verde acqua.](images/teal.gif)

Verde acqua = " \# 008080"

![Esempio di colore fucsia.](images/fuchsia.gif)

Fucsia = " \# FF00FF"

![Esempio di colore Aqua.](images/aqua.gif)

Aqua = " \# 00FFFF"



 

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="scheme-colors"></a>Colori dello schema

I colori dello schema a cui fa riferimento lo schema vengono definiti a livello di documento usando il tag meta con un attributo Name di "tema Color Scheme".


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Questo tag consente di definire un massimo di otto colori dello schema. I colori non definiti devono essere impostati su nero. I colori dello schema consentono di modificare la combinazione di colori utilizzata per un documento completo semplicemente modificando il contenuto della combinazione di colori del tema. Per garantire che la grafica importata da diverse applicazioni di creazione usi coerentemente i colori dello schema, vengono definite le interpretazioni seguenti. "Usage" è una breve descrizione dello scopo e la colonna "Description" fornisce dettagli aggiuntivi.



| Indice | Nome              | Utilizzo                         | Descrizione                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | Schema. sfondo | Sfondo                    | Colore utilizzato per lo sfondo di un elemento grafico (e, di frequente, per la pagina intera).                                    |
| 1     | Schema. Text       | Testo e righe                | Colore del testo associato a una forma e al colore della linea standard.                                                      |
| 2     | Schema. Shadow     | Ombreggiature                       | Colore ombreggiatura standard: colore usato in genere per le ombreggiature delle forme.                                                     |
| 3     | Schema. title      | Testo titolo                    | Il colore da utilizzare per l'intestazione o il testo del titolo.                                                                              |
| 4     | Schema. Fill       | Riempie                         | Colore di riempimento standard: colore usato in genere per riempire le forme.                                                          |
| 5     | Schema. accento     | Accento                        | Colore "Highlight" normale utilizzato per evidenziare un elemento importante di un elemento grafico.                                             |
| 6     | Schema. Hyperlink  | Accento e collegamento ipertestuale          | Colore di evidenziazione usato per i collegamenti ipertestuali. Può essere usato per altri scopi in cui il colore denota un collegamento ad altre informazioni. |
| 7     | Schema. seguito   | Accento e collegamento ipertestuale seguito | Colore di evidenziazione per i collegamenti ipertestuali seguiti; appropriato anche per i collegamenti "indietro".                                         |



 

È possibile fare riferimento a un colore dello schema in base al nome o all'indice, pertanto schema. Fill e Scheme (4) hanno lo stesso colore.

I colori dello schema non fanno parte dello schema predefinito se non si specifica un colore. Un colore di riempimento non specificato deve essere sempre interpretato come bianco, indipendentemente dal colore del colore 4 dello schema. I colori "accento" devono essere contrapposti sia allo sfondo (0) sia ai colori di riempimento (4), mentre i colori del testo e del testo del titolo devono avere la stessa proprietà. Una tecnica standard consiste nel fare in modo che gli accenti siano colorati e il testo standard non venga colorato, in genere nero o bianco.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="system-colors"></a>Colori di sistema

Le applicazioni talvolta registrano i colori in base alle impostazioni del sistema operativo all'interno della grafica. Normalmente questi sono temporanei e non devono essere scritti; le definizioni thesystemcolor sono disponibili solo per supportare questo. Un colore di sistema viene introdotto definendo un tag appropriato in un nuovo spazio dei nomi e inserendo le informazioni appropriate nel contenuto dell'elemento.

Questa proposta definisce un tag di questo tipo per codificare i colori dell'interfaccia utente di Windows definiti nel file di intestazione Winuser. h.


```HTML
win.color
<!element win.color #pcdata>
```



Il contenuto dell'elemento è un singolo integer che contiene il valore del colore pertinente \_ definito da winuser. h. È possibile adottare una tecnica simile per qualsiasi specifica di colore del sistema o dell'applicazione specifica. Si consiglia vivamente di utilizzare questa funzionalità solo per compatibilità con le versioni precedenti.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="pure-colors"></a>Colori puri


```HTML
pure
<!elementpure empty>
```



Se l'elemento <pure/> viene visualizzato in un valore di colore, è un suggerimento che il colore non dovrebbe essere approssimato da un modello di dithering. Si tratta di una funzionalità di livello 1, che non deve essere rispettata da un'implementazione conforme. La designazione è importante per i grafici visualizzati sui dispositivi di risoluzione media, ad esempio le visualizzazioni video, in cui le funzionalità di piccole dimensioni (ad esempio le linee) potrebbero causare un alias non valido con i colori dichiarati. Nei dispositivi, ad esempio stampanti, che in genere dipendono da tutti i colori, ad eccezione dei pochi colori completamente saturi, la dithering è in genere sufficiente per evitare questo problema.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="color-adjustments"></a>Regolazioni colori

Il colore di base può essere regolato da operazioni aritmetiche sul valore RGB. Queste operazioni vengono definite utilizzando elementi aggiuntivi all'interno del valore del colore. Tali modifiche sono utili solo quando vengono applicate a colori derivati da altri elementi. È possibile specificare tale regolazione su un valore di colore fisso. Tuttavia, un'implementazione di può ridurre questo valore al valore RGB corrispondente e archiviarlo anziché l'originale.

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



Il parametro delle prime sei operazioni è un singolo valore numerico integrale compreso tra 0 e 255. La regolazione viene eseguita sul valore RGB di 3x8bit come indicato di seguito:

1.  Se <gray/> si specifica, il valore RGB viene sostituito da yyy, dove y è il valore di luminanza (y) calcolato dal valore sRGB in seguito a ITU-r BT. 709. Il calcolo è il seguente:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Se viene fornita una modifica di colore. op, ogni componente viene regolato separatamente in base alla tabella seguente. c è il valore del componente e p è il valore Color. Parameter.

    | Operazione       | Formula                            |
    |-----------------|------------------------------------|
    | Darken          | c: = CXP/255                       |
    | schiarire         | c: = 255-(255-c) XP/255           |
    | add             | c: = c + p                         |
    | sottrarre        | c: = c-p                         |
    | reversesubtract | c: = p-c                         |
    | BlackWhite      | Se c < p thenc: = 0elsec: = 255 |

    

     

    In ogni caso, se il valore del componente calcolato, c, supera 255, viene utilizzato 255 e se è minore di 0, viene utilizzato 0.

3.  Se <INVERT128/> viene specificato, il valore 128 viene sottratto o aggiunto a ogni componente a seconda che il componente sia minore di 128 o meno.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Se <invert/> viene specificato, ogni componente viene sostituito da 255 meno il valore del componente.
    ```HTML
    c := 255-c
    ```

    

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="font"></a>carattere


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Un tipo di carattere viene identificato usando un attributo di stile come definito nella [sezione CSS1 5,2 (proprietà del tipo di carattere)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) . Il corpo dell'elemento del tipo di carattere è, al momento, non definito, ma può essere usato in futuro per codificare le informazioni standard sui tipi di carattere. Le implementazioni iniziali di questa proposta devono mantenere ma non interpretare le informazioni.

È possibile che il supporto verrà aggiunto in futuro per informazioni sui tipi di carattere out-of-line (tipi di carattere scaricabili o risorse dei tipi di carattere condivise). Questa operazione verrà eseguita da un elemento di collegamento XML all'interno del contenuto dell'elemento font, assicurando compatbility precedenti con implementazioni iniziali.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

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



L'elemento bitmap consente di includere in un grafico un riferimento a una risorsa immagine out-of-line (normalmente una bitmap).

bitmap è una funzionalità di livello 1.

L'attributo Behavior può essere usato per indicare il modo in cui la bitmap deve essere gestita da un'applicazione di modifica. Il valore può essere uno o entrambi i token seguenti.



| token    | Descrizione                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| separato | Contrassegna la bitmap come entità separata, che non deve essere considerata parte integrante del documento. La bitmap non deve essere mantenuta nel documento. Se il documento viene copiato, la bitmap non deve essere copiata; Se il documento viene spostato, la bitmap non deve essere spostata. |
| originale | L'attributo title identifica il percorso originale della bitmap come URL; in caso contrario, il significato di title non viene specificato.                                                                                                                                                          |



 

Questi valori sono entrambi hint per il comportamento previsto. L'opzione separato si riferisce al comportamento dei dati a cui viene fatto riferimento da href. Se vengono specificati sia un oggetto separato che un originale, l'applicazione deve ignorare l'URI href e rigenerare la bitmap dai dati originali. Se viene specificato solo originale, l'applicazione deve usare l'URI href per trovare la bitmap ma può dare all'utente la possibilità di rigenerarla.

È possibile rendere l'URI href e l'attributo title lo stesso valore (lessicale), che è appropriato se la bitmap a cui viene fatto riferimento non è "archiviata con" il documento. È previsto (sebbene non necessario) che href venga usato per la copia personalizzata del documento, che può essere eliminato se le forme di riferimento vengono eliminate e tale titolo viene usato per indicare una copia condivisa. Pertanto, se entrambi contengono lo stesso valore, non esiste alcuna copia specifica del documento.

Le applicazioni possono ignorare l'hint se non si adatta al modello di archiviazione effettivo dei dati XML.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

### <a name="picture-file-formats"></a>Formati di file immagine

Nel contesto di questa proposta, i dati esterni sono invariabilmente una bitmap o un file usato per produrre una bitmap. Al livello di rendering 0, non è necessario supportare alcun formato di bitmap esterno. i percorsi possono essere riempiti solo con colori a tinta unita. Per eseguire il rendering del set completo di riempimenti di livello 1 di rendering, è necessario che le bitmap siano supportate. Il livello di rendering 1 include (solo) i formati seguenti:

1.  JFIF, ad esempio i dati in formato ISO/IEC 10918 incorporati in un file con l'intestazione JFIF (che può essere considerata come un particolare marcatore APP0 dopo il creatore di SOI) e includendo (solo) la gamma di formati JPEG supportati dal codice IJG V6.
2.  PNG, come definito dalla specifica PNG versione 1,0.

Il livello di rendering 2 include anche il supporto per gli elementi seguenti:

-   GIF, come definito dalla specifica GIF pubblicata da CompuServ in 1987 (normalmente denominata "GIF87a"). GIF89a deve essere anche supportato a questo livello, soggetto alla restrizione che i dati non devono contenere alcun blocco di estensione che debba interpretare per visualizzare la bitmap diversa dal controllo grafico extensionswithouta requisito per l'input dell'utente o un ritardo. In questo modo è possibile includere i commenti, ma non l'estensione del testo normale. Un'applicazione può inserire le estensioni dell'applicazione (0x21, 0xFF) ma, usando la terminologia di questa proposta, deve contenere solo la modifica, non il rendering e i dati.

Tutti gli altri formati di dati usati nel grafico forzano tale grafico ad almeno modificare il livello 3 e possibilmente il livello di rendering 3 (se i dati sono necessari per eseguire il rendering dell'immagine). È consigliabile pubblicare i formati supportati da un'applicazione. Ad esempio, Microsoft Office supporta i formati aggiuntivi seguenti in modo nativo e può quindi scrivere i dati di modifica in questo formato:

1.  WMF--metafile Windows (formato Win 3,1)
2.  EMF--metafile "Enhanced" di Windows (formato Win32)
3.  PICT--Mac OS file PICT di rinvio (tutte le versioni ma senza record QuickTime o altre estensioni)
4.  BMP: formato di file bitmap di Windows, formati "OS/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 e BITMAPV5

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="vector"></a>vettore


```HTML
v
<!element v "( #pcdata | p )*">
```



Un percorso grafico vettoriale è codificato come PCDATA. Il contenuto dell'elemento v è misto, contenente una descrizione del percorso vettoriale facoltativamente parametrizzata con gli elementi p.

[Torna alla panoramica di la](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

