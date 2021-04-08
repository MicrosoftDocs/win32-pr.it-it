---
title: Uso di Teredo con helper IP
description: L'API helper protocollo Internet (helper IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728479"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="24305-103">Uso di Teredo con helper IP</span><span class="sxs-lookup"><span data-stu-id="24305-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="24305-104">L'API [Helper protocollo Internet](/windows/desktop/IpHlp/about-ip-helper) (helper IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale.</span><span class="sxs-lookup"><span data-stu-id="24305-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="24305-105">Quando si opera sulla piattaforma Windows Vista, queste informazioni includono la porta UDP dinamica assegnata all'interfaccia Teredo e le modifiche che possono verificarsi nella porta designata.</span><span class="sxs-lookup"><span data-stu-id="24305-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="24305-106">Le funzioni seguenti vengono utilizzate dall'API helper IP per semplificare l'utilizzo dell'interfaccia Teredo:</span><span class="sxs-lookup"><span data-stu-id="24305-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="24305-107">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="24305-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="24305-108">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="24305-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="24305-109">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="24305-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 