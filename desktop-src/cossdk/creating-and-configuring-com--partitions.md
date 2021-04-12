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
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="dfbef-103">Creazione e configurazione di partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="dfbef-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="dfbef-104">Gli amministratori possono utilizzare COM+ per creare e configurare le partizioni COM+ a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="dfbef-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="dfbef-105">In realtà, tutte le attività di creazione e configurazione che un amministratore può eseguire da Servizi componenti o gli strumenti di amministrazione Active Directory utenti e computer possono essere eseguite utilizzando le raccolte, gli oggetti e le interfacce COM+ oppure tramite l'interfaccia di sistema Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="dfbef-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="dfbef-106">**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="dfbef-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="dfbef-107">La partizione globale è l'unica partizione COM+ disponibile.</span><span class="sxs-lookup"><span data-stu-id="dfbef-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="dfbef-108">\* \* Windows 2000: \* \* il servizio partizioni COM+ non è disponibile in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dfbef-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="dfbef-109">Il servizio partizioni COM+ non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dfbef-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="dfbef-110">Per utilizzare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) su true.</span><span class="sxs-lookup"><span data-stu-id="dfbef-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="dfbef-111">Per eseguire attività correlate alle partizioni, COM+ fornisce gli elementi di programmazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfbef-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="dfbef-112">Metodi e proprietà dell'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) nella classe [**COMAdminCatalog**](comadmincatalog.md) :</span><span class="sxs-lookup"><span data-stu-id="dfbef-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="dfbef-113">Proprietà [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="dfbef-114">Proprietà [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="dfbef-115">Proprietà [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="dfbef-116">Metodo [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="dfbef-117">Metodo [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="dfbef-118">Metodo [**Getpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="dfbef-119">Proprietà [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="dfbef-120">Set di oggetti COM+ per la creazione e la gestione di partizioni in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dfbef-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="dfbef-121">Chiave del registro di sistema COM+, **PartitionCache**, per la modifica delle dimensioni della cache della partizione.</span><span class="sxs-lookup"><span data-stu-id="dfbef-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="dfbef-122">Set di [raccolte di amministrazione com+](com--administration-collections.md)correlate alle partizioni:</span><span class="sxs-lookup"><span data-stu-id="dfbef-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="dfbef-123">Raccolta di [**partizioni**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-124">Raccolta [**PartitionUsers**](partitionusers.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-125">Raccolta [**RolesForPartition**](rolesforpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-126">Raccolta [**UsersInPartitionRole**](usersinpartitionrole.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="dfbef-127">Proprietà di altre [raccolte di amministrazione com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="dfbef-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="dfbef-128">Proprietà PartitionID nella raccolta [**ApplicationInstances**](applicationinstances.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-129">Proprietà AppPartitionID nella raccolta di [**applicazioni**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-130">Proprietà PartitionDescription, PartitionID e partitionName nella raccolta [**FilesForImport**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-131">Proprietà DSPartitionLookupEnabled, LocalPartitionLookupEnabled e PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-132">Proprietà EventClassPartitionID e SubscriberPartitionID nella raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="dfbef-133">Proprietà EventClassPartitionID e SubscriberPartitionID nella raccolta [**TransientSubscriptions**](transientsubscriptions.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbef-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfbef-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfbef-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfbef-135">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="dfbef-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="dfbef-136">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="dfbef-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="dfbef-137">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="dfbef-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="dfbef-138">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="dfbef-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="dfbef-139">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="dfbef-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="dfbef-140">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="dfbef-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



