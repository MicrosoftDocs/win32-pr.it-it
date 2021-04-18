---
description: La funzionalità partizioni COM+ include una cache di partizione. Questa cache archivia i mapping da utente a partizione ed è progettata per evitare l'accesso Active Directory ripetitivo.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurazione della cache della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305225"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="6e85e-104">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="6e85e-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="6e85e-105">La funzionalità partizioni COM+ include una cache di partizione.</span><span class="sxs-lookup"><span data-stu-id="6e85e-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="6e85e-106">Questa cache archivia i mapping da utente a partizione ed è progettata per evitare l'accesso Active Directory ripetitivo.</span><span class="sxs-lookup"><span data-stu-id="6e85e-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="6e85e-107">Modifica delle dimensioni della cache</span><span class="sxs-lookup"><span data-stu-id="6e85e-107">Changing Cache Size</span></span>

<span data-ttu-id="6e85e-108">La cache di partizione è costituita da tre tabelle, le cui dimensioni possono essere modificate per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6e85e-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="6e85e-109">Queste tabelle sono costituite dal numero di voci SID nella cache, dal numero di voci OU nella cache e dal numero di voci della partizione nella cache.</span><span class="sxs-lookup"><span data-stu-id="6e85e-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="6e85e-110">Per modificare le dimensioni della tabella, gli amministratori possono modificare i valori di una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6e85e-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="6e85e-111">La chiave del registro di sistema e i relativi valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e85e-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="6e85e-112">**HKLM \\ software \\ Microsoft \\ COM3 \\ PartitionCache**</span><span class="sxs-lookup"><span data-stu-id="6e85e-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="6e85e-113">Valori chiave</span><span class="sxs-lookup"><span data-stu-id="6e85e-113">Key values</span></span>                         | <span data-ttu-id="6e85e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e85e-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e85e-115">**NumSidEntries**</span><span class="sxs-lookup"><span data-stu-id="6e85e-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="6e85e-116">Contiene il \_ valore reg DWORD per il numero di voci SID nella cache (valore predefinito = 512).</span><span class="sxs-lookup"><span data-stu-id="6e85e-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="6e85e-117">Questo valore deve essere impostato su un valore maggiore del numero di identità univoche che un computer sarà in grado di gestire nell'intervallo di tempo di invalidamento della cache.</span><span class="sxs-lookup"><span data-stu-id="6e85e-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="6e85e-118">**NumNameEntries**</span><span class="sxs-lookup"><span data-stu-id="6e85e-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="6e85e-119">Contiene il \_ valore reg DWORD per il numero di voci di nome unità organizzativa nella cache (impostazione predefinita = 64).</span><span class="sxs-lookup"><span data-stu-id="6e85e-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="6e85e-120">Questo valore deve essere impostato su un valore maggiore del numero di nomi di unità organizzative univoci che un computer sarà in grado di gestire nell'intervallo di tempo di invalidamento della cache.</span><span class="sxs-lookup"><span data-stu-id="6e85e-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="6e85e-121">**NumPartitionEntries**</span><span class="sxs-lookup"><span data-stu-id="6e85e-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="6e85e-122">Contiene il \_ valore reg DWORD per il numero di voci della partizione nella cache (valore predefinito = 1024).</span><span class="sxs-lookup"><span data-stu-id="6e85e-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="6e85e-123">Nell'intervallo di tempo di invalidamento della cache, il valore DWORD deve essere impostato su un numero maggiore del numero di partizioni univoche che un computer sarà in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="6e85e-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="6e85e-124">Questo perché il contesto di un componente può includere un ID di partizione per una partizione che non risiede nel computer.</span><span class="sxs-lookup"><span data-stu-id="6e85e-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="6e85e-125">**EntryExpiration**</span><span class="sxs-lookup"><span data-stu-id="6e85e-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="6e85e-126">Contiene il \_ valore reg DWORD per il numero di cicli (ogni segno di indisponibilità = ~ 7 minuti) finché una voce della cache non diventa non valida (impostazione predefinita = 4 (~ 28 minuti)).</span><span class="sxs-lookup"><span data-stu-id="6e85e-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="6e85e-127">Scaricamento della cache</span><span class="sxs-lookup"><span data-stu-id="6e85e-127">Flushing the Cache</span></span>

<span data-ttu-id="6e85e-128">Poiché COM+ memorizza nella cache la partizione predefinita per gli utenti, potrebbe essere necessario chiamare questo metodo dopo aver modificato la partizione predefinita per un utente nel Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e85e-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="6e85e-129">Gli amministratori possono eseguire questa operazione a livello di codice chiamando il metodo [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="6e85e-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e85e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e85e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e85e-131">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="6e85e-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="6e85e-132">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="6e85e-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="6e85e-133">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="6e85e-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="6e85e-134">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="6e85e-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="6e85e-135">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="6e85e-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




