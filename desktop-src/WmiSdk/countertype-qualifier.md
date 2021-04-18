---
description: Il qualificatore CounterType contiene il valore integer per il tipo di contatore di proprietà per le proprietà nelle \_ classi PerfRawData Win32. CookingType contiene le costanti per i tipi di formule di proprietà nelle \_ classi PerfFormattedData Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificatore CounterType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310404"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="2fa9a-104">Qualificatore CounterType</span><span class="sxs-lookup"><span data-stu-id="2fa9a-104">CounterType Qualifier</span></span>

<span data-ttu-id="2fa9a-105">Il qualificatore **CounterType** contiene il valore integer per il tipo di contatore di proprietà per le proprietà nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="2fa9a-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="2fa9a-106">**CookingType** contiene le costanti per i tipi di formule di proprietà nelle classi [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="2fa9a-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="2fa9a-107">Per ulteriori informazioni e per una suddivisione dei tipi di contatore per funzione, vedere [tipi di contatori](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="2fa9a-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="2fa9a-108">CounterType</span><span class="sxs-lookup"><span data-stu-id="2fa9a-108">CounterType</span></span> | <span data-ttu-id="2fa9a-109">CookingType</span><span class="sxs-lookup"><span data-stu-id="2fa9a-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="2fa9a-110">0</span><span class="sxs-lookup"><span data-stu-id="2fa9a-110">0</span></span>           | <span data-ttu-id="2fa9a-111">\_ \_ RAWCOUNT Hex contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="2fa9a-112">256</span><span class="sxs-lookup"><span data-stu-id="2fa9a-112">256</span></span>         | <span data-ttu-id="2fa9a-113">\_ \_ \_ RAWCOUNT Hex contatore di grandi dimensioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="2fa9a-114">2816</span><span class="sxs-lookup"><span data-stu-id="2fa9a-114">2816</span></span>        | <span data-ttu-id="2fa9a-115">\_testo contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="2fa9a-116">65536</span><span class="sxs-lookup"><span data-stu-id="2fa9a-116">65536</span></span>       | <span data-ttu-id="2fa9a-117">\_RAWCOUNT contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="2fa9a-118">65792</span><span class="sxs-lookup"><span data-stu-id="2fa9a-118">65792</span></span>       | <span data-ttu-id="2fa9a-119">\_contatore prestazioni \_ RAWCOUNT di grandi dimensioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="2fa9a-120">73728</span><span class="sxs-lookup"><span data-stu-id="2fa9a-120">73728</span></span>       | <span data-ttu-id="2fa9a-121">PRESTAZIONI \_ doppie \_ RAW</span><span class="sxs-lookup"><span data-stu-id="2fa9a-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="2fa9a-122">4195328</span><span class="sxs-lookup"><span data-stu-id="2fa9a-122">4195328</span></span>     | <span data-ttu-id="2fa9a-123">\_Delta contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="2fa9a-124">4195584</span><span class="sxs-lookup"><span data-stu-id="2fa9a-124">4195584</span></span>     | <span data-ttu-id="2fa9a-125">\_Delta contatore prestazioni \_ elevate \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="2fa9a-126">4260864</span><span class="sxs-lookup"><span data-stu-id="2fa9a-126">4260864</span></span>     | <span data-ttu-id="2fa9a-127">\_contatore di esempio delle prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="2fa9a-128">4523008</span><span class="sxs-lookup"><span data-stu-id="2fa9a-128">4523008</span></span>     | <span data-ttu-id="2fa9a-129">\_tipo di \_ QUEUELEN del contatore delle prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="2fa9a-130">4523264</span><span class="sxs-lookup"><span data-stu-id="2fa9a-130">4523264</span></span>     | <span data-ttu-id="2fa9a-131">\_tipo di \_ QUEUELEN di grandi dimensioni contatore prestazioni \_ \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="2fa9a-132">5571840</span><span class="sxs-lookup"><span data-stu-id="2fa9a-132">5571840</span></span>     | <span data-ttu-id="2fa9a-133">\_ \_ \_ Tipo QUEUELEN del contatore delle prestazioni 100 NS \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="2fa9a-134">6620416</span><span class="sxs-lookup"><span data-stu-id="2fa9a-134">6620416</span></span>     | <span data-ttu-id="2fa9a-135">\_ \_ \_ \_ tipo QUEUELEN ora obj contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="2fa9a-136">272696320</span><span class="sxs-lookup"><span data-stu-id="2fa9a-136">272696320</span></span>   | <span data-ttu-id="2fa9a-137">contatore delle prestazioni \_ \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="2fa9a-138">272696576</span><span class="sxs-lookup"><span data-stu-id="2fa9a-138">272696576</span></span>   | <span data-ttu-id="2fa9a-139">\_ \_ conteggio bulk del contatore delle prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="2fa9a-140">537003008</span><span class="sxs-lookup"><span data-stu-id="2fa9a-140">537003008</span></span>   | <span data-ttu-id="2fa9a-141">\_frazione RAW \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="2fa9a-142">541132032</span><span class="sxs-lookup"><span data-stu-id="2fa9a-142">541132032</span></span>   | <span data-ttu-id="2fa9a-143">\_timer contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="2fa9a-144">541525248</span><span class="sxs-lookup"><span data-stu-id="2fa9a-144">541525248</span></span>   | <span data-ttu-id="2fa9a-145">\_timer di \_ sistema per precisione prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="2fa9a-146">542180608</span><span class="sxs-lookup"><span data-stu-id="2fa9a-146">542180608</span></span>   | <span data-ttu-id="2fa9a-147">\_Timer 100NSEC \_ perf</span><span class="sxs-lookup"><span data-stu-id="2fa9a-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="2fa9a-148">542573824</span><span class="sxs-lookup"><span data-stu-id="2fa9a-148">542573824</span></span>   | <span data-ttu-id="2fa9a-149">\_ \_ Timer 100 ns precisione \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="2fa9a-150">543229184</span><span class="sxs-lookup"><span data-stu-id="2fa9a-150">543229184</span></span>   | <span data-ttu-id="2fa9a-151">\_ \_ timer ora obj \_ perf</span><span class="sxs-lookup"><span data-stu-id="2fa9a-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="2fa9a-152">543622400</span><span class="sxs-lookup"><span data-stu-id="2fa9a-152">543622400</span></span>   | <span data-ttu-id="2fa9a-153">\_ \_ timer oggetto precisione \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="2fa9a-154">549585920</span><span class="sxs-lookup"><span data-stu-id="2fa9a-154">549585920</span></span>   | <span data-ttu-id="2fa9a-155">\_frazione campione \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="2fa9a-156">557909248</span><span class="sxs-lookup"><span data-stu-id="2fa9a-156">557909248</span></span>   | <span data-ttu-id="2fa9a-157">\_timer contatore \_ prestazioni \_ inv</span><span class="sxs-lookup"><span data-stu-id="2fa9a-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="2fa9a-158">558957824</span><span class="sxs-lookup"><span data-stu-id="2fa9a-158">558957824</span></span>   | <span data-ttu-id="2fa9a-159">\_Timer di 100NSEC Perf \_ \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="2fa9a-160">574686464</span><span class="sxs-lookup"><span data-stu-id="2fa9a-160">574686464</span></span>   | <span data-ttu-id="2fa9a-161">\_contatore prestazioni \_ \_ multitimer</span><span class="sxs-lookup"><span data-stu-id="2fa9a-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="2fa9a-162">575735040</span><span class="sxs-lookup"><span data-stu-id="2fa9a-162">575735040</span></span>   | <span data-ttu-id="2fa9a-163">PRESTAZIONI \_ 100NSEC \_ \_ multitimer</span><span class="sxs-lookup"><span data-stu-id="2fa9a-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="2fa9a-164">591463680</span><span class="sxs-lookup"><span data-stu-id="2fa9a-164">591463680</span></span>   | <span data-ttu-id="2fa9a-165">\_contatore delle \_ prestazioni \_ multitimer \_ inv</span><span class="sxs-lookup"><span data-stu-id="2fa9a-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="2fa9a-166">592512256</span><span class="sxs-lookup"><span data-stu-id="2fa9a-166">592512256</span></span>   | <span data-ttu-id="2fa9a-167">PERF \_ 100NSEC \_ \_ multitimer \_ inv</span><span class="sxs-lookup"><span data-stu-id="2fa9a-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="2fa9a-168">805438464</span><span class="sxs-lookup"><span data-stu-id="2fa9a-168">805438464</span></span>   | <span data-ttu-id="2fa9a-169">\_timer medio \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="2fa9a-170">807666944</span><span class="sxs-lookup"><span data-stu-id="2fa9a-170">807666944</span></span>   | <span data-ttu-id="2fa9a-171">\_tempo trascorso prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="2fa9a-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="2fa9a-172">1073742336</span></span>  | <span data-ttu-id="2fa9a-173">contatori delle prestazioni \_ \_ NoData</span><span class="sxs-lookup"><span data-stu-id="2fa9a-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="2fa9a-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="2fa9a-174">1073874176</span></span>  | <span data-ttu-id="2fa9a-175">media prestazioni in \_ \_ blocco</span><span class="sxs-lookup"><span data-stu-id="2fa9a-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="2fa9a-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="2fa9a-176">1073939457</span></span>  | <span data-ttu-id="2fa9a-177">\_base di esempio delle prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="2fa9a-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="2fa9a-178">1073939458</span></span>  | <span data-ttu-id="2fa9a-179">\_base media \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="2fa9a-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="2fa9a-180">1073939459</span></span>  | <span data-ttu-id="2fa9a-181">\_base prestazioni raw \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="2fa9a-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="2fa9a-182">1073939712</span></span>  | <span data-ttu-id="2fa9a-183">\_timestamp precisione \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="2fa9a-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="2fa9a-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="2fa9a-184">1073939715</span></span>  | <span data-ttu-id="2fa9a-185">\_ \_ base grezza per prestazioni elevate \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="2fa9a-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="2fa9a-186">1107494144</span></span>  | <span data-ttu-id="2fa9a-187">\_contatori delle \_ prestazioni \_ multibase</span><span class="sxs-lookup"><span data-stu-id="2fa9a-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="2fa9a-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="2fa9a-188">2147483648</span></span>  | <span data-ttu-id="2fa9a-189">\_tipo di \_ istogramma del contatore delle prestazioni \_</span><span class="sxs-lookup"><span data-stu-id="2fa9a-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="2fa9a-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fa9a-190">Requirements</span></span>



| <span data-ttu-id="2fa9a-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa9a-191">Requirement</span></span> | <span data-ttu-id="2fa9a-192">Valore</span><span class="sxs-lookup"><span data-stu-id="2fa9a-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2fa9a-193">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa9a-193">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa9a-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fa9a-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2fa9a-195">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa9a-195">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa9a-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fa9a-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2fa9a-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fa9a-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa9a-198">Qualificatori specifici delle classi di prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="2fa9a-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

