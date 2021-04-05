---
title: Macro wrapper TraceLogging
description: Elenca le macro wrapper per i provider TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714152"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="6bb0c-103">Macro wrapper TraceLogging</span><span class="sxs-lookup"><span data-stu-id="6bb0c-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="6bb0c-104">Elenca le macro wrapper per i provider TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="6bb0c-105">Per registrare gli eventi usando i provider TraceLogging, è necessario usare le macro TraceLogging Write [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) o [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span><span class="sxs-lookup"><span data-stu-id="6bb0c-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="6bb0c-106">Per entrambe le macro è necessario eseguire il wrapping di tutti i dati degli eventi in una macro wrapper.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="6bb0c-107">Sono disponibili diverse macro wrapper per tipi di dati diversi.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="6bb0c-108">Per un elenco completo delle macro TraceLogging, vedere [macro TraceLogging](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="6bb0c-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="6bb0c-109">Oltre alle macro wrapper precedenti, sono disponibili diverse macro per i singoli tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="6bb0c-110">Tutte queste macro hanno lo stesso formato della macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) .</span><span class="sxs-lookup"><span data-stu-id="6bb0c-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="6bb0c-111">È possibile usare la macro TraceLoggingValue per rilevare automaticamente la macro wrapper appropriata da usare oppure usare direttamente la macro specifica.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="6bb0c-112">**TraceLoggingBinary**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="6bb0c-113">**TraceLoggingChannel**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="6bb0c-114">**TraceLoggingCustomAttribute**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="6bb0c-115">**TraceLoggingDescription**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="6bb0c-116">**TraceLoggingEventTag**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="6bb0c-117">**TraceLoggingKeyword**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="6bb0c-118">**TraceLoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="6bb0c-119">**TraceLoggingOpcode**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="6bb0c-120">**TraceLoggingSocketAddress**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="6bb0c-121">**TraceLoggingStruct**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="6bb0c-122">**TraceLoggingValue**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="6bb0c-123">**TraceLoggingOptionGroup** è specifico per l'uso all'interno \_ del \_ provider TRACELOGGING define.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="6bb0c-124">**TraceLoggingOptionGroup**</span><span class="sxs-lookup"><span data-stu-id="6bb0c-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="6bb0c-125">Ecco le singole macro wrapper.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="6bb0c-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="6bb0c-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="6bb0c-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="6bb0c-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="6bb0c-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="6bb0c-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="6bb0c-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="6bb0c-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="6bb0c-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="6bb0c-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="6bb0c-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="6bb0c-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="6bb0c-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="6bb0c-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="6bb0c-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="6bb0c-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="6bb0c-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="6bb0c-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="6bb0c-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="6bb0c-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="6bb0c-136">TraceLoggingBool</span><span class="sxs-lookup"><span data-stu-id="6bb0c-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="6bb0c-137">TraceLoggingFileTime</span><span class="sxs-lookup"><span data-stu-id="6bb0c-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="6bb0c-138">TraceLoggingGuid</span><span class="sxs-lookup"><span data-stu-id="6bb0c-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="6bb0c-139">TraceLoggingPointer</span><span class="sxs-lookup"><span data-stu-id="6bb0c-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="6bb0c-140">TraceLoggingSystemTime</span><span class="sxs-lookup"><span data-stu-id="6bb0c-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="6bb0c-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="6bb0c-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="6bb0c-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="6bb0c-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="6bb0c-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="6bb0c-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="6bb0c-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="6bb0c-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="6bb0c-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="6bb0c-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="6bb0c-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="6bb0c-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="6bb0c-147">TraceLoggingWchar</span><span class="sxs-lookup"><span data-stu-id="6bb0c-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="6bb0c-148">TraceLoggingChar</span><span class="sxs-lookup"><span data-stu-id="6bb0c-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="6bb0c-149">TraceLoggingIntPtr</span><span class="sxs-lookup"><span data-stu-id="6bb0c-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="6bb0c-150">TraceLoggingUIntPtr</span><span class="sxs-lookup"><span data-stu-id="6bb0c-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="6bb0c-151">TraceLoggingBoolean</span><span class="sxs-lookup"><span data-stu-id="6bb0c-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="6bb0c-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="6bb0c-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="6bb0c-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="6bb0c-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="6bb0c-154">TraceLoggingPid</span><span class="sxs-lookup"><span data-stu-id="6bb0c-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="6bb0c-155">TraceLoggingTid</span><span class="sxs-lookup"><span data-stu-id="6bb0c-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="6bb0c-156">TraceLoggingPort</span><span class="sxs-lookup"><span data-stu-id="6bb0c-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="6bb0c-157">TraceLoggingWinError</span><span class="sxs-lookup"><span data-stu-id="6bb0c-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="6bb0c-158">TraceLoggingNTStatus</span><span class="sxs-lookup"><span data-stu-id="6bb0c-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="6bb0c-159">TraceLoggingHResult</span><span class="sxs-lookup"><span data-stu-id="6bb0c-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="6bb0c-160">TraceLoggingSocketAddress</span><span class="sxs-lookup"><span data-stu-id="6bb0c-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="6bb0c-161">TraceLoggingSid</span><span class="sxs-lookup"><span data-stu-id="6bb0c-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="6bb0c-162">TraceLoggingString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-162">TraceLoggingString</span></span>

-   <span data-ttu-id="6bb0c-163">TraceLoggingWideString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="6bb0c-164">TraceLoggingCountedString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="6bb0c-165">TraceLoggingCountedWideString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="6bb0c-166">TraceLoggingAnsiString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="6bb0c-167">TraceLoggingUnicodeString</span><span class="sxs-lookup"><span data-stu-id="6bb0c-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="6bb0c-168">TraceLoggingBinary ( \* dati void, dimensioni dei dati in byte, \[ nome facoltativo \] ) i parametri della macro sono diversi da quelli precedenti.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="6bb0c-169">Se il parametro *Name* viene specificato, deve essere un valore letterale stringa (non una variabile) e non può contenere caratteri null incorporati.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="6bb0c-170">Se il parametro *Name* non viene specificato, viene generato automaticamente un nome.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="6bb0c-171">L'API TraceLogging rende disponibili anche diverse macro per le matrici.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="6bb0c-172">Queste matrici possono avere una lunghezza fissa o essere di lunghezza variabile, a seconda della macro del wrapper che si sceglie di usare.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="6bb0c-173">Tutte queste macro wrapper seguono questo formato.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="6bb0c-174">Il parametro *pVals* punta alla matrice di dati e *cVals* indica il numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="6bb0c-175">*cVals* deve essere una costante e non può essere una variabile.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="6bb0c-176">Analogamente alle macro wrapper per valore singolo, il *nome*, la **Descrizione** e i *tag* sono parametri facoltativi e devono seguire le stesse restrizioni illustrate con la macro **TraceLoggingValue** .</span><span class="sxs-lookup"><span data-stu-id="6bb0c-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="6bb0c-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="6bb0c-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="6bb0c-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="6bb0c-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="6bb0c-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="6bb0c-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="6bb0c-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="6bb0c-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="6bb0c-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="6bb0c-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="6bb0c-187">TraceLoggingBoolFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="6bb0c-188">TraceLoggingGuidFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="6bb0c-189">TraceLoggingPointerFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="6bb0c-190">TraceLoggingFileTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="6bb0c-191">TraceLoggingSystemTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="6bb0c-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="6bb0c-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="6bb0c-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="6bb0c-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="6bb0c-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="6bb0c-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="6bb0c-198">TraceLoggingWcharFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="6bb0c-199">TraceLoggingCharFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="6bb0c-200">TraceLoggingIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="6bb0c-201">TraceLoggingUIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="6bb0c-202">TraceLoggingBooleanFixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="6bb0c-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="6bb0c-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="6bb0c-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="6bb0c-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="6bb0c-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="6bb0c-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="6bb0c-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="6bb0c-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="6bb0c-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="6bb0c-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="6bb0c-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="6bb0c-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="6bb0c-215">TraceLoggingBoolArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="6bb0c-216">TraceLoggingGuidArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="6bb0c-217">TraceLoggingPointerArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="6bb0c-218">TraceLoggingFileTimeArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="6bb0c-219">TraceLoggingSystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="6bb0c-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="6bb0c-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="6bb0c-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="6bb0c-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="6bb0c-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="6bb0c-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="6bb0c-226">TraceLoggingWcharArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="6bb0c-227">TraceLoggingCharArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="6bb0c-228">TraceLoggingIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="6bb0c-229">TraceLoggingUIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="6bb0c-230">TraceLoggingBooleanArray</span><span class="sxs-lookup"><span data-stu-id="6bb0c-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="6bb0c-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="6bb0c-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="6bb0c-232">TraceLoggingHexUInt16Array</span></span>

 

 




