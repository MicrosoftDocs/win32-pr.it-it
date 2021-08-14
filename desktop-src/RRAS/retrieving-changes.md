---
title: Recupero delle modifiche
description: Dopo che un client ha eseguito la registrazione per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica dal gestore tabelle di routing.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea0de478a1f46e2281b18644026c2d8db44d113679f4f4f9bd5b18a1123e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788171"
---
# <a name="retrieving-changes"></a>Recupero delle modifiche

Dopo che un client ha eseguito la registrazione per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica dal gestore tabelle di routing. Il gestore tabelle di routing usa il callback [**\_ \_ CALLBACK DELL'EVENTO RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) fornito in una chiamata precedente a [**RtmRegisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) Il gestore tabelle di routing indica che si è verificato un evento \_ RTM CHANGE \_ NOTIFICATION.

Per il codice di esempio che illustra come usare queste funzioni, vedere [Usare il callback di notifica degli eventi.](use-the-event-notification-callback.md)

 

 




