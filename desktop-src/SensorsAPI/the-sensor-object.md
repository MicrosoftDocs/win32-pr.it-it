---
description: L'oggetto Sensor rappresenta un sensore specifico.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Oggetto Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314666"
---
# <a name="the-sensor-object"></a>Oggetto Sensor

L'oggetto Sensor rappresenta un sensore specifico.

L'API del sensore rappresenta ogni sensore come oggetto sensore. È possibile utilizzare un determinato oggetto sensore tramite l'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) . Questa interfaccia consente di:

-   Recuperare i metadati relativi al sensore, ad esempio l'ID, il tipo o il nome descrittivo.
-   Recuperare informazioni sui dati specifici che possono essere forniti dal sensore.
-   Recuperare i dati in modo sincrono.
-   Recuperare le informazioni sullo stato, ad esempio se il sensore è pronto.
-   Consente di specificare gli eventi che il programma riceverà.
-   Specificare l'interfaccia di callback che l'API del sensore può usare per fornire al programma notifiche degli eventi.

 

 



