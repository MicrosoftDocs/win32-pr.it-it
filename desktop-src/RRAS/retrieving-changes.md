---
title: Recupero delle modifiche
description: Una volta che un client si è registrato per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica da Gestione tabelle di routing.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515619"
---
# <a name="retrieving-changes"></a>Recupero delle modifiche

Una volta che un client si è registrato per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica da Gestione tabelle di routing. Gestione tabelle di routing utilizza il callback di [**\_ \_ callback evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) fornito in una chiamata precedente a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity). Gestione tabelle di routing indica che \_ \_ si è verificato un evento di notifica della modifica RTM.

Per il codice di esempio che illustra come usare queste funzioni, vedere [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).

 

 




