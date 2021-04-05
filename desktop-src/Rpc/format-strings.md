---
title: Stringhe di formato
description: Una stringa di formato è un token interpretato che il motore di rapporto di recapito riconosce. Le stringhe di formato sono spesso denominate MOPs; Questa documentazione usa il termine formato stringa in tutto.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711428"
---
# <a name="format-strings"></a>Stringhe di formato

Una stringa di formato è un token interpretato che il motore di rapporto di recapito riconosce. Le stringhe di formato sono spesso denominate MOPs; Questa documentazione usa il termine formato stringa in tutto.

Per maggiore precisione, un carattere di formato è un singolo token interpretabile (Atomic). Ogni carattere di formato è di dimensioni pari a un byte. Una stringa di formato è una sequenza di caratteri di formato o caratteri di formato e dati numerici. Il termine descrittore viene utilizzato anche per la denominazione di sequenze comuni; una stringa di formato di parametro o un descrittore di parametro è ad esempio una stringa di formato utilizzata per descrivere un parametro di una routine.

I caratteri di formato presentano nomi simbolici suggestivi, ad esempio FC \_ Long o FC \_ struct. Tutti i caratteri stringa di formato usati da MIDL e dal motore NDR sono definiti nel file Ndrtypes. h.

## <a name="format-string-tables"></a>Formattare le tabelle di stringhe

Due tabelle di stringhe di formato primarie vengono usate dal motore: la tabella delle stringhe di formato della procedura, **\_ \_ MIDL \_ ProcFormatString**, che mantiene i descrittori di routine e la tabella di stringhe di formato del tipo, **\_ \_ MIDL \_ TypeFormatString**, che mantiene i descrittori del tipo di dati. Il compilatore genera entrambi i file stub principali ( \* \_ c. c, \* \_ s. c, \* \_ p. c). La tabella delle stringhe di formato delle procedure viene utilizzata principalmente da diversi interpreti, ma viene utilizzata anche per la conversione del buffer indipendentemente dalla modalità del compilatore. La tabella delle stringhe di formato del tipo viene utilizzata quando si chiama il motore di recapito di base per indicare tipi di dati specifici su cui lavorare.

## <a name="format-string-notation"></a>Notazione stringa di formato

La notazione utilizzata in questo documento segue le linee guida comuni per la descrizione della programmazione, con una barra ( \| ) utilizzata per indicare costrutti alternativi e parentesi quadre ( \[ \] ) utilizzati per indicare gli elementi facoltativi. Le stringhe di formato vengono spesso impilate per migliorare la leggibilità (responsabilità). In questo documento FC indica un singolo carattere di formato. I caratteri di formato vengono presentati in tutte le MAIUSCOLe, usando i nomi simbolici effettivi. Altri campi arbitrari sono rappresentati da un nome e da una dimensione.

Le parentesi angolari ( <> ) vengono utilizzate per indicare le dimensioni dei descrittori. Vengono utilizzate le convenzioni illustrate nella tabella seguente.



| Notation     | Significato                                                   |
|--------------|-----------------------------------------------------------|
| <*n*>  | Le dimensioni del descrittore sono pari a n byte.                        |
| <>     | Le dimensioni del descrittore variano.                            |
| {<>}\* | Il descrittore viene ripetuto per un numero qualsiasi di volte (0, 1, 2...). |



 

I caratteri di formato seguenti hanno un significato speciale.



| Carattere | Significato                                   |
|-----------|-------------------------------------------|
| \_fine FC   | Indica la fine di alcune stringhe di formato. |
| \_Pad FC   | Carattere di riempimento non interpretato.              |



 

 

 




