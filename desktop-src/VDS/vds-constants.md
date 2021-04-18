---
description: Costanti VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Costanti VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318208"
---
# <a name="vds-constants"></a><span data-ttu-id="1de8c-103">Costanti VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-103">VDS Constants</span></span>

<span data-ttu-id="1de8c-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1de8c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1de8c-105">Le costanti VDS sono classificate come segue:</span><span class="sxs-lookup"><span data-stu-id="1de8c-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="1de8c-106">Costanti di stato dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="1de8c-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="1de8c-107">Costanti degli hint di automagic</span><span class="sxs-lookup"><span data-stu-id="1de8c-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="1de8c-108">Costanti varie</span><span class="sxs-lookup"><span data-stu-id="1de8c-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="1de8c-109">Costanti di stato dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="1de8c-109">Object Status Constants</span></span>



| <span data-ttu-id="1de8c-110">Costante</span><span class="sxs-lookup"><span data-stu-id="1de8c-110">Constant</span></span>           | <span data-ttu-id="1de8c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1de8c-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="1de8c-112">STATO \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="1de8c-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="1de8c-113">0</span><span class="sxs-lookup"><span data-stu-id="1de8c-113">0</span></span>     |
| <span data-ttu-id="1de8c-114">STATO \_ online</span><span class="sxs-lookup"><span data-stu-id="1de8c-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="1de8c-115">1</span><span class="sxs-lookup"><span data-stu-id="1de8c-115">1</span></span>     |
| <span data-ttu-id="1de8c-116">STATO \_ non \_ pronto</span><span class="sxs-lookup"><span data-stu-id="1de8c-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="1de8c-117">2</span><span class="sxs-lookup"><span data-stu-id="1de8c-117">2</span></span>     |
| <span data-ttu-id="1de8c-118">STATO \_ nessun \_ supporto</span><span class="sxs-lookup"><span data-stu-id="1de8c-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="1de8c-119">3</span><span class="sxs-lookup"><span data-stu-id="1de8c-119">3</span></span>     |
| <span data-ttu-id="1de8c-120">STATO \_ offline</span><span class="sxs-lookup"><span data-stu-id="1de8c-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="1de8c-121">4</span><span class="sxs-lookup"><span data-stu-id="1de8c-121">4</span></span>     |
| <span data-ttu-id="1de8c-122">STATO \_ non riuscito</span><span class="sxs-lookup"><span data-stu-id="1de8c-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="1de8c-123">5</span><span class="sxs-lookup"><span data-stu-id="1de8c-123">5</span></span>     |
| <span data-ttu-id="1de8c-124">STATO \_ mancante</span><span class="sxs-lookup"><span data-stu-id="1de8c-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="1de8c-125">6</span><span class="sxs-lookup"><span data-stu-id="1de8c-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="1de8c-126">Costanti degli hint di automagic</span><span class="sxs-lookup"><span data-stu-id="1de8c-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="1de8c-127">Costante</span><span class="sxs-lookup"><span data-stu-id="1de8c-127">Constant</span></span>                               | <span data-ttu-id="1de8c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1de8c-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="1de8c-129">\_MOSTLYREADS hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="1de8c-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="1de8c-130">0x0002L</span></span> |
| <span data-ttu-id="1de8c-131">\_OPTIMIZEFORSEQUENTIALREADS hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="1de8c-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="1de8c-132">0x0004L</span></span> |
| <span data-ttu-id="1de8c-133">\_OPTIMIZEFORSEQUENTIALWRITES hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="1de8c-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="1de8c-134">0x0008L</span></span> |
| <span data-ttu-id="1de8c-135">\_REMAPENABLED hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="1de8c-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="1de8c-136">0x0020L</span></span> |
| <span data-ttu-id="1de8c-137">\_WRITETHROUGHCACHINGENABLED hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="1de8c-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="1de8c-138">0x0040L</span></span> |
| <span data-ttu-id="1de8c-139">\_HARDWARECHECKSUMENABLED hint \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="1de8c-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="1de8c-140">0x0080L</span></span> |
| <span data-ttu-id="1de8c-141">HINT VDS che è stato \_ \_ ritirato</span><span class="sxs-lookup"><span data-stu-id="1de8c-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="1de8c-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="1de8c-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="1de8c-143">Costanti varie</span><span class="sxs-lookup"><span data-stu-id="1de8c-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="1de8c-144">Costante</span><span class="sxs-lookup"><span data-stu-id="1de8c-144">Constant</span></span>                     | <span data-ttu-id="1de8c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="1de8c-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="1de8c-146">\_min priorità di ricompilazione VDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="1de8c-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="1de8c-147">0x0001L</span></span>    |
| <span data-ttu-id="1de8c-148">\_ \_ informazioni lun versione \_ VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="1de8c-149">1</span><span class="sxs-lookup"><span data-stu-id="1de8c-149">1</span></span>          |
| <span data-ttu-id="1de8c-150">\_lunghezza max ComputerName \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="1de8c-151">15</span><span class="sxs-lookup"><span data-stu-id="1de8c-151">15</span></span>         |
| <span data-ttu-id="1de8c-152">\_lunghezza massima ProviderName \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="1de8c-153">200</span><span class="sxs-lookup"><span data-stu-id="1de8c-153">200</span></span>        |
| <span data-ttu-id="1de8c-154">\_lunghezza massima VERSIONSTRING \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="1de8c-155">16</span><span class="sxs-lookup"><span data-stu-id="1de8c-155">16</span></span>         |
| <span data-ttu-id="1de8c-156">\_prop lettera di unità \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="1de8c-157">N/D</span><span class="sxs-lookup"><span data-stu-id="1de8c-157">N/A</span></span>        |
| <span data-ttu-id="1de8c-158">dimensioni MASSIMe del \_ \_ nome FS \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="1de8c-159">8</span><span class="sxs-lookup"><span data-stu-id="1de8c-159">8</span></span>          |
| <span data-ttu-id="1de8c-160">il \_ membro IDX non è valido \_</span><span class="sxs-lookup"><span data-stu-id="1de8c-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="1de8c-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1de8c-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="1de8c-162">\_ \_ lunghezza nome partizione \_ GPT</span><span class="sxs-lookup"><span data-stu-id="1de8c-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="1de8c-163">36</span><span class="sxs-lookup"><span data-stu-id="1de8c-163">36</span></span>         |
| <span data-ttu-id="1de8c-164">\_percorso massimo</span><span class="sxs-lookup"><span data-stu-id="1de8c-164">MAX\_PATH</span></span>                    | <span data-ttu-id="1de8c-165">260</span><span class="sxs-lookup"><span data-stu-id="1de8c-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1de8c-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1de8c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de8c-167">Riferimento VDS</span><span class="sxs-lookup"><span data-stu-id="1de8c-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
