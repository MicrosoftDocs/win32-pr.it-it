---
title: Registrazione con gestione tabelle di routing
description: Prima che un client possa accedere alla tabella di routing, deve prima eseguire la registrazione con gestione tabelle di routing tramite la funzione RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gestione tabelle di routing versione 2 RRAS, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221356"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrazione con gestione tabelle di routing

Prima che un client possa accedere alla tabella di routing, deve prima eseguire la registrazione con gestione tabelle di routing tramite la funzione [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .

Quando un client esegue la registrazione, passa a gestione tabelle di routing una struttura di [**\_ \_ informazioni sull'entità RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) . Questa struttura contiene le informazioni che identificano in modo univoco un client, la famiglia di indirizzi e l'istanza di gestione tabelle di routing con cui il client sta effettuando la registrazione. Un client può anche stabilire il callback di [**\_ \_ callback evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) . Il servizio di gestione delle tabelle di routing utilizzerà questo callback per notificare al client gli eventi, ad esempio le notifiche di modifica e le registrazioni dei client.

Gestione tabelle di routing completa l'elaborazione della registrazione e restituisce un handle per il client. Il client deve usare questo handle per tutte le chiamate successive alle funzioni RTMv2.

La funzione [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) utilizzata in RTMv2 è analoga alla funzione [**RtmRegisterClient**](rtmregisterclient.md) utilizzata in RTMv1. La funzione **RtmRegisterClient** è obsoleta, ad eccezione dei client che utilizzano IPX.

Una volta che un client ha terminato l'interazione con gestione tabelle di routing, deve chiamare [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). Gestione tabelle di routing Elimina l'handle associato al client. Per evitare perdite di memoria, il client deve assicurarsi che rilasci tutti gli handle ed elimini tutte le route e gli hop successivi che possiede prima di chiamare **RtmDeregisterEntity**.

Per il codice di esempio che illustra come usare queste funzioni, vedere eseguire la [registrazione con gestione tabelle di routing](register-with-the-routing-table-manager.md) e [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).

 

 




