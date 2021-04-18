---
description: Hot Spare
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Hot Spare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4d007e9219ea79ae3bda31be595c33b537661a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318920"
---
# <a name="hot-sparing"></a>Hot Spare

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La sostituzione a caldo è la sostituzione di un disco o di un'unità per un'unità o un disco guasto o guasto. (I provider hardware agiscono sulle unità; i provider di software agiscono sui dischi). È possibile condividere un'unità di riserva a caldo tra tutti i LUN del sottosistema o associarlo a un LUN specifico. Analogamente, è possibile associare un disco di riserva a caldo a un singolo volume, un pacchetto e un provider software oppure condividerlo tra tutti gli host in una rete SAN.

Se il volume o il LUN associato è a tolleranza di errore, è possibile sostituire una riserva a caldo per un disco danneggiato o per ricompilare eventuali mirror o RAID di parità interessati. È possibile sostituire una riserva a caldo per un disco guasto anche se il volume o il LUN associato non è a tolleranza di errore. Supponendo che sia possibile determinare l'errore imminente prima della perdita irreversibile dei dati, è possibile eseguire temporaneamente il mirroring della riserva a caldo sul disco o sull'unità con errore, quindi rimuovere il disco o l'unità che ha avuto esito negativo.

Il costato attivo può essere automatico o manuale. Se un provider implementa lo spessore a caldo automatico, esegue la sostituzione dinamicamente. Il costato attivo manuale richiede l'intervento di un operatore o di un'applicazione. Una riserva a caldo può contenere dati parziali o la formattazione di un utilizzo precedente. VDS sovrascrive la riserva a caldo quando si verifica la sostituzione.

Non è possibile usare una riserva a caldo per le normali operazioni di binding. Se la riserva a caldo è più grande del disco o dell'unità in errore, qualsiasi spazio in eccesso rimane inutilizzato fino a quando non viene dichiarato in modo esplicito disponibile per l'associazione. Una volta utilizzata la riserva a caldo per il ripristino, il disco o l'unità non è più una riserva a caldo. In altre parole, l'asse 1 16-gigabyte non può fungere da 2 8 gigabyte a caldo.

 

 
