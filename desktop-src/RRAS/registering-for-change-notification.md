---
title: Registrazione per la notifica delle modifiche
description: Un client può registrarsi per ricevere la notifica delle modifiche alle informazioni di routing archiviate nel gestore tabelle di routing. Questa richiesta può essere effettuata solo dopo che un client è stato registrato con gestione tabelle di routing.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7049478a5be834b08b7bb17ad9ebfb0fdf70736837f27d53e7900bf7bfdc88dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788620"
---
# <a name="registering-for-change-notification"></a>Registrazione per la notifica delle modifiche

Un client può registrarsi per ricevere la notifica delle modifiche alle informazioni di routing archiviate nel gestore tabelle di routing. Questa richiesta può essere effettuata solo dopo che un client è stato registrato con gestione tabelle di routing.

Per eseguire la registrazione per la notifica delle modifiche, un client deve chiamare [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specificando i tipi di modifiche per cui il client deve ricevere la notifica. Se al client deve essere notificata la modifica a destinazioni specifiche, il client chiama [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) una volta per ogni destinazione.

Il client può smettere di ricevere notifiche di modifica chiamando [**RtmDeregisterFromChangeNotification.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

Per il codice di esempio che illustra come usare queste funzioni, vedere [Register For Change Notification](register-for-change-notification.md).

 

 




