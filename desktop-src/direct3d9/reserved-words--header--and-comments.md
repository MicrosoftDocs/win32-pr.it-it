---
description: La tabella seguente mostra quali parole sono riservate e non devono essere usate.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Parole riservate, intestazione e commenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343656"
---
# <a name="reserved-words-header-and-comments"></a>Parole riservate, intestazione e commenti

La tabella seguente mostra quali parole sono riservate e non devono essere usate.

| Parole riservate | Parole riservate | Parole riservate|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | Ulonglong |
| RISORSA \_ BINARIA | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| Cstring          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

L'intestazione a lunghezza variabile è obbligatoria e deve essere all'inizio del flusso di dati. L'intestazione contiene i dati seguenti.



| Tipo           | Necessario | Dimensioni (in byte) | Valore | Descrizione                  |
|----------------|----------|-----------------|-------|------------------------------|
| Numero magico   | x        | 4               | Xof   |                              |
| Numero di versione | x        | 2               | 03    | Versione principale 3              |
|                |          |                 | 03    | Versione secondaria 3              |
| Tipo di formato    | x        | 4               | txt   | File di testo                    |
|                |          |                 | bin   | File binario                  |
|                |          |                 | tzip  | File di testo compresso MSZip   |
|                |          |                 | bzip  | File binario compresso MSZip |
| Dimensioni float     | x        | 0064            |       | Float a 64 bit                |
|                | x        | "0032"          |       | Float a 32 bit                |



 

I valori nella tabella sono delimitati da virgolette per richiamare l'attenzione sul numero di caratteri in ogni valore. Quelli con 4 byte contengono quattro caratteri, quelli con 2 byte contengono due caratteri.

I commenti sono applicabili solo nei file di testo. I commenti possono essere presenti in qualsiasi punto del flusso di dati. Un commento inizia con una doppia barra (//) in stile C++ o con un segno di cancelletto ( \# ). Il commento viene eseguito alla nuova riga successiva. L'esempio seguente mostra i commenti validi.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 



