---
description: Gli amministratori possono utilizzare COM+ per creare e configurare le partizioni COM+ a livello di codice.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Creazione e configurazione di partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523561"
---
# <a name="creating-and-configuring-com-partitions"></a>Creazione e configurazione di partizioni COM+

Gli amministratori possono utilizzare COM+ per creare e configurare le partizioni COM+ a livello di codice. In realtà, tutte le attività di creazione e configurazione che un amministratore può eseguire da Servizi componenti o gli strumenti di amministrazione Active Directory utenti e computer possono essere eseguite utilizzando le raccolte, gli oggetti e le interfacce COM+ oppure tramite l'interfaccia di sistema Active Directory (ADSI).

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

* * Windows 2000: * * il servizio partizioni COM+ non è disponibile in Windows 2000.

> [!Note]  
> Il servizio partizioni COM+ non è abilitato per impostazione predefinita. Per utilizzare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) su true.

 

Per eseguire attività correlate alle partizioni, COM+ fornisce gli elementi di programmazione seguenti:

-   Metodi e proprietà dell'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) nella classe [**COMAdminCatalog**](comadmincatalog.md) :
    -   Proprietà [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .
    -   Proprietà [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .
    -   Proprietà [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .
    -   Metodo [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .
    -   Metodo [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .
    -   Metodo [**Getpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .
    -   Proprietà [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .
-   Set di oggetti COM+ per la creazione e la gestione di partizioni in Active Directory.
-   Chiave del registro di sistema COM+, **PartitionCache**, per la modifica delle dimensioni della cache della partizione.
-   Set di [raccolte di amministrazione com+](com--administration-collections.md)correlate alle partizioni:
    -   Raccolta di [**partizioni**](partitions.md) .
    -   Raccolta [**PartitionUsers**](partitionusers.md) .
    -   Raccolta [**RolesForPartition**](rolesforpartition.md) .
    -   Raccolta [**UsersInPartitionRole**](usersinpartitionrole.md) .
-   Proprietà di altre [raccolte di amministrazione com+](com--administration-collections.md):
    -   Proprietà PartitionID nella raccolta [**ApplicationInstances**](applicationinstances.md) .
    -   Proprietà AppPartitionID nella raccolta di [**applicazioni**](applications.md) .
    -   Proprietà PartitionDescription, PartitionID e partitionName nella raccolta [**FilesForImport**](filesforimport.md) .
    -   Proprietà DSPartitionLookupEnabled, LocalPartitionLookupEnabled e PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) .
    -   Proprietà EventClassPartitionID e SubscriberPartitionID nella raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .
    -   Proprietà EventClassPartitionID e SubscriberPartitionID nella raccolta [**TransientSubscriptions**](transientsubscriptions.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche della partizione](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache della partizione](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione di partizioni all'interno Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



