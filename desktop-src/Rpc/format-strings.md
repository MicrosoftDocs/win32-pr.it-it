---
title: Stringhe di formato
description: Una stringa di formato è un token interpretato che il motore NDR comprende. Le stringhe di formato sono spesso denominate MOP. questa documentazione usa il termine stringa di formato in tutto.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8c14fa649e71411c5706193e83fd9a09d30f8a0c57fec411d8c34fef675ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929868"
---
# <a name="format-strings"></a>Stringhe di formato

Una stringa di formato è un token interpretato che il motore NDR comprende. Le stringhe di formato sono spesso denominate MOP. questa documentazione usa il termine stringa di formato in tutto.

Per essere più precisi, un carattere di formato è un singolo token interpretabile (atomico). Ogni carattere di formato ha una dimensione di un byte. Una stringa di formato è una sequenza di caratteri di formato o caratteri di formato e dati numerici. Il termine descrittore viene usato anche per la denominazione di sequenze comuni. Ad esempio, una stringa di formato di parametro o un descrittore di parametro è una stringa di formato usata per descrivere un parametro di una routine.

I caratteri di formato hanno nomi simbolici allusivi, ad esempio FC \_ LONG o FC \_ STRUCT. Tutti i caratteri della stringa di formato usati da MIDL e dal motore NDR sono definiti nel file Ndrtypes.h.

## <a name="format-string-tables"></a>Formattare tabelle di stringhe

Il motore usa due tabelle di stringhe di formato principali: la tabella delle stringhe di formato della **\_ \_ procedura, MIDL \_ ProcFormatString**, che mantiene i descrittori di procedura, e la tabella delle stringhe di formato del **\_ \_ tipo, MIDL \_ TypeFormatString,** che mantiene i descrittori dei tipi di dati. Il compilatore genera entrambi nei file stub principali ( \* \_ c.c, \* \_ s.c, \* \_ p.c). La tabella delle stringhe di formato di routine viene usata principalmente da diversi interpreti, ma viene usata anche per la conversione del buffer indipendentemente dalla modalità del compilatore. La tabella delle stringhe di formato del tipo viene usata quando si chiama il motore NDR principale per indicare tipi di dati specifici su cui lavorare.

## <a name="format-string-notation"></a>Notazione stringa di formato

La notazione usata in questo documento segue le linee guida comuni per la descrizione della programmazione, con una barra ( ) usata per indicare costrutti alternativi e parentesi quadre ( ) usate per indicare elementi \| \[ \] facoltativi. Le stringhe di formato sono spesso sovrapposte per una maggiore leggibilità (responsabilità). In questo documento, FC indica un singolo carattere di formato. I caratteri di formato vengono presentati in caratteri maiuscoli, usando i nomi simbolici effettivi. Altri campi arbitrari sono rappresentati da un nome e da una dimensione.

Le parentesi angolari ( <> ) vengono usate per indicare le dimensioni dei descrittori. Vengono utilizzate le convenzioni illustrate nella tabella seguente.



| Notation     | Significato                                                   |
|--------------|-----------------------------------------------------------|
| <*N*>  | La dimensione del descrittore è n byte.                        |
| <>     | La dimensione del descrittore varia.                            |
| {<>}\* | Il descrittore viene ripetuto un numero qualsiasi di volte (0,1,2 ...). |



 

I caratteri di formato seguenti hanno un significato speciale.



| Carattere | Significato                                   |
|-----------|-------------------------------------------|
| FC \_ END   | Indica la fine di alcune stringhe di formato. |
| FC \_ PAD   | Carattere di riempimento non interpretato.              |



 

 

 




