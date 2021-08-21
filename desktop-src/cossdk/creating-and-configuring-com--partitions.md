---
description: Gli amministratori possono usare COM+ per creare e configurare partizioni COM+ a livello di codice.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Creazione e configurazione di partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cc9623272d4aba345cc666deb5c63965584af94f42dbf869b00cf7d52a2f30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858991"
---
# <a name="creating-and-configuring-com-partitions"></a>Creazione e configurazione di partizioni COM+

Gli amministratori possono usare COM+ per creare e configurare partizioni COM+ a livello di codice. Di fatto, tutte le attività di creazione e configurazione che un amministratore può eseguire da Servizi componenti o dagli strumenti di amministrazione di Utenti e computer di Active Directory possono essere eseguite usando raccolte, oggetti e interfacce COM+ o tramite Active Directory System Interface (ADSI).

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

**Windows 2000: ** Il servizio partizioni COM+ non è disponibile in Windows 2000.

> [!Note]  
> Il servizio partizioni COM+ non è abilitato per impostazione predefinita. Per usare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione di Servizi componenti o impostando la proprietà PartitionsEnabled della raccolta [**LocalComputer**](localcomputer.md) su True.

 

Per eseguire attività correlate alla partizione, COM+ fornisce gli elementi di programmazione seguenti:

-   Metodi e proprietà [**dell'interfaccia ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) nella [**classe COMAdminCatalog:**](comadmincatalog.md)
    -   [**Proprietà CurrentPartition.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition)
    -   [**Proprietà CurrentPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid)
    -   [**Proprietà CurrentPartitionName.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname)
    -   [**Metodo FlushPartitionCache.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)
    -   [**Metodo GetPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid)
    -   [**Metodo GetPartitionName.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname)
    -   [**Proprietà GlobalPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid)
-   Set di oggetti COM+ per la creazione e la gestione delle partizioni in Active Directory.
-   Una chiave del Registro di sistema COM+, **PartitionCache**, per modificare le dimensioni della cache della partizione.
-   Un set di raccolte di amministrazione [COM+ correlate alle partizioni:](com--administration-collections.md)
    -   [**Raccolta partizioni.**](partitions.md)
    -   [**Insieme PartitionUsers.**](partitionusers.md)
    -   [**Raccolta RolesForPartition.**](rolesforpartition.md)
    -   [**Raccolta UsersInPartitionRole.**](usersinpartitionrole.md)
-   Proprietà di altre [raccolte di amministrazione COM+:](com--administration-collections.md)
    -   Proprietà PartitionID nella [**raccolta ApplicationInstances.**](applicationinstances.md)
    -   Proprietà AppPartitionID nella [**raccolta Applications.**](applications.md)
    -   Proprietà PartitionDescription, PartitionID e PartitionName nella [**raccolta FilesForImport.**](filesforimport.md)
    -   Proprietà DSPartitionLookupEnabled, LocalPartitionLookupEnabled e PartitionsEnabled nella [**raccolta LocalComputer.**](localcomputer.md)
    -   Proprietà EventClassPartitionID e SubscriberPartitionID nella [**raccolta SubscriptionsForComponent.**](subscriptionsforcomponent.md)
    -   Proprietà EventClassPartitionID e SubscriberPartitionID nella [**raccolta TransientSubscriptions.**](transientsubscriptions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



