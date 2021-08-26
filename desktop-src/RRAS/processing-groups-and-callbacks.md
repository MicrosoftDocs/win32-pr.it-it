---
title: Elaborazione di gruppi e callback
description: La tabella seguente riepiloga una serie di passaggi di un'interazione operativa tra un protocollo di routing e il gestore di gruppi multicast.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3315f0a5db0dbcef9ac13e07ff9b9a2bb0b476be
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479687"
---
# <a name="processing-groups-and-callbacks"></a>Elaborazione di gruppi e callback

La tabella seguente riepiloga una serie di passaggi di un'interazione operativa tra un protocollo di routing e il gestore di gruppi multicast. La prima colonna descrive le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore del gruppo multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing e le azioni eseguite dal gestore di gruppi multicast, ad esempio i callback. La terza colonna presenta eventuali informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.

Le attività elencate in questa tabella non vengono eseguite in un ordine specifico. si verificano invece in base allo stato delle appartenenze a gruppi multicast. La tabella seguente illustra un ordine di esempio.




| Azione del protocollo di routing | Azione di gestione del gruppo multicast | Note | 
|-------------------------|--------------------------------|-------|
| Gestire le appartenenze ai gruppi in base alle informazioni sul protocollo ricevute sulle interfacce di proprietà del protocollo. La gestione viene eseguita usando le funzioni seguenti:<ul><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li></ul> | Aggiungere ed eliminare dall'elenco di interfacce in uscita per le voci specificate (s, g), (*, g)* e ( , *). Questo elenco rappresenta il set di interfacce in cui vengono inoltrati i dati per questo gruppo. I dati per questo gruppo derivano dall'origine specificata. | 
| Inviare avvisi ai protocolli di routing sotto forma di callback. Gli eventi seguenti attivano il gestore di gruppi multicast per richiamare un callback:<ul><li>Aggiungere o lasciare gruppi ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li><li>Appartenenza al gruppo modificata da IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li><li>Dati ricevuti su un'interfaccia errata ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li><li>Dati ricevuti da nuove origini o da un nuovo gruppo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>e PMGM_RPF_CALLBACK</strong></a>).</li></ul> | Usando questi callback, il gestore di gruppi multicast è in grado di coordinare l'inoltro di pacchetti quando in un router sono presenti diversi protocolli di routing multicast. | 
| Enumerare le voci di inoltro multicast usando le <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>funzioni MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>e <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe.</strong></a> Prendere decisioni sui dati multicast in base ai risultati dell'enumerazione . | Restituisce gli MFE richiesti. Restituisce ERROR_NO_MORE items quando non sono presenti più MFE da restituire.<br /> | Usare le <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>funzioni MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> per enumerare le statistiche MFE. Per <a href="administrative-application-scenario.md">un esempio completo dell'uso</a> di queste funzioni, vedere Scenario dell'applicazione amministrativa.<br /> | 
| Modificare il router adiacente upstream in un'istanza MFE usando la <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>funzione MgmSetMfe.</strong></a> | I client usano questa funzione per modificare le informazioni relative all'interfaccia in ingresso. | 




 

 

