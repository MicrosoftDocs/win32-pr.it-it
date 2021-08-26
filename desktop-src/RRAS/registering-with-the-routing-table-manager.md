---
title: Registrazione con Gestione tabelle di routing
description: Prima di poter accedere alla tabella di routing, un client deve prima registrarsi con la gestione tabelle di routing usando la funzione RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gestione tabelle di routing versione 2 RRAS, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088072fac8679d9b2f87729b67a826ac850e77109f18b28fef3c2dc33c433f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028291"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrazione con Gestione tabelle di routing

Prima di poter accedere alla tabella di routing, un client deve prima registrarsi con la gestione tabelle di routing usando la [**funzione RtmRegisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

Quando un client si registra, passa al gestore tabelle di routing una [**struttura RTM \_ ENTITY \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Questa struttura contiene le informazioni che identificano in modo univoco un client, la famiglia di indirizzi e l'istanza del gestore tabelle di routing con cui il client sta registrando. Un client può anche stabilire il callback [**\_ DI \_ CALLBACK DELL'EVENTO RTM.**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) Il gestore tabelle di routing utilizzerà questo callback per notificare al client eventi quali le notifiche di modifica e le registrazioni client.

Il gestore tabelle di routing completa l'elaborazione della registrazione e restituisce un handle al client. Il client deve usare questo handle per tutte le chiamate successive alle funzioni RTMv2.

La [**funzione RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) usata in RTMv2 è analoga alla funzione [**RtmRegisterClient**](rtmregisterclient.md) usata in RTMv1. La **funzione RtmRegisterClient** è obsoleta, ad eccezione dei client che usano IPX.

Al termine dell'interazione con il gestore tabelle di routing, un client deve [**chiamare RtmDeregisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity) Il gestore tabelle di routing elimina l'handle associato al client. Per evitare perdite di memoria, il client deve assicurarsi che rilasci tutti gli handle ed elimini tutte le route e gli hop successivi di cui è proprietario prima di chiamare **RtmDeregisterEntity.**

Per il codice di esempio che illustra come usare queste funzioni, vedere Eseguire la registrazione con Gestione tabelle [di routing](register-with-the-routing-table-manager.md) e Usare il callback di notifica [degli eventi.](use-the-event-notification-callback.md)

 

 




