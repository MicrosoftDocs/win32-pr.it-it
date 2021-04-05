---
title: Considerazioni sui set di proprietà
description: È consigliabile mantenere piccoli i set di proprietà perché il flusso del set di proprietà viene letto in memoria prima che una singola proprietà possa essere letta o scritta.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considerazioni sui set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714560"
---
# <a name="property-set-considerations"></a>Considerazioni sui set di proprietà

È consigliabile mantenere piccoli i set di proprietà perché il flusso del set di proprietà viene letto in memoria prima che una singola proprietà possa essere letta o scritta. "Small" significa meno di 32 kilobyte di dati. Questo raramente presenta un problema perché, in genere, le proprietà "inline" saranno elementi piccoli, ad esempio stringhe descrittive, parole chiave, timestamp, conteggi, nomi di autore, identificatori univoci globali (GUID), identificatori di classe (CLSID) e così via.

Per archiviare blocchi di dati di dimensioni maggiori o nei casi in cui la dimensione totale di un set di proprietà correlate supera la quantità consigliata, è consigliabile utilizzare tipi non semplici come **il \_ flusso di VT** e l' **\_ archiviazione VT** . Questi elementi non vengono archiviati all'interno del flusso del set di proprietà, pertanto non influiscono significativamente sul sovraccarico iniziale del primo accesso e della scrittura di una proprietà. Il flusso del set di proprietà contiene un overhead minimo perché contiene il nome del flusso di pari livello o della proprietà con valori di archiviazione e questa operazione richiede una quantità di tempo minore per l'elaborazione.

Per altre informazioni, vedere:

-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Archiviazione di set di proprietà](storing-property-sets.md)
-   [Caratteristiche di prestazioni](performance-characteristics.md)
-   [Implementazione del set di proprietà informazioni di riepilogo](implementing-the-summary-information-property-set.md)

 

 




