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
# <a name="processing-groups-and-callbacks"></a>Gruppi e callback di elaborazione

Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione operativa tra un protocollo di routing e il gestore del gruppo multicast. Nella prima colonna sono descritte le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore del gruppo multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing ed eventuali azioni eseguite dal gestore del gruppo multicast, ad esempio i callback. La terza colonna presenta informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.

Le attività elencate in questa tabella non vengono eseguite in un ordine specifico. si basano invece sullo stato delle appartenenze ai gruppi multicast. La tabella seguente mostra un ordine di esempio.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Azione protocollo di routing</th>
<th>Azione gestione gruppi multicast</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gestire le appartenenze ai gruppi in base alle informazioni sul protocollo ricevute su tali interfacce di proprietà del protocollo. La gestione viene eseguita utilizzando le funzioni seguenti:
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li>
</ul></td>
<td>Aggiungere ed eliminare dall'elenco di interfacce in uscita per le voci (s, g), (*, g) e (*, *) specificate. Questo elenco rappresenta il set di interfacce su cui vengono trasmessi i dati per questo gruppo. I dati per questo gruppo sono dall'origine specificata.</td>

</tr>
<tr class="even">

<td>Inviare avvisi ai protocolli di routing sotto forma di callback. Gli eventi seguenti attivano il gestore del gruppo multicast per richiamare un callback:
<ul>
<li>Join o Leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>L'appartenenza a un gruppo è stata modificata da IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>Dati ricevuti in un'interfaccia errata ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Dati ricevuti da nuove origini o a un nuovo gruppo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> e <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li>
</ul></td>
<td>Utilizzando questi callback, il gestore del gruppo multicast è in grado di coordinare l'inoltro dei pacchetti quando in un router sono presenti diversi protocolli di routing multicast.</td>
</tr>
<tr class="odd">
<td>Enumerare le voci di inoltri multicast (MFE) utilizzando le funzioni <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>e <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> . Prendere decisioni sui dati multicast in base ai risultati dell'enumerazione.</td>
<td>Restituisce l'oggetto MFE richiesto. Restituisce ERROR_NO_MORE gli elementi quando non sono più presenti MFE da restituire.<br/></td>
<td>Usare le funzioni <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> per enumerare le statistiche di MFE. Per un esempio completo dell'utilizzo di queste funzioni, vedere <a href="administrative-application-scenario.md">scenario di applicazione amministrativa</a> .<br/></td>
</tr>
<tr class="even">
<td>Modificare il Neighbor upstream in un MFE usando la funzione <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</td>

<td>I client utilizzano questa funzione per modificare le informazioni relative all'interfaccia in ingresso.</td>
</tr>
</tbody>
</table>



 

 

