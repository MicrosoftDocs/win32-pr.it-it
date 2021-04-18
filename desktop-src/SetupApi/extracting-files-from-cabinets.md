---
description: È possibile estrarre i file da un file CAB in due modi. Il primo e il modo più semplice consiste nel sfruttare l'elaborazione automatica del cabinet incorporata nelle funzioni di installazione.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Estrazione di file da file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308107"
---
# <a name="extracting-files-from-cabinets"></a>Estrazione di file da file CAB

È possibile estrarre i file da un file CAB in due modi. Il primo e il modo più semplice consiste nel sfruttare l'elaborazione automatica del cabinet incorporata nelle funzioni di installazione.

Le funzioni di installazione, ad esempio [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), controllano la compressione in ogni file. Se il file si trova in un file CAB, le funzioni cercano innanzitutto un file con tale nome all'esterno del cabinet. Se trovate, le funzioni installano il file esterno, ignorando il file all'interno del cabinet. In questo modo è possibile aggiornare un singolo file all'interno del cabinet senza ricompilare il file CAB.

Le funzioni di installazione tengono inoltre traccia dei file di un file CAB che sono stati recuperati, in modo che un file venga estratto una sola volta, anche se viene installato più volte.

Il secondo modo per estrarre i file da un file CAB consiste nell'usare [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Questa funzione esegue l'iterazione di ogni file in un file CAB, inviando una notifica a una routine di callback per ogni file trovato. La routine di callback restituisce quindi un valore che indica se il file deve essere estratto o ignorato.

> [!Note]  
> L'API di installazione non fornisce una routine di callback predefinita per la gestione delle notifiche del cabinet. Se si chiama [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) in modo esplicito, è necessario fornire una routine di callback per elaborare le notifiche del cabinet restituite dalla funzione.

 

 

 



