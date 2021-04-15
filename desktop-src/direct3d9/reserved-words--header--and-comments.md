---
description: La tabella seguente mostra quali parole sono riservate e non devono essere usate.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Parole riservate, intestazioni e commenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520889"
---
# <a name="reserved-words-header-and-comments"></a>Parole riservate, intestazioni e commenti

La tabella seguente mostra quali parole sono riservate e non devono essere usate.



|                  |          |           |
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| risorsa BINARIa \_ | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

L'intestazione a lunghezza variabile è obbligatoria e deve trovarsi all'inizio del flusso di dati. L'intestazione contiene i dati seguenti.



| Tipo           | Necessario | Dimensioni (in byte) | Valore | Descrizione                  |
|----------------|----------|-----------------|-------|------------------------------|
| Numero magico   | x        | 4               | XOF   |                              |
| Numero di versione | x        | 2               | 03    | Versione principale 3              |
|                |          |                 | 03    | Versione secondaria 3              |
| Tipo di formato    | x        | 4               | txt   | File di testo                    |
|                |          |                 | bin   | File binario                  |
|                |          |                 | tzip  | File di testo compresso MSZip   |
|                |          |                 | bzip  | File binario compresso MSZip |
| Dimensioni float     | x        | 0064            |       | float a 64 bit                |
|                | x        | "0032"          |       | float a 32 bit                |



 

I valori nella tabella sono delimitati da virgolette per richiamare l'attenzione sul numero di caratteri in ogni valore. Quelli con 4 byte contengono quattro caratteri, quelli con 2 byte contengono due caratteri.

I commenti sono applicabili solo ai file di testo. I commenti possono essere presenti in qualsiasi punto del flusso di dati. Un commento inizia con le barre doppie (//) di tipo C++ o con un segno di cancelletto ( \# ). Il commento viene eseguito alla nuova riga successiva. Nell'esempio seguente vengono illustrati i commenti validi.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 



