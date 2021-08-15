---
description: È possibile estrarre file da un file CAB in due modi. Il primo e più semplice è sfruttare l'elaborazione automatica dei file CAB integrata nelle funzioni di configurazione.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Estrazione di file da file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887252"
---
# <a name="extracting-files-from-cabinets"></a>Estrazione di file da file CAB

È possibile estrarre file da un file CAB in due modi. Il primo e più semplice è sfruttare l'elaborazione automatica dei file CAB integrata nelle funzioni di configurazione.

Le funzioni di installazione, ad [**esempio SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), controllano la compressione in ogni file. Se il file si trova in un file CAB, le funzioni ricercano prima di tutto un file con lo stesso nome all'esterno dell'archivio. Se viene trovato, le funzioni installano il file esterno, ignorando il file all'interno del file CAB. In questo modo è possibile aggiornare un singolo file all'interno del file CAB senza ricompilare l'archivio.

Le funzioni di installazione rilevano anche quali file in un file CAB sono stati recuperati, in modo che un file viene estratto una sola volta, anche se viene installato più volte.

Il secondo modo per estrarre i file da un file CAB è tramite [**SetupIterateCabinet.**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) Questa funzione scorre ogni file in un file CAB, inviando una notifica a una routine di callback per ogni file trovato. La routine di callback restituisce quindi un valore che indica se il file deve essere estratto o ignorato.

> [!Note]  
> L'API di installazione non fornisce una routine di callback predefinita per gestire le notifiche cab. Se si chiama [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) in modo esplicito, è necessario fornire una routine di callback per elaborare le notifiche cab restituite dalla funzione.

 

 

 



