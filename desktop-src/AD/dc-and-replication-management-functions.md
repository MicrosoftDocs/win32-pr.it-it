---
title: Controller di dominio e funzioni di gestione della replica
description: Questo argomento contiene un elenco di funzioni usate per il controller di dominio e la gestione della replica.
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046531"
---
# <a name="domain-controller-and-replication-management-functions"></a>Controller di dominio e funzioni di gestione della replica

Il controller di dominio (DC) e le funzioni di gestione della replica forniscono gli strumenti per individuare i dati relativi a un controller di dominio, convertendo i nomi degli oggetti di rete tra formati diversi, modificando i nomi dell'entità servizio (SPN) e gli agenti del servizio directory (DSA) e gestendo la replica dei server. Le funzioni seguenti consentono agli sviluppatori di lavorare con i controller di dominio, la replica e il servizio directory:

-   [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**DsBindingSetTimeout**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**DsBindToISTG**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**DsBindWithSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**DsBindWithSpnEx**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**DsClientMakeSpnForTargetServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**DsCrackSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**DsCrackUnquotedMangledRdn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**DsFreeDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**DsFreeNameResult**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**DsFreePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**DsFreeSchemaGuidMap**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**DsGetDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**DsGetRdnW**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**DsInheritSecurityIdentity**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**DsIsMangledDn**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**DsIsMangledRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**DsListDomainsInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**DsListInfoForServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**DsListRoles**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**DsListServersForDomainInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**DsListServersInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**DsListSites**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**DsMakePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**DsMapSchemaGuids**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**DsQuerySitesByCost**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**DsQuerySitesFree**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**DsQuoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**DsRemoveDsDomain**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**DsRemoveDsServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**DsReplicaFreeInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**DsReplicaVerifyObjects**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**DsUnquoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**SyncUpdateProc**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

La maggior parte di queste funzioni richiede un handle associato al servizio directory. Le funzioni [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda) e [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda) avviano una sessione RPC con un controller di dominio specifico, quindi associano un handle al servizio directory e restituiscono l'handle. Quando l'handle non è più necessario, utilizzare la funzione [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) per terminare la sessione RPC e annullare il binding dell'handle.

La replica viene eseguita tra un server di origine e un server di destinazione. Un server di origine gestisce un elenco dei server di destinazione in cui deve essere replicato e un server di destinazione gestisce un elenco dei server di origine da cui riceve la replica. Utilizzare la funzione [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) per aggiungere all'elenco dei server di origine in un server di destinazione e utilizzare la funzione [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) per rimuovere i riferimenti dall'elenco dei server di origine in un server di destinazione. La funzione [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya) può essere utilizzata per modificare un riferimento al server di origine esistente in un server di destinazione. Per modificare l'elenco dei server di destinazione in un server di origine, utilizzare la funzione [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) .

La replica effettiva viene eseguita dalle funzioni [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) e [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) . La funzione **DsReplicaSync** sincronizza un server di destinazione specifico con un unico server di origine. Utilizzare la funzione **DsReplicaSyncAll** per sincronizzare un server di destinazione con tutti gli altri server del sito.

 

 