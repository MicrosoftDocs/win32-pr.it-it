---
title: Richiamate avviso di eliminazione
description: Quando viene notificato al gestore del gruppo multicast che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il \_ callback di callback dell'avviso di eliminazione PMGM \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045248"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="79981-103">Richiamate avviso di eliminazione</span><span class="sxs-lookup"><span data-stu-id="79981-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="79981-104">Quando viene notificato al gestore del gruppo multicast che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="79981-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="79981-105">Questo callback notifica ai protocolli di routing che i client non appartengono più al gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="79981-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="79981-106">Pertanto, i protocolli di routing devono interrompere la richiesta di dati multicast per i gruppi specificati.</span><span class="sxs-lookup"><span data-stu-id="79981-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="79981-107">Il gestore del gruppo multicast dispone di un set predefinito di regole utilizzate per determinare quando questo callback viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="79981-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="79981-108">Queste regole sono basate sul tipo di richiesta di eliminazione inviata dal client e sull'ordine in cui sono state ricevute le richieste di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="79981-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="79981-109">Richieste di eliminazione con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="79981-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="79981-110">Quando viene ricevuta una potatura con caratteri jolly per un gruppo ( \* , g) e l'interfaccia finale viene rimossa per il client penultimo (ovvero, quando le interfacce per un solo client rimangono), il gestore del gruppo multicast richiama il callback di [**\_ \_ \_ callback dell'avviso di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) al client rimanente.</span><span class="sxs-lookup"><span data-stu-id="79981-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="79981-111">Una volta rimossa l'interfaccia finale per l'ultimo client (ovvero, quando non restano altre interfacce), questo callback viene richiamato per tutti gli altri client registrati con il gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="79981-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="79981-112">Richieste di eliminazione Source-Specific</span><span class="sxs-lookup"><span data-stu-id="79981-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="79981-113">Quando viene ricevuta una potatura specifica dell'origine per un gruppo (s, g), il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) solo per il client proprietario dell'interfaccia in ingresso verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="79981-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




