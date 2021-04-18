---
description: Dopo che è stato eseguito il commit di una coda chiamando SetupCommitFileQueue, l'elaborazione delle operazioni in coda verrà avviata. In ogni fase la coda Invia una notifica alla routine di callback specificata nella chiamata a SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notifiche della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316083"
---
# <a name="queue-notifications"></a>Notifiche della coda

Dopo che è stato eseguito il commit di una coda chiamando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), l'elaborazione delle operazioni in coda verrà avviata. In ogni fase la coda Invia una notifica alla routine di callback specificata nella chiamata a **SetupCommitFileQueue**.

Di seguito è riportata la sintassi utilizzata da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) per inviare una notifica alla routine di callback.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

I valori di *param1* e *param2* contengono informazioni aggiuntive relative alla notifica inviata alla routine di callback. Ogni notifica, i relativi valori *param1* e *param2* e il modo in cui la routine di callback della coda predefinita gestisce tale notifica, è descritta in dettaglio in [notifiche coda file](file-queue-notifications.md).

 

 



