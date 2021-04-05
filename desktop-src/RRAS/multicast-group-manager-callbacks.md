---
title: Callback di gestione gruppi multicast
description: Il gestore del gruppo multicast usa i callback seguenti per notificare ai client (in genere, protocolli di routing) gli eventi e le modifiche di stato
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872738"
---
# <a name="multicast-group-manager-callbacks"></a><span data-ttu-id="c8394-103">Callback di gestione gruppi multicast</span><span class="sxs-lookup"><span data-stu-id="c8394-103">Multicast Group Manager Callbacks</span></span>

<span data-ttu-id="c8394-104">Il gestore del gruppo multicast utilizza i callback seguenti per notificare ai client (in genere, protocolli di routing) gli eventi e le modifiche di stato:</span><span class="sxs-lookup"><span data-stu-id="c8394-104">The multicast group manager uses the following callbacks to notify clients (typically, routing protocols) of events and state changes:</span></span>

[<span data-ttu-id="c8394-105">**\_ \_ callback avviso di creazione PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="c8394-105">**PMGM\_CREATION\_ALERT\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[<span data-ttu-id="c8394-106">**\_ \_ callback avviso PMGM \_ join**</span><span class="sxs-lookup"><span data-stu-id="c8394-106">**PMGM\_JOIN\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[<span data-ttu-id="c8394-107">**\_ \_ callback avviso di eliminazione \_ PMGM**</span><span class="sxs-lookup"><span data-stu-id="c8394-107">**PMGM\_PRUNE\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[<span data-ttu-id="c8394-108">**\_callback di \_ join \_ locale di PMGM**</span><span class="sxs-lookup"><span data-stu-id="c8394-108">**PMGM\_LOCAL\_JOIN\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[<span data-ttu-id="c8394-109">**\_callback di \_ Leave \_ locale di PMGM**</span><span class="sxs-lookup"><span data-stu-id="c8394-109">**PMGM\_LOCAL\_LEAVE\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[<span data-ttu-id="c8394-110">**\_callback RPF di PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="c8394-110">**PMGM\_RPF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[<span data-ttu-id="c8394-111">**PMGM \_ errato \_ se \_ callback**</span><span class="sxs-lookup"><span data-stu-id="c8394-111">**PMGM\_WRONG\_IF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

<span data-ttu-id="c8394-112">Il gestore del gruppo multicast utilizza i callback seguenti per notificare l'evento IGMP degli eventi e delle modifiche di stato:</span><span class="sxs-lookup"><span data-stu-id="c8394-112">The multicast group manager uses the following callbacks to notify IGMP of events and state changes:</span></span>

[<span data-ttu-id="c8394-113">**PMGM \_ Disabilita \_ \_ callback IGMP**</span><span class="sxs-lookup"><span data-stu-id="c8394-113">**PMGM\_DISABLE\_IGMP\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[<span data-ttu-id="c8394-114">**PMGM \_ Abilita \_ \_ callback IGMP**</span><span class="sxs-lookup"><span data-stu-id="c8394-114">**PMGM\_ENABLE\_IGMP\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 