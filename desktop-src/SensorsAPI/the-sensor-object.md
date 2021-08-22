---
description: L'oggetto sensore rappresenta un sensore specifico.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Oggetto Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ad666153be31958bb758ca4b504e10591ccbe29c9d37355499c9d22c5aae2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666411"
---
# <a name="the-sensor-object"></a>Oggetto Sensor

L'oggetto sensore rappresenta un sensore specifico.

L'API Sensor rappresenta ogni sensore come oggetto sensore. È possibile usare un particolare oggetto sensore tramite la relativa [**interfaccia ISensor.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) Questa interfaccia consente di:

-   Recuperare i metadati relativi al sensore, ad esempio l'ID, il tipo o il nome descrittivo.
-   Recuperare informazioni sui dati specifici che il sensore può fornire.
-   Recuperare i dati in modo sincrono.
-   Recuperare informazioni sullo stato, ad esempio se il sensore è pronto.
-   Specificare gli eventi che verranno ricevuti dal programma.
-   Specificare l'interfaccia di callback che l'API Sensor può usare per fornire al programma notifiche degli eventi.

 

 



