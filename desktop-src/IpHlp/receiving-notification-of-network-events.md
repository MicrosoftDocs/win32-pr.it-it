---
description: Usare le funzioni seguenti per assicurarsi che un'applicazione riceva la notifica di determinati eventi di rete.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Ricezione di notifiche di eventi di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146614"
---
# <a name="receiving-notification-of-network-events"></a>Ricezione di notifiche di eventi di rete

Usare le funzioni seguenti per assicurarsi che un'applicazione riceva la notifica di determinati eventi di rete.

Usare la [**funzione NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) per richiedere la notifica di eventuali modifiche che si verificano nel mapping tra indirizzi IP e interfacce nel computer locale.

Analogamente, la funzione [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) consente a un'applicazione di richiedere la notifica di qualsiasi modifica che si verifica nella tabella di routing IP.

Le notifiche fornite da queste funzioni non specificano le modifiche. specificano semplicemente che è cambiato qualcosa. Usare altre funzioni helper IP, ad esempio [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)per determinare la natura esatta della modifica.

 

 



