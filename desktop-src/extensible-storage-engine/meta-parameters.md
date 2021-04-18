---
description: 'Altre informazioni su: meta Parameters'
title: Meta parametri
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306206"
---
# <a name="meta-parameters"></a><span data-ttu-id="3db3c-103">Meta parametri</span><span class="sxs-lookup"><span data-stu-id="3db3c-103">Meta Parameters</span></span>


<span data-ttu-id="3db3c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3db3c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="3db3c-105">Meta parametri</span><span class="sxs-lookup"><span data-stu-id="3db3c-105">Meta Parameters</span></span>

<span data-ttu-id="3db3c-106">Questo argomento contiene i parametri usati per controllare altri parametri.</span><span class="sxs-lookup"><span data-stu-id="3db3c-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="3db3c-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="3db3c-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="3db3c-108">129</span><span class="sxs-lookup"><span data-stu-id="3db3c-108">129</span></span>  
<span data-ttu-id="3db3c-109">Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="3db3c-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="3db3c-110">Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione.</span><span class="sxs-lookup"><span data-stu-id="3db3c-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="3db3c-111">Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="3db3c-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="3db3c-112">Inoltre, il parametro stesso può avere altri effetti sul comportamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="3db3c-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="3db3c-113">A questo punto, sono disponibili due configurazioni supportate:</span><span class="sxs-lookup"><span data-stu-id="3db3c-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="3db3c-114">Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.</span><span class="sxs-lookup"><span data-stu-id="3db3c-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="3db3c-115">Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.</span><span class="sxs-lookup"><span data-stu-id="3db3c-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="3db3c-116">Small Configuration modifica le impostazioni predefinite dei seguenti parametri di sistema con i valori specificati:</span><span class="sxs-lookup"><span data-stu-id="3db3c-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3db3c-117">Parametro di sistema</span><span class="sxs-lookup"><span data-stu-id="3db3c-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="3db3c-118">Nuovo valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3db3c-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="3db3c-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="3db3c-120">30000</span><span class="sxs-lookup"><span data-stu-id="3db3c-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="3db3c-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="3db3c-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="3db3c-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="3db3c-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="3db3c-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="3db3c-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="3db3c-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="3db3c-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="3db3c-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="3db3c-130">64</span><span class="sxs-lookup"><span data-stu-id="3db3c-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="3db3c-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="3db3c-132">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="3db3c-134">16</span><span class="sxs-lookup"><span data-stu-id="3db3c-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="3db3c-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="3db3c-136">14</span><span class="sxs-lookup"><span data-stu-id="3db3c-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="3db3c-138">16</span><span class="sxs-lookup"><span data-stu-id="3db3c-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="3db3c-140">65536</span><span class="sxs-lookup"><span data-stu-id="3db3c-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="3db3c-142">10</span><span class="sxs-lookup"><span data-stu-id="3db3c-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="3db3c-144">16</span><span class="sxs-lookup"><span data-stu-id="3db3c-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="3db3c-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="3db3c-146">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="3db3c-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="3db3c-148">2</span><span class="sxs-lookup"><span data-stu-id="3db3c-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="3db3c-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="3db3c-150">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="3db3c-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="3db3c-152">16</span><span class="sxs-lookup"><span data-stu-id="3db3c-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="3db3c-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="3db3c-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="3db3c-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="3db3c-156">0</span><span class="sxs-lookup"><span data-stu-id="3db3c-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="3db3c-158">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="3db3c-160">32</span><span class="sxs-lookup"><span data-stu-id="3db3c-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="3db3c-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="3db3c-162">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="3db3c-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="3db3c-164">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="3db3c-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="3db3c-166">1</span><span class="sxs-lookup"><span data-stu-id="3db3c-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="3db3c-168">1024</span><span class="sxs-lookup"><span data-stu-id="3db3c-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="3db3c-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="3db3c-170">0</span><span class="sxs-lookup"><span data-stu-id="3db3c-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="3db3c-172">8</span><span class="sxs-lookup"><span data-stu-id="3db3c-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3db3c-173">La configurazione di piccole dimensioni ha anche diversi altri effetti sul motore di database, tra cui:</span><span class="sxs-lookup"><span data-stu-id="3db3c-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="3db3c-174">Tutte le risorse gestite dai parametri di sistema vengono allocate dall'heap in base alle esigenze</span><span class="sxs-lookup"><span data-stu-id="3db3c-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="3db3c-175">Le altre risorse interne usate dal motore di database vengono ridimensionate</span><span class="sxs-lookup"><span data-stu-id="3db3c-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="3db3c-176">Diverse attività di manutenzione vengono ridimensionate per evitare attività dei thread in background</span><span class="sxs-lookup"><span data-stu-id="3db3c-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-177">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="3db3c-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-178">1 (legacy)</span><span class="sxs-lookup"><span data-stu-id="3db3c-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-179">Digitare:</span><span class="sxs-lookup"><span data-stu-id="3db3c-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-180">Integer</span><span class="sxs-lookup"><span data-stu-id="3db3c-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-181">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="3db3c-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="3db3c-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-183">Ambito:</span><span class="sxs-lookup"><span data-stu-id="3db3c-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-184">Istanza</span><span class="sxs-lookup"><span data-stu-id="3db3c-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-185">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="3db3c-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-186">Sì</span><span class="sxs-lookup"><span data-stu-id="3db3c-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-187">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="3db3c-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-188">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-189">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="3db3c-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-190">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-191">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="3db3c-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-192">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-193">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="3db3c-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-194">Sì</span><span class="sxs-lookup"><span data-stu-id="3db3c-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-195">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="3db3c-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-196">Sì</span><span class="sxs-lookup"><span data-stu-id="3db3c-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-197">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="3db3c-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-198">A partire da Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3db3c-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3db3c-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="3db3c-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="3db3c-200">130</span><span class="sxs-lookup"><span data-stu-id="3db3c-200">130</span></span>  
<span data-ttu-id="3db3c-201">Questo parametro viene utilizzato per controllare quando il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="3db3c-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="3db3c-202">Questo parametro viene utilizzato in combinazione con JET_paramConfiguration per impedire l'impostazione di alcuni parametri di sistema dalle impostazioni predefinite della configurazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="3db3c-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="3db3c-203">I parametri di sistema seguenti verranno protetti dall'impostazione quando questo parametro è impostato su false:</span><span class="sxs-lookup"><span data-stu-id="3db3c-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="3db3c-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="3db3c-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="3db3c-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="3db3c-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="3db3c-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="3db3c-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="3db3c-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="3db3c-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="3db3c-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="3db3c-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="3db3c-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="3db3c-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="3db3c-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="3db3c-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="3db3c-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="3db3c-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="3db3c-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="3db3c-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="3db3c-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="3db3c-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="3db3c-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="3db3c-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="3db3c-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="3db3c-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="3db3c-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="3db3c-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="3db3c-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="3db3c-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="3db3c-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="3db3c-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="3db3c-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="3db3c-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="3db3c-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="3db3c-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="3db3c-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="3db3c-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="3db3c-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="3db3c-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="3db3c-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="3db3c-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="3db3c-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="3db3c-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="3db3c-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="3db3c-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="3db3c-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="3db3c-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="3db3c-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="3db3c-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="3db3c-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="3db3c-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="3db3c-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="3db3c-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="3db3c-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="3db3c-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="3db3c-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="3db3c-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="3db3c-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="3db3c-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="3db3c-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="3db3c-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="3db3c-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="3db3c-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="3db3c-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="3db3c-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-244">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="3db3c-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-245">Vero</span><span class="sxs-lookup"><span data-stu-id="3db3c-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-246">Digitare:</span><span class="sxs-lookup"><span data-stu-id="3db3c-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="3db3c-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-248">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="3db3c-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-249">False, True</span><span class="sxs-lookup"><span data-stu-id="3db3c-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-250">Ambito:</span><span class="sxs-lookup"><span data-stu-id="3db3c-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-251">Istanza</span><span class="sxs-lookup"><span data-stu-id="3db3c-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-252">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="3db3c-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-253">Sì</span><span class="sxs-lookup"><span data-stu-id="3db3c-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-254">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="3db3c-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-255">Sì</span><span class="sxs-lookup"><span data-stu-id="3db3c-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-256">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="3db3c-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-257">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-258">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="3db3c-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-259">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-260">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="3db3c-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-261">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-262">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="3db3c-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-263">No</span><span class="sxs-lookup"><span data-stu-id="3db3c-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-264">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="3db3c-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3db3c-265">A partire da Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3db3c-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="3db3c-266">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3db3c-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-267"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3db3c-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3db3c-268">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3db3c-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db3c-269"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3db3c-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3db3c-270">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3db3c-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db3c-271"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3db3c-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3db3c-272">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3db3c-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3db3c-273">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3db3c-273">See Also</span></span>

[<span data-ttu-id="3db3c-274">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="3db3c-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="3db3c-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="3db3c-275">JetInit</span></span>](./jetinit-function.md)
