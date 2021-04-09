---
title: Contenitori e server
description: Contenitori e server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856905"
---
# <a name="containers-and-servers"></a>Contenitori e server

Le applicazioni per documenti composti sono di due tipi di base: applicazioni contenitore e applicazioni server. Le applicazioni contenitore OLE offrono agli utenti la possibilità di creare, modificare, salvare e recuperare documenti composti. Le applicazioni server OLE forniscono agli utenti i mezzi per creare documenti e altre rappresentazioni dati che possono essere contenuti come collegamenti o incorporamenti nelle applicazioni contenitore. Un'applicazione OLE può essere un'applicazione contenitore, un'applicazione server o entrambe.

Le applicazioni server OLE variano inoltre a seconda che siano implementate come *server in-process* o *server locali*. Un server in-process è una libreria a collegamento dinamico (DLL) eseguita nello spazio di processo dell'applicazione contenitore. È possibile eseguire un server in-process solo dall'interno dell'applicazione contenitore.

> [!Note]  
> Le versioni future di OLE consentiranno il collegamento e l'incorporamento tra i limiti del computer, in modo che un'applicazione contenitore in un computer sarà in grado di utilizzare un oggetto documento composto fornito da un *server remoto* in esecuzione in un altro computer. Dal punto di vista di un'applicazione contenitore, qualsiasi applicazione server OLE eseguita nello stesso spazio di processo, sia nello stesso computer che in un computer remoto, è un *Server processÂ*.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> </dl>

 

 




