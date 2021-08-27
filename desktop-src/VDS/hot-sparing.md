---
description: Sparing a caldo
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Sparing a caldo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125951"
---
# <a name="hot-sparing"></a>Sparing a caldo

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Lo sparing a caldo è la sostituzione di un disco o di un'unità per un disco o un'unità in errore o non riuscita. I provider di hardware agiscono sulle unità, i provider di software agiscono sui dischi. È possibile condividere un'unità hot spare tra tutti i LUN nel sottosistema o associarla a un LUN specifico. Analogamente, è possibile associare un disco di riserva a caldo a un singolo volume, pacchetto e provider software oppure condividerlo tra tutti gli host in una san.

Se il volume o il LUN associato è a tolleranza di errore, è possibile sostituire una riserva a caldo per un disco o un'unità non riuscita e ricompilare eventuali RAID o mirror di parità interessati. È possibile sostituire una riserva a caldo per un disco in errore anche se il volume o il LUN associato non è a tolleranza di errore. Supponendo che sia possibile determinare l'errore imminente prima di una perdita di dati irreversibile, è possibile eseguire temporaneamente il mirroring della riserva a caldo sul disco o sull'unità in errore e quindi rimuovere il disco o l'unità in errore.

Lo sparing a caldo può essere automatico o manuale. Se un provider implementa lo sparing automatico a caldo, esegue la sostituzione in modo dinamico. Lo sparing a caldo manuale richiede l'intervento dell'operatore o dell'applicazione. Una riserva a caldo può contenere dati parziali o formattazione di un uso precedente. VDS sovrascrive la riserva a caldo quando si verifica la sostituzione.

Non è possibile usare una riserva a caldo per le normali operazioni di associazione. Se lo spazio di riserva a caldo è maggiore del disco o dell'unità con errore, lo spazio in eccesso rimane inutilizzato fino a quando non viene dichiarato in modo esplicito disponibile per l'associazione. Dopo aver usato la riserva a caldo per il ripristino, il disco o l'unità non è più una riserva a caldo. In altre parole, un mandrino da 16 gigabyte non può fungere da due ricambi a caldo da 8 gigabyte.

 

 
