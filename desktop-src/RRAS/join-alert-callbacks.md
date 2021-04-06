---
title: Callback di avviso di join
description: Quando al gestore del gruppo multicast viene notificato che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il \_ callback di callback di avviso di PMGM join \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044930"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="41449-103">Callback di avviso di join</span><span class="sxs-lookup"><span data-stu-id="41449-103">Join Alert Callbacks</span></span>

<span data-ttu-id="41449-104">Quando al gestore del gruppo multicast viene notificato che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback di [**\_ callback di \_ avviso \_ di PMGM join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="41449-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="41449-105">Questo callback notifica ai protocolli di routing che i nuovi host sono stati aggiunti ai gruppi specificati.</span><span class="sxs-lookup"><span data-stu-id="41449-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="41449-106">Pertanto, i protocolli di routing devono richiedere dati multicast per i gruppi specificati dal callback.</span><span class="sxs-lookup"><span data-stu-id="41449-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="41449-107">Il gestore del gruppo multicast utilizza un set predefinito di regole utilizzate per determinare quando viene richiamato il callback.</span><span class="sxs-lookup"><span data-stu-id="41449-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="41449-108">Questo set di regole è basato sul tipo di richiesta di join inviato dal client e sull'ordine con cui sono state ricevute le richieste di join.</span><span class="sxs-lookup"><span data-stu-id="41449-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="41449-109">Richieste di join con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="41449-109">Wildcard Join Requests</span></span>

<span data-ttu-id="41449-110">Quando viene ricevuto un join con caratteri jolly per un gruppo ( \* , g) dal primo client, il gestore del gruppo multicast richiama il callback di [**\_ callback di \_ avviso \_ di PMGM join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) a tutti gli altri client registrati.</span><span class="sxs-lookup"><span data-stu-id="41449-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="41449-111">Quando viene ricevuto un join con caratteri jolly per un gruppo dal secondo client, il gestore del gruppo multicast richiama questo callback al primo client per l'aggiunta al gruppo.</span><span class="sxs-lookup"><span data-stu-id="41449-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="41449-112">Richieste di join Source-Specific</span><span class="sxs-lookup"><span data-stu-id="41449-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="41449-113">Il gestore del gruppo multicast non richiama questo callback per i successivi join al gruppo.</span><span class="sxs-lookup"><span data-stu-id="41449-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="41449-114">Quando viene ricevuto un join specifico dell'origine per un gruppo (s, g), il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di join PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) solo per il client proprietario dell'interfaccia in ingresso verso l'origine s.</span><span class="sxs-lookup"><span data-stu-id="41449-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




