---
title: Abilitazione e disabilitazione di callback IGMP
description: Il gestore del gruppo multicast utilizza due callback a IGMP per coordinare le modifiche alla proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872821"
---
# <a name="igmp-enable-and-disable-callbacks"></a><span data-ttu-id="409a8-103">Abilitazione e disabilitazione di callback IGMP</span><span class="sxs-lookup"><span data-stu-id="409a8-103">IGMP Enable and Disable Callbacks</span></span>

<span data-ttu-id="409a8-104">Il gestore del gruppo multicast utilizza due callback a IGMP per coordinare le modifiche alla proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP.</span><span class="sxs-lookup"><span data-stu-id="409a8-104">The multicast group manager uses two callbacks to IGMP to coordinate changes in interface ownership from IGMP to a routing protocol, and from a routing protocol to IGMP.</span></span> <span data-ttu-id="409a8-105">I callback consentono a IGMP di coesistere su un'interfaccia con un altro protocollo di routing, ad esempio DVMRP.</span><span class="sxs-lookup"><span data-stu-id="409a8-105">The callbacks enable IGMP to coexist on an interface with another routing protocol, such as DVMRP.</span></span>

<span data-ttu-id="409a8-106">Dopo che la proprietà di un'interfaccia è stata modificata, il gestore del gruppo multicast richiama per prima cosa il callback di [**\_ \_ \_ callback IGMP PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="409a8-106">After the ownership of an interface changes, the multicast group manager first invokes the [**PMGM\_DISABLE\_IGMP\_CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) callback.</span></span> <span data-ttu-id="409a8-107">IGMP deve interrompere l'aggiunta e l'eliminazione delle appartenenze ai gruppi nell'interfaccia specificata fino a quando il gestore del gruppo multicast richiama il callback di [**\_ \_ \_ callback IGMP di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="409a8-107">IGMP must stop adding and deleting group memberships on the specified interface until the multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.</span></span>

<span data-ttu-id="409a8-108">Il gestore del gruppo multicast richiama il callback [**PMGM \_ enable \_ IGMP \_ callback**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) dopo il completamento della modifica della proprietà dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="409a8-108">The multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback after the change of interface ownership is complete.</span></span>

 

 