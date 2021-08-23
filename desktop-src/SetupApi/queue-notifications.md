---
description: Dopo aver eseguito il commit di una coda chiamando SetupCommitFileQueue, inizierà a elaborare le operazioni in coda. A ogni passaggio, la coda invia una notifica alla routine di callback specificata nella chiamata a SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notifiche della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665491"
---
# <a name="queue-notifications"></a>Notifiche della coda

Dopo aver eseguito il commit di una coda chiamando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), inizierà a elaborare le operazioni in coda. A ogni passaggio, la coda invia una notifica alla routine di callback specificata nella chiamata a **SetupCommitFileQueue.**

Di seguito è riportata la [**sintassi utilizzata da SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) per inviare una notifica alla routine di callback.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

I valori *di Param1* e *Param2* contengono informazioni aggiuntive relative alla notifica inviata alla routine di callback. Ogni notifica, i relativi valori *Param1* e *Param2* e il modo in cui la routine di callback della coda predefinita gestisce la notifica, è descritta in dettaglio in Notifiche delle code [di file.](file-queue-notifications.md)

 

 



