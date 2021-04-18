---
title: Glossario del file System proiettato di Windows
description: Termini speciali usati in ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/21/2020
ms.locfileid: "106299477"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="444a6-103">Glossario del file System proiettato di Windows</span><span class="sxs-lookup"><span data-stu-id="444a6-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="444a6-104">Termini speciali usati in ProjFS.</span><span class="sxs-lookup"><span data-stu-id="444a6-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="444a6-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Archivio di backup**</span><span class="sxs-lookup"><span data-stu-id="444a6-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-106">Dati gerarchici gestiti dal provider proiettati nella file system come file e directory.</span><span class="sxs-lookup"><span data-stu-id="444a6-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**segnaposto Dirty**</span><span class="sxs-lookup"><span data-stu-id="444a6-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-108">Un file o una directory che è stata modificata localmente e non è più una cache dello stato nell'archivio del provider.</span><span class="sxs-lookup"><span data-stu-id="444a6-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="444a6-109">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**file/directory completa**</span><span class="sxs-lookup"><span data-stu-id="444a6-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-111">Un file o una directory creata nel file system locale o un file che è stato modificato, rendendolo non più una cache dello stato nell'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="444a6-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="444a6-112">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**segnaposto idrato**</span><span class="sxs-lookup"><span data-stu-id="444a6-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-114">File il cui contenuto e metadati sono stati memorizzati nella cache su disco.</span><span class="sxs-lookup"><span data-stu-id="444a6-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="444a6-115">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**segnaposto**</span><span class="sxs-lookup"><span data-stu-id="444a6-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-117">Un file o una directory che non è completamente presente su disco.</span><span class="sxs-lookup"><span data-stu-id="444a6-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="444a6-118">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**rimozione definitiva**</span><span class="sxs-lookup"><span data-stu-id="444a6-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-120">Segnaposto nascosto speciale che rappresenta un elemento eliminato dalla file system locale.</span><span class="sxs-lookup"><span data-stu-id="444a6-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="444a6-121">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**file/directory virtuale**</span><span class="sxs-lookup"><span data-stu-id="444a6-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-123">Un file o una directory che non esiste fisicamente sul disco, ma viene proiettata in risultati di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="444a6-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="444a6-124">Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="444a6-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**istanza di virtualizzazione**</span><span class="sxs-lookup"><span data-stu-id="444a6-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-126">Oggetto in memoria che gestisce la comunicazione tra il provider e ProjFS per il set di file e directory che si trovano in una particolare radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="444a6-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="444a6-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**radice di virtualizzazione**</span><span class="sxs-lookup"><span data-stu-id="444a6-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="444a6-128">Una directory nella file system in cui vengono proiettati i dati del provider.</span><span class="sxs-lookup"><span data-stu-id="444a6-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->