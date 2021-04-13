---
title: Gruppi e callback di elaborazione
description: Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione operativa tra un protocollo di routing e il gestore del gruppo multicast.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339478"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="07bc8-103">Gruppi e callback di elaborazione</span><span class="sxs-lookup"><span data-stu-id="07bc8-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="07bc8-104">Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione operativa tra un protocollo di routing e il gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="07bc8-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="07bc8-105">Nella prima colonna sono descritte le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="07bc8-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="07bc8-106">La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing ed eventuali azioni eseguite dal gestore del gruppo multicast, ad esempio i callback.</span><span class="sxs-lookup"><span data-stu-id="07bc8-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="07bc8-107">La terza colonna presenta informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="07bc8-107">The third column presents any additional information.</span></span>

<span data-ttu-id="07bc8-108">Ogni riga della tabella rappresenta un passaggio.</span><span class="sxs-lookup"><span data-stu-id="07bc8-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="07bc8-109">Le attività elencate in questa tabella non vengono eseguite in un ordine specifico. si basano invece sullo stato delle appartenenze ai gruppi multicast.</span><span class="sxs-lookup"><span data-stu-id="07bc8-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="07bc8-110">La tabella seguente mostra un ordine di esempio.</span><span class="sxs-lookup"><span data-stu-id="07bc8-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07bc8-111">Azione protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="07bc8-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="07bc8-112">Azione gestione gruppi multicast</span><span class="sxs-lookup"><span data-stu-id="07bc8-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="07bc8-113">Note</span><span class="sxs-lookup"><span data-stu-id="07bc8-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07bc8-114">Gestire le appartenenze ai gruppi in base alle informazioni sul protocollo ricevute su tali interfacce di proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="07bc8-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="07bc8-115">La gestione viene eseguita utilizzando le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="07bc8-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="07bc8-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="07bc8-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="07bc8-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="07bc8-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="07bc8-118">Aggiungere ed eliminare dall'elenco di interfacce in uscita per le voci (s, g), (*, g) e (*, \*) specificate.</span><span class="sxs-lookup"><span data-stu-id="07bc8-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="07bc8-119">Questo elenco rappresenta il set di interfacce su cui vengono trasmessi i dati per questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="07bc8-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="07bc8-120">I dati per questo gruppo sono dall'origine specificata.</span><span class="sxs-lookup"><span data-stu-id="07bc8-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="07bc8-121">Inviare avvisi ai protocolli di routing sotto forma di callback.</span><span class="sxs-lookup"><span data-stu-id="07bc8-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="07bc8-122">Gli eventi seguenti attivano il gestore del gruppo multicast per richiamare un callback:</span><span class="sxs-lookup"><span data-stu-id="07bc8-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="07bc8-123">Join o Leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="07bc8-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="07bc8-124">L'appartenenza a un gruppo è stata modificata da IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="07bc8-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="07bc8-125">Dati ricevuti in un'interfaccia errata ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="07bc8-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="07bc8-126">Dati ricevuti da nuove origini o a un nuovo gruppo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> e <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="07bc8-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="07bc8-127">Utilizzando questi callback, il gestore del gruppo multicast è in grado di coordinare l'inoltro dei pacchetti quando in un router sono presenti diversi protocolli di routing multicast.</span><span class="sxs-lookup"><span data-stu-id="07bc8-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07bc8-128">Enumerare le voci di inoltri multicast (MFE) utilizzando le funzioni <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>e <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="07bc8-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="07bc8-129">Prendere decisioni sui dati multicast in base ai risultati dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="07bc8-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="07bc8-130">Restituisce l'oggetto MFE richiesto.</span><span class="sxs-lookup"><span data-stu-id="07bc8-130">Return the requested MFEs.</span></span> <span data-ttu-id="07bc8-131">Restituisce ERROR_NO_MORE gli elementi quando non sono più presenti MFE da restituire.</span><span class="sxs-lookup"><span data-stu-id="07bc8-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="07bc8-132">Usare le funzioni <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> per enumerare le statistiche di MFE.</span><span class="sxs-lookup"><span data-stu-id="07bc8-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="07bc8-133">Per un esempio completo dell'utilizzo di queste funzioni, vedere <a href="administrative-application-scenario.md">scenario di applicazione amministrativa</a> .</span><span class="sxs-lookup"><span data-stu-id="07bc8-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07bc8-134">Modificare il Neighbor upstream in un MFE usando la funzione <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="07bc8-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="07bc8-135">I client utilizzano questa funzione per modificare le informazioni relative all'interfaccia in ingresso.</span><span class="sxs-lookup"><span data-stu-id="07bc8-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

