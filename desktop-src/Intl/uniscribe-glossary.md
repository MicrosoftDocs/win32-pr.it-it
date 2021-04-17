---
description: Una larghezza ABC è un valore composto definito da una struttura GDI ABC. La struttura contiene i membri abcA, abcB e abcC, corrispondenti all'&\# 0034; A&\# 0034;, &\# 0034; B&\# 0034; e &\# 0034; C&\# 0034; larghezze di un glifo o di un'esecuzione.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glossario Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e154e65c103ce6e4287ac8aa2e76e0be4206f9fd
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339587"
---
# <a name="uniscribe-glossary"></a>Glossario Uniscribe

Una larghezza ABC è un valore composto definito da una struttura GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) . La struttura contiene i membri **abcA**, **abcb** e **abcC**, corrispondenti alle larghezze "a", "B" e "C" di un [glifo](#glyph) o di un' [esecuzione](#run).

La larghezza "A" è [sottoblocco](#underhang) (positiva, nota anche come "riempimento") o [sporgenza](#overhang) (negativa) a sinistra dell'equivalente sullo schermo dell'input penna che rappresenta il glifo o l'esecuzione. La larghezza "B" è la larghezza nera, ovvero la larghezza dall'input più a sinistra all'input penna più a destra. La larghezza "C" è sporgente a destra dell'input penna.

Nell'illustrazione seguente viene mostrata una F minuscola in corsivo con sporgenza sia a sinistra che a destra. Ovvero le larghezze "A" e "C" sono entrambe negative. Per un'illustrazione di larghezze positive "A" e "C", vedere [sottoblocco](#underhang) .

![illustrazione che mostra una F minuscola in corsivo con sporgenza sia a sinistra che a destra.](images/abcwidth.gif)

Quando due o più glifi vengono visualizzati come un'unità, in genere solo il glifo più a sinistra contribuisce alla larghezza "A" dell'esecuzione e solo il glifo più a destra contribuisce alla larghezza "C" dell'esecuzione. Tuttavia, non si tratta di una regola restrittiva. Se, ad esempio, il primo glifo in un'esecuzione è una lettera limitata e il secondo glifo è un segno diacritici ampio, che viene gestito come glifo separato, il segno diacritici può estendersi oltre la lettera.

## <a name="abc-width"></a>Larghezza ABC

Una larghezza ABC è un valore composto definito da una struttura GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) . La struttura contiene i membri **abcA**, **abcb** e **abcC**, corrispondenti alle larghezze "a", "B" e "C" di un [glifo](#glyph) o di un' [esecuzione](#run).

La larghezza "A" è [sottoblocco](#underhang) (positiva, nota anche come "riempimento") o [sporgenza](#overhang) (negativa) a sinistra dell'equivalente sullo schermo dell'input penna che rappresenta il glifo o l'esecuzione. La larghezza "B" è la larghezza nera, ovvero la larghezza dall'input più a sinistra all'input penna più a destra. La larghezza "C" è sporgente a destra dell'input penna.

Nell'illustrazione seguente viene mostrata una F minuscola in corsivo con sporgenza sia a sinistra che a destra. Ovvero le larghezze "A" e "C" sono entrambe negative. Per un'illustrazione di larghezze positive "A" e "C", vedere [sottoblocco](#underhang) .

![illustrazione che mostra una F minuscola in corsivo con sporgenza sia a sinistra che a destra.](images/abcwidth.gif)

Quando due o più glifi vengono visualizzati come un'unità, in genere solo il glifo più a sinistra contribuisce alla larghezza "A" dell'esecuzione e solo il glifo più a destra contribuisce alla larghezza "C" dell'esecuzione. Tuttavia, non si tratta di una regola restrittiva. Se, ad esempio, il primo glifo in un'esecuzione è una lettera limitata e il secondo glifo è un segno diacritici ampio, che viene gestito come glifo separato, il segno diacritici può estendersi oltre la lettera.

## <a name="advance-width"></a>larghezza avanzata

La larghezza di avanzamento di un [glifo](#glyph) è il movimento nella direzione della scrittura dal punto di partenza per il rendering di tale glifo sul punto iniziale per il rendering del glifo successivo.

## <a name="bidirectional-stack"></a>stack bidirezionale

Lo stack bidirezionale è un intero a 5 bit che tiene traccia dei livelli di annidamento tra il testo da sinistra a destra e quello da destra a sinistra. Viene sempre avviato da zero per da sinistra a destra. Tutti i valori pari, quindi, rappresentano il testo da sinistra a destra e tutti i valori dispari rappresentano il testo da destra a sinistra. Lo stack bidirezionale è rappresentato nel membro **uBidiLevel** di una struttura [**\_ dello stato dello script**](/windows/win32/api/usp10/ns-usp10-script_state) .

## <a name="bidirectional-text"></a>testo bidirezionale

Il testo bidirezionale contiene parti da sinistra a destra e da destra a sinistra, ma il termine viene anche applicato in modo debole al testo da destra a sinistra. Tutto il testo da destra a sinistra richiede l'uso dello [stack bidirezionale](#bidirectional-stack), perché il [livello di incorporamento](#embedding-level) predefinito pari a zero implica testo da sinistra a destra.

## <a name="cell-width"></a>Larghezza cella

Un'applicazione può giustificare il testo in modo da adattarla a una riga regolando la larghezza della cella per determinati glifi. Per il testo non giustificato, la larghezza della cella per un glifo corrisponde alla [larghezza di avanzamento](#advance-width).

## <a name="cluster"></a>cluster

Un cluster è la più piccola unità linguistica che può essere modellata. In linguaggi come l'arabo e molte lingue indiane, i glifi usati per rappresentare ogni carattere (punto di codice Unicode) dipendono fortemente dai punti di codice circostanti, che costituiscono il cluster. In questi linguaggi, le applicazioni possono tradurre i punti di codice in glifi appropriati solo esaminando il cluster. In alcuni script, ad esempio devangat, l'ordine dei glifi in un cluster può differire dall'ordine dei punti di codice Unicode corrispondenti. Per ulteriori informazioni, vedere [elaborazione del glifo Windows](/typography/develop/processing-part1) nel sito Microsoft Typography.

## <a name="complex-script"></a>script complesso

Uno script complesso è uno [script](#complex-script) con le proprietà seguenti:

-   Consente il rendering bidirezionale.
-   Con shaping contestuale.
-   Contiene caratteri combinati.
-   Dispone di regole specializzate di suddivisione delle parole e di giustificazione.
-   Filtra le combinazioni di caratteri non valide.
-   Non è supportato nei tipi di carattere principali di Windows e pertanto potrebbe richiedere il [fallback del tipo di carattere](#font-fallback).

In alcuni alfabeti complessi, l'ordine dei glifi potrebbe essere piuttosto diverso dall'ordine dei caratteri Unicode sottostanti che rappresentano. Per altri dettagli, vedere [informazioni sugli script complessi](about-complex-scripts.md) .

> [!Note]  
> Nel contesto della tipografia è talvolta auspicabile gestire lo script Latino usato per scrivere l'inglese come script complesso. Gli esempi includono la caratteristica alternativa stilistica descritta nella documentazione del [**record di \_ funzionalità \_ OPENTYPE**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record), o legature, ad esempio "Fi", dove un singolo glifo rappresenta due o più caratteri consecutivi.

 

## <a name="embedding-level"></a>livello di incorporamento

Nel [testo bidirezionale](#bidirectional-text), il livello di incorporamento è l'indice dello [stack bidirezionale](#bidirectional-stack).

## <a name="font-fallback"></a>fallback del tipo di carattere

Il fallback del tipo di carattere è la selezione automatica di un tipo di carattere diverso dal tipo di carattere selezionato dall'utente in un'applicazione. In Uniscribe il fallback del tipo di carattere viene applicato dalla funzione [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando tutto o parte del testo è in uno script che non è supportato dal tipo di carattere selezionato dall'utente.

## <a name="glyph"></a>glifo

Un glifo è una singola unità di visualizzazione in un tipo di carattere. Per OpenType, questa unità è definita da un contorno. Per altri tipi di tipi di carattere, può essere definita da una bitmap, da un set di comandi grafici e da like. Un glifo non corrisponde necessariamente a un singolo carattere. Ad esempio, la legatura "Fi" ("Fi") rappresenta i due caratteri "f" e "i". Il carattere "o" minuscolo vietnamita con circonflesso e tilde ("ỗ") è in genere composto da più glifi.

## <a name="item"></a>item

Un elemento ha un solo [script](#complex-script) e una direzione. La funzione [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) o [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) può analizzare un paragrafo in elementi. Un elemento non è necessariamente un' [esecuzione](#run). Può contenere caratteri di più stili. Per determinare gli [intervalli](#range)è necessario combinare le informazioni sull'elemento e sull'esecuzione.

## <a name="lrm"></a>LRM

LRM indica il contrassegno da sinistra a destra (punto di codice Unicode U + 200E). Questo contrassegno specifica che i caratteri che lo seguono nell'ordine logico devono essere sottoposti a rendering da sinistra a destra.

## <a name="ltr"></a>LTR

LTR indica da sinistra a destra.

## <a name="range"></a>range

Un intervallo è un caso speciale di un' [esecuzione](#run). Rientra interamente in un [elemento](#item). Pertanto, se un elemento viene suddiviso in esecuzioni, ognuna di queste esecuzioni è un intervallo.

## <a name="rlm"></a>RLM

RLM indica il segno da destra a sinistra (punto di codice Unicode U + 200F). Questo contrassegno indica che i caratteri che lo seguono nell'ordine logico devono essere sottoposti a rendering da destra a sinistra.

## <a name="rtl"></a>RTL

RTL indica da destra a sinistra.

## <a name="run"></a>Run

Un'esecuzione è un passaggio del testo per Uniscribe per il rendering. Deve avere un unico stile, ovvero, il tipo di carattere, la dimensione e il colore, ma può essere disegnato da un'ampia gamma di [script](#complex-script). Un'esecuzione può includere il contenuto da sinistra a destra e da destra a sinistra.

## <a name="nads"></a>PALLE

PALLE indica le forme di cifre nazionali (punto di codice Unicode U + 206E. Il termine specifica che è necessario eseguire il rendering delle cifre europee (U + 0030-U + 0039) come cifre nazionali. Per ulteriori informazioni sulle cifre nazionali, vedere [forme digit](digit-shapes.md) .

## <a name="nods"></a>NODI

Il numero di nodi indica le forme letterali (punto di codice Unicode U + 206F). Il termine specifica che le cifre europee (U + 0030-U + 0039) devono essere visualizzate normalmente e non come cifre nazionali.

## <a name="overhang"></a>sporgere sul

La sporgenza è la parte dell'input penna di un glifo che si estende oltre la [larghezza avanzata](#advance-width) del glifo. La maggior parte dei glifi (ad esempio "H") non hanno sporgenza, in quanto è presente uno spazio vuoto su entrambi i lati per separarli da glifi adiacenti. Un esempio di glifo con sporgenza è il corsivo "f" usato in questo argomento per illustrare la [larghezza di ABC](#abc-width). Sia la parte superiore che la parte inferiore del corsivo "f" sporgono i glifi adiacenti. La sporgenza corrisponde a una larghezza "A" o "C" negativa.

## <a name="padding"></a>riempimento

Vedere [sottoblocco](#underhang).

## <a name="script"></a>script

Uno script è un sistema di linguaggio scritto, ad esempio alfabeto latino, alfabeto arabo, script in cinese. Un singolo script può essere applicato a una o più lingue umane. Lo script non ha alcuna relazione particolare con un tipo di carattere. Ad esempio, è possibile eseguire il rendering dello script latino in modo altrettanto corretto per il tipo di carattere Times New Roman o Arial.

## <a name="underhang"></a>sottoblocco

Il sottoblocco è una larghezza dello spazio vuoto a sinistra o a destra della parte solida di un glifo. Il sottoblocco corrisponde a una larghezza positiva "A" o "C", come descritto per la [larghezza ABC](#abc-width). Il sottoblocco è talvolta noto come "riempimento". Nella figura seguente viene illustrato il sottoblocco per la lettera minuscola n.

![illustrazione che mostra il sottoblocco per la lettera minuscola n.](images/underhang.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
