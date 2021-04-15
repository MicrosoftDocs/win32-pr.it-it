---
description: Di seguito sono riportate le strutture file system distribuito DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Strutture di file system distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483772"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="f7624-103">Strutture di file system distribuito</span><span class="sxs-lookup"><span data-stu-id="f7624-103">Distributed File System Structures</span></span>

<span data-ttu-id="f7624-104">Di seguito sono riportate le strutture file system distribuito (DFS):</span><span class="sxs-lookup"><span data-stu-id="f7624-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f7624-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f7624-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f7624-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="f7624-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="f7624-107">Buffer di input utilizzato con il codice di controllo [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)</span><span class="sxs-lookup"><span data-stu-id="f7624-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="f7624-108">Struttura _DFS_INFO_1</span><span class="sxs-lookup"><span data-stu-id="f7624-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="f7624-109">Contiene il nome di una radice file system distribuito (DFS) o di un collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-110">Struttura _DFS_INFO_2</span><span class="sxs-lookup"><span data-stu-id="f7624-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="f7624-111">Contiene informazioni su una radice o un collegamento file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="f7624-112">Questa struttura contiene il nome, lo stato e il numero di destinazioni DFS per la radice o il collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-113">Struttura _DFS_INFO_3</span><span class="sxs-lookup"><span data-stu-id="f7624-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="f7624-114">Contiene informazioni su una radice o un collegamento file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="f7624-115">Questa struttura contiene il nome, lo stato, il numero di destinazioni DFS e le informazioni su ogni destinazione della radice o del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-116">Struttura _DFS_INFO_4</span><span class="sxs-lookup"><span data-stu-id="f7624-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="f7624-117">Contiene informazioni su una radice o un collegamento file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="f7624-118">Questa struttura contiene il nome, lo stato, il **GUID**, il timeout, il numero di destinazioni e le informazioni su ogni destinazione della radice o del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-119">Struttura _DFS_INFO_5</span><span class="sxs-lookup"><span data-stu-id="f7624-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="f7624-120">Contiene informazioni su una radice o un collegamento file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="f7624-121">Questa struttura contiene le proprietà nome, stato, **GUID**, timeout, spazio dei nomi/radice/collegamento, dimensione metadati e numero di destinazioni per la radice o il collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-122">Struttura _DFS_INFO_6</span><span class="sxs-lookup"><span data-stu-id="f7624-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="f7624-123">Contiene informazioni su una radice o un collegamento file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="f7624-124">Questa struttura contiene le proprietà nome, stato, **GUID**, timeout, spazio dei nomi/radice/collegamento, dimensione metadati, numero di destinazioni e informazioni su ogni destinazione della radice o del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-125">Struttura _DFS_INFO_7</span><span class="sxs-lookup"><span data-stu-id="f7624-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="f7624-126">Contiene informazioni su uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="f7624-127">Questa struttura contiene il **GUID** della versione per i metadati per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f7624-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-128">Struttura _DFS_INFO_8</span><span class="sxs-lookup"><span data-stu-id="f7624-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="f7624-129">Contiene il nome, lo stato, il **GUID**, il timeout, i flag delle proprietà, le dimensioni dei metadati, le informazioni di destinazione DFS e il descrittore di sicurezza del punto di analisi del collegamento per una radice o un collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-130">Struttura _DFS_INFO_9</span><span class="sxs-lookup"><span data-stu-id="f7624-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="f7624-131">Contiene il nome, lo stato, il **GUID**, il timeout, i flag delle proprietà, le dimensioni dei metadati, le informazioni di destinazione DFS, il descrittore di sicurezza del reparse point del collegamento e un elenco di destinazioni DFS per un collegamento o una radice.</span><span class="sxs-lookup"><span data-stu-id="f7624-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-132">Struttura _DFS_INFO_50</span><span class="sxs-lookup"><span data-stu-id="f7624-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="f7624-133">Contiene la versione dei metadati DFS e le funzionalità di uno spazio dei nomi DFS esistente.</span><span class="sxs-lookup"><span data-stu-id="f7624-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-134">Struttura _DFS_INFO_100</span><span class="sxs-lookup"><span data-stu-id="f7624-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="f7624-135">Contiene un commento associato a una radice file system distribuito (DFS) o a un collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-136">Struttura _DFS_INFO_101</span><span class="sxs-lookup"><span data-stu-id="f7624-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="f7624-137">Descrive lo stato di archiviazione in una radice DFS, un collegamento, una destinazione radice o una destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-138">Struttura _DFS_INFO_102</span><span class="sxs-lookup"><span data-stu-id="f7624-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="f7624-139">Contiene un valore di timeout da associare a una radice file system distribuito (DFS) o a un collegamento in una radice DFS denominata.</span><span class="sxs-lookup"><span data-stu-id="f7624-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-140">Struttura _DFS_INFO_103</span><span class="sxs-lookup"><span data-stu-id="f7624-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="f7624-141">Contiene proprietà che impostano comportamenti specifici per un collegamento o una radice DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-142">Struttura _DFS_INFO_104</span><span class="sxs-lookup"><span data-stu-id="f7624-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="f7624-143">Contiene la priorità di una destinazione radice DFS o di una destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-144">Struttura _DFS_INFO_105</span><span class="sxs-lookup"><span data-stu-id="f7624-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="f7624-145">Contiene informazioni su un collegamento o una radice DFS, inclusi il commento, lo stato, il timeout e i comportamenti DFS specificati dai flag della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7624-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-146">Struttura _DFS_INFO_106</span><span class="sxs-lookup"><span data-stu-id="f7624-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="f7624-147">Contiene lo stato di archiviazione e la priorità per una destinazione radice DFS o una destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="f7624-148">Questa struttura viene utilizzata solo con la funzione [**NetDfsSetInfo**](netdfssetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f7624-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-149">Struttura _DFS_INFO_107</span><span class="sxs-lookup"><span data-stu-id="f7624-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="f7624-150">Contiene informazioni su un collegamento o una radice DFS, inclusi il commento, lo stato, il timeout, i flag di proprietà e il descrittore di sicurezza del punto di analisi del collegamento.</span><span class="sxs-lookup"><span data-stu-id="f7624-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-151">Struttura _DFS_INFO_150</span><span class="sxs-lookup"><span data-stu-id="f7624-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="f7624-152">Contiene il descrittore di sicurezza per il punto di analisi di un collegamento DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-153">Struttura _DFS_INFO_200</span><span class="sxs-lookup"><span data-stu-id="f7624-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="f7624-154">Contiene il nome di uno spazio dei nomi di file system distribuito basato su dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="f7624-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-155">Struttura _DFS_INFO_300</span><span class="sxs-lookup"><span data-stu-id="f7624-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="f7624-156">Contiene il nome e il tipo (basati su dominio o autonomo) di uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-157">Struttura _DFS_STORAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="f7624-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="f7624-158">Contiene informazioni su una radice DFS o una destinazione del collegamento in uno spazio dei nomi DFS o dalla cache gestita dal client DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-159">Struttura _DFS_STORAGE_INFO_1</span><span class="sxs-lookup"><span data-stu-id="f7624-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="f7624-160">Contiene informazioni su una destinazione DFS, inclusi il nome del server di destinazione DFS e il nome della condivisione, nonché lo stato e la priorità della destinazione.</span><span class="sxs-lookup"><span data-stu-id="f7624-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-161">Struttura _DFS_SUPPORTED_NAMESPACE_VERSION_INFO</span><span class="sxs-lookup"><span data-stu-id="f7624-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="f7624-162">Contiene informazioni sulla versione per uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f7624-163">Struttura _DFS_TARGET_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="f7624-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="f7624-164">Contiene la classe di priorità e il rango di una specifica destinazione DFS.</span><span class="sxs-lookup"><span data-stu-id="f7624-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
