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
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="43104-103">Ricezione della notifica degli eventi di rete</span><span class="sxs-lookup"><span data-stu-id="43104-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="43104-104">Usare le funzioni seguenti per assicurarsi che un'applicazione riceva una notifica di determinati eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="43104-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="43104-105">Utilizzare la funzione [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) per richiedere la notifica di qualsiasi modifica apportata nel mapping tra gli indirizzi IP e le interfacce nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="43104-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="43104-106">Analogamente, la funzione [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) consente a un'applicazione di richiedere la notifica di qualsiasi modifica che si verifica nella tabella di routing IP.</span><span class="sxs-lookup"><span data-stu-id="43104-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="43104-107">Le notifiche fornite da queste funzioni non specificano le modifiche. specificano semplicemente che un elemento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="43104-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="43104-108">Usare altre funzioni helper IP, ad esempio [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), per determinare la natura esatta della modifica.</span><span class="sxs-lookup"><span data-stu-id="43104-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



