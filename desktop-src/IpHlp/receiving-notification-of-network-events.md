---
description: Usare le funzioni seguenti per assicurarsi che un'applicazione riceva una notifica di determinati eventi di rete.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Ricezione della notifica degli eventi di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306593"
---
# <a name="receiving-notification-of-network-events"></a>Ricezione della notifica degli eventi di rete

Usare le funzioni seguenti per assicurarsi che un'applicazione riceva una notifica di determinati eventi di rete.

Utilizzare la funzione [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) per richiedere la notifica di qualsiasi modifica apportata nel mapping tra gli indirizzi IP e le interfacce nel computer locale.

Analogamente, la funzione [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) consente a un'applicazione di richiedere la notifica di qualsiasi modifica che si verifica nella tabella di routing IP.

Le notifiche fornite da queste funzioni non specificano le modifiche. specificano semplicemente che un elemento è stato modificato. Usare altre funzioni helper IP, ad esempio [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), per determinare la natura esatta della modifica.

 

 



