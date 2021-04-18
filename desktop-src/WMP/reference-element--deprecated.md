---
title: Elemento Reference (deprecato)
description: Elemento Reference (deprecato)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metafile di Windows Media, elemento Reference
- Metafile, elemento Reference
- Reference-elemento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298528"
---
# <a name="reference-element-deprecated"></a>Elemento Reference (deprecato)

In questo argomento viene documentata una funzionalità che non viene più utilizzata nella versione corrente dei file di Windows Media.

L'elemento **Reference** contiene un elenco di riferimenti agli URL. Ogni elemento nell'elenco ha il formato URL ref *XX*  =  , dove *XX* è un numero intero e *URL* è l'URL di un file di formato ASF (Advanced Systems Format).

**Sintassi**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



I numeri interi rappresentati da *XX* devono essere in ordine crescente. Ovvero il valore integer in ogni riga deve essere maggiore di quello della riga precedente.

Quando un programma client legge un elemento di riferimento, tenta di connettersi al file multimediale rappresentato dal primo URL nell'elenco. Se l'operazione ha esito negativo, il programma client tenta di connettersi al file rappresentato dall'URL successivo nell'elenco. Il programma client continua a scorrere l'elenco fino a quando non riesce a connettersi o raggiunge la fine dell'elenco. Si noti che se il programma client effettua una connessione, non legge alcun URL successivo nell'elenco.

**Codice di esempio**

Nell'esempio seguente il programma client tenterà innanzitutto di connettersi al file rappresentato dall'URL di MMS. Se l'operazione non è riuscita, il programma client tenterà di connettersi al file rappresentato dall'URL http.


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>Commenti

Il formato di file ASF comprende un'ampia gamma di tipi di supporti, inclusi audio e video. I file ASF usano anche diverse estensioni di file, tra cui WMA e WMV.

I numeri interi rappresentati da *XX* devono essere in ordine crescente. Ovvero il valore integer in ogni riga deve essere maggiore di quello della riga precedente.

Quando un programma client legge un elemento di riferimento, tenta di connettersi al file multimediale rappresentato dal primo URL nell'elenco. Se l'operazione ha esito negativo, il programma client tenta di connettersi al file rappresentato dall'URL successivo nell'elenco. Il programma client continua a scorrere l'elenco fino a quando non riesce a connettersi o raggiunge la fine dell'elenco. Si noti che se il programma client effettua una connessione, non legge alcun URL successivo nell'elenco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Versioni precedenti dei file di Windows Media (deprecato)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




