---
description: Le funzioni di installazione gestiscono gli armadi internamente. Per enumerare ed estrarre in modo esplicito i file da un file CAB, è possibile chiamare la funzione SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Uso dei file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316607"
---
# <a name="using-cabinet-files"></a>Uso dei file CAB

Le funzioni di installazione gestiscono gli armadi internamente. Per enumerare ed estrarre in modo esplicito i file da un file CAB, è possibile chiamare la funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

Nell'argomento seguente viene descritta l'elaborazione del file CAB interna alle funzioni di installazione e come usare [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Vengono inoltre descritte le notifiche inviate da **SetupIterateCabinet** e il formato necessario di una routine di callback del cabinet per elaborare tali notifiche.

-   [Estrazione di file da file CAB](extracting-files-from-cabinets.md)
-   [Creazione di una routine di callback del cabinet](creating-a-cabinet-callback-routine.md)

 

 



