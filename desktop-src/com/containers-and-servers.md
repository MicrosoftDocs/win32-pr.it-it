---
title: Contenitori e server
description: Contenitori e server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d301d85bc317cd4e60d609e73b6b7232cfb5634a33bf32a2496fe8cd672d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993571"
---
# <a name="containers-and-servers"></a>Contenitori e server

Le applicazioni documento composte sono di due tipi di base: applicazioni contenitore e applicazioni server. Le applicazioni contenitore OLE offrono agli utenti la possibilità di creare, modificare, salvare e recuperare documenti composti. Le applicazioni server OLE consentono agli utenti di creare documenti e altre rappresentazioni dei dati che possono essere contenuti come collegamenti o incorporamenti nelle applicazioni contenitore. Un'applicazione OLE può essere un'applicazione contenitore, un'applicazione server o entrambe.

Le applicazioni server OLE differiscono anche per il fatto che siano implementate *come server in-process* o *server locali.* Un server in-process è una libreria di collegamento dinamico (DLL) che viene eseguita nello spazio di elaborazione dell'applicazione contenitore. È possibile eseguire un server in-process solo dall'interno dell'applicazione contenitore.

> [!Note]  
> Le versioni future di OLE consentiranno il collegamento e l'incorporamento oltre i limiti del computer, in modo che un'applicazione contenitore in un computer possa usare un oggetto documento composto fornito da un *server* remoto in esecuzione in un altro computer. Dal punto di vista di un'applicazione contenitore, qualsiasi applicazione server OLE eseguita nel proprio spazio di elaborazione, sia nello stesso computer che in un computer remoto, è un *server out-of-process.*

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> </dl>

 

 




