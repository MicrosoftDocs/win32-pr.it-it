---
description: Una larghezza ABC è un valore composito definito da una struttura ABC GDI. La struttura contiene i membri abcA, abcB e abcC, corrispondenti al &\# 0034; Un&\# 0034;, &\# 0034; B&\# 0034; e &\# 0034; C&\# 0034; larghezze di un glifo o di un'esecuzione.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glossario uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146974"
---
# <a name="uniscribe-glossary"></a>Glossario uniscribe

Una larghezza ABC è un valore composito definito da una struttura [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) GDI. La struttura contiene i membri **abcA**, **abcB** e **abcC**, corrispondenti alle larghezze "A", "B" e "C" di un [glifo](#glyph) o [di un'esecuzione.](#run)

La larghezza "A" è sottofase [(positiva;](#underhang) nota anche come "spaziatura interna") o [sporgenza](#overhang) (negativa) a sinistra dell'equivalente sullo schermo dell'input penna che rappresenta il glifo o la corsa. La larghezza "B" è la larghezza nera, la larghezza dall'input penna più a sinistra all'input penna più a destra. La larghezza "C" è sporgente a destra dell'input penna.

La figura seguente mostra una F minuscola corsiva con sporgenza a sinistra e a destra. In questo caso, le larghezze "A" e "C" sono entrambe negative. Vedere [underhang per](#underhang) un'illustrazione delle larghezze positive di "A" e "C".

![Figura che mostra una F minuscola corsiva con sporgenza a sinistra e a destra.](images/abcwidth.gif)

Quando due o più glifi vengono visualizzati come unità, in genere solo il glifo più a sinistra contribuisce alla larghezza "A" dell'esecuzione e solo il glifo più a destra contribuisce alla larghezza "C" della corsa. Tuttavia, questa non è una regola rigorosa. Ad esempio, se il primo glifo in un'esecuzione è una lettera stretta e il secondo glifo è un segno diacritico ampio e vengono gestiti come glifi separati, il segno diacritico potrebbe effettivamente estendersi oltre la lettera.

## <a name="abc-width"></a>Larghezza ABC

Una larghezza ABC è un valore composito definito da una struttura [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) GDI. La struttura contiene i membri **abcA**, **abcB** e **abcC**, corrispondenti alle larghezze "A", "B" e "C" di un [glifo](#glyph) o [di un'esecuzione.](#run)

La larghezza "A" è sottofase [(positiva;](#underhang) nota anche come "spaziatura interna") o [sporgenza](#overhang) (negativa) a sinistra dell'equivalente sullo schermo dell'input penna che rappresenta il glifo o la corsa. La larghezza "B" è la larghezza nera, la larghezza dall'input penna più a sinistra all'input penna più a destra. La larghezza "C" è sporgente a destra dell'input penna.

La figura seguente mostra una F minuscola corsiva con sporgenza a sinistra e a destra. In questo caso, le larghezze "A" e "C" sono entrambe negative. Vedere [underhang per](#underhang) un'illustrazione delle larghezze positive di "A" e "C".

![Figura che mostra una F minuscola corsiva con sporgenza a sinistra e a destra.](images/abcwidth.gif)

Quando due o più glifi vengono visualizzati come unità, in genere solo il glifo più a sinistra contribuisce alla larghezza "A" dell'esecuzione e solo il glifo più a destra contribuisce alla larghezza "C" della corsa. Tuttavia, questa non è una regola rigorosa. Ad esempio, se il primo glifo in un'esecuzione è una lettera stretta e il secondo glifo è un segno diacritico ampio e vengono gestiti come glifi separati, il segno diacritico potrebbe effettivamente estendersi oltre la lettera.

## <a name="advance-width"></a>larghezza di avanzamento

La larghezza di [](#glyph) avanzamento di un glifo è lo spostamento nella direzione di scrittura dal punto iniziale per il rendering del glifo al punto iniziale per il rendering del glifo successivo.

## <a name="bidirectional-stack"></a>stack bidirezionale

Lo stack bidirezionale è un intero a 5 bit che tiene traccia dei livelli di annidamento tra testo da sinistra a destra e da destra a sinistra. Inizia sempre da zero per da sinistra a destra. Tutti i valori pari rappresentano quindi il testo da sinistra a destra e tutti i valori dispari rappresentano il testo da destra a sinistra. Lo stack bidirezionale è rappresentato nel membro **uBidiLevel** di una [**struttura SCRIPT \_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state)

## <a name="bidirectional-text"></a>testo bidirezionale

Il testo bidirezionale contiene sia parti da sinistra a destra che da destra a sinistra, ma il termine viene talvolta applicato in modo libero al testo puro da destra a sinistra. Tutto il testo da destra a sinistra richiede l'uso [](#embedding-level) dello [stack bidirezionale](#bidirectional-stack), perché il livello di incorporamento predefinito pari a zero implica il testo da sinistra a destra.

## <a name="cell-width"></a>larghezza della cella

Un'applicazione può giustificare il testo per adattarlo a una riga regolando la larghezza della cella per determinati glifi. Per il testo ingiustificato, la larghezza della cella per un glifo è uguale alla larghezza [di avanzamento.](#advance-width)

## <a name="cluster"></a>cluster

Un cluster è l'unità linguistica più piccola che può essere modellata. In lingue come l'arabo e molte delle lingue indic, i glifi usati per rappresentare ogni carattere (punto di codice Unicode) dipendono fortemente dai punti di codice circostanti, che costituiscono il cluster. In questi linguaggi, le applicazioni possono convertire i punti di codice in glifi appropriati solo esaminando il cluster. In alcuni script, ad esempio Devanagari, l'ordine dei glifi all'interno di un cluster può differire dall'ordine dei punti di codice Unicode corrispondenti. Per altre informazioni, vedere [Windows Glyph Processing](/typography/develop/processing-part1) nel sito di tipografia Microsoft.

## <a name="complex-script"></a>script complesso

Uno script complesso è [uno script](#complex-script) con una delle proprietà seguenti:

-   Consente il rendering bidirezionale.
-   Ha una forma contestuale.
-   Contiene caratteri di combinazione.
-   Dispone di regole specifiche per l'interruzione delle parole e la giustificazione.
-   Filtra le combinazioni di caratteri non validi.
-   Non è supportato nei tipi di carattere di base Windows e pertanto potrebbe richiedere il [fallback del tipo di carattere](#font-fallback).

In alcuni script complessi, l'ordine dei glifi potrebbe essere piuttosto diverso dall'ordine dei caratteri Unicode sottostanti che rappresentano. Per [altre informazioni, vedere Informazioni](about-complex-scripts.md) sugli script complessi.

> [!Note]  
> Nel contesto della tipografia, talvolta è preferibile gestire lo script latino usato per scrivere l'inglese come script complesso. Ad esempio, la funzionalità Alternative stilische descritta nella documentazione di [**OPENTYPE \_ FEATURE \_ RECORD**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)o le legature, ad esempio "fi", in cui un singolo glifo rappresenta due o più caratteri consecutivi.

 

## <a name="embedding-level"></a>livello di incorporamento

Nel [testo bidirezionale](#bidirectional-text)il livello di incorporamento è l'indice dello [stack bidirezionale.](#bidirectional-stack)

## <a name="font-fallback"></a>fallback dei tipi di carattere

Il fallback del tipo di carattere è la selezione automatica di un tipo di carattere diverso da quello selezionato dall'utente in un'applicazione. In Uniscribe il fallback del tipo di carattere viene applicato dalla funzione [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando tutto o parte del testo si trova in uno script che il tipo di carattere selezionato dall'utente non supporta.

## <a name="glyph"></a>glifo

Un glifo è una singola unità di visualizzazione in un tipo di carattere. Per OpenType, questa unità è definita da una struttura. Per altri tipi di carattere, può essere definito da una bitmap, un set di comandi grafici e simili. Un glifo non corrisponde necessariamente a un singolo carattere. Ad esempio, la legatura "fi" ("fi") rappresenta i due caratteri "f" e "i". La "o" minuscola in lingua taiwanese con circumflex e tilde ("ỗ") è in genere composta da più glifi.

## <a name="item"></a>item

Un elemento ha un singolo [script e](#complex-script) direzione. La [**funzione ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) o [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) può analizzare un paragrafo in elementi. Un elemento non è necessariamente [un'esecuzione di](#run). Può contenere caratteri di più stili. Le informazioni sull'elemento e sull'esecuzione devono essere combinate per determinare [gli intervalli](#range).

## <a name="lrm"></a>Lrm

LRM indica il CONTRASSEGNO DA SINISTRA A DESTRA (punto di codice Unicode U+200E). Questo contrassegno specifica che il rendering dei caratteri che lo segue in ordine logico deve essere eseguito da sinistra a destra.

## <a name="ltr"></a>Ltr

LTR indica da sinistra a destra.

## <a name="range"></a>range

Un intervallo è un caso speciale di [un'esecuzione](#run). Si trova interamente all'interno di un [elemento](#item). Pertanto, se un elemento viene suddiviso in esecuzioni, ognuna di queste esecuzioni è un intervallo.

## <a name="rlm"></a>Rlm

RLM indica il CONTRASSEGNO DA DESTRA A SINISTRA (punto di codice Unicode U+200F). Questo segno indica che il rendering dei caratteri che lo segue in ordine logico deve essere eseguito da destra a sinistra.

## <a name="rtl"></a>RTL

RTL indica da destra a sinistra.

## <a name="run"></a>Run

Un'esecuzione è un passaggio di testo per il rendering di Uniscribe. Deve avere un solo stile, ad esempio tipo di carattere, dimensioni e colore, ma può essere disegnato da un'ampia gamma di [script.](#complex-script) Un'esecuzione può contenere sia contenuto da sinistra a destra che da destra a sinistra.

## <a name="nads"></a>Palle

NADS indica NATIONAL DIGIT SHAPES (punto di codice Unicode U+206E. Il termine specifica che il rendering delle cifre europa (da U+0030 a U+0039) deve essere eseguito come cifre nazionali. Per [altre informazioni sulle](digit-shapes.md) cifre nazionali, vedere Forme delle cifre.

## <a name="nods"></a>Annuisce

NODS indica NOMINAL DIGIT SHAPES (punto di codice Unicode U+206F). Il termine specifica che il rendering delle cifre europa (da U+0030 a U+0039) deve essere eseguito normalmente, non come cifre nazionali.

## <a name="overhang"></a>Sporgenza

La sporgenza è la parte dell'input penna di un glifo che si estende oltre la larghezza [di](#advance-width) avanzamento del glifo. La maggior parte dei glifi (ad esempio "H") non ha sporgenza, perché su entrambi i lati è presente un piccolo spazio vuoto per separarli dai glifi adiacenti. Un esempio di un glifo con sporgenza è il corsivo "f" usato in questo argomento per illustrare [la larghezza ABC.](#abc-width) Sia la parte superiore che la parte inferiore del corsivo "f" sovrastono i glifi adiacenti. La sporgenza corrisponde a una larghezza negativa "A" o "C".

## <a name="padding"></a>riempimento

Vedere [underhang](#underhang).

## <a name="script"></a>script

Uno script è un sistema di linguaggio scritto, ad esempio alfabeto latino, alfabeto arabo, script cinese. Un singolo script può essere applicato a uno o più linguaggi umani. Lo script non ha alcuna relazione particolare con un tipo di carattere. Ad esempio, il rendering dello script latino può essere eseguito in modo uniforme dal tipo di carattere Times New Roman o Arial.

## <a name="underhang"></a>underhang

Il sottofase è una larghezza di spazi vuoti a sinistra o a destra della parte a tinta unita di un glifo. Underhang corrisponde a una larghezza positiva "A" o "C", come descritto per [ABC width](#abc-width). Underhang è talvolta noto come "spaziatura interna". La figura seguente mostra la parte inferiore della lettera minuscola n.

![figura che mostra la parte inferiore della lettera minuscola n.](images/underhang.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
