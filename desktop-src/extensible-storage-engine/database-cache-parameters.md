---
description: 'Altre informazioni su: parametri della cache del database'
title: Parametri della cache del database
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308552"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="0cc93-103">Parametri della cache del database</span><span class="sxs-lookup"><span data-stu-id="0cc93-103">Database Cache Parameters</span></span>


<span data-ttu-id="0cc93-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0cc93-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="0cc93-105">Parametri della cache del database</span><span class="sxs-lookup"><span data-stu-id="0cc93-105">Database Cache Parameters</span></span>

<span data-ttu-id="0cc93-106">Questo argomento contiene i parametri usati per la cache del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="0cc93-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="0cc93-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="0cc93-108">22</span><span class="sxs-lookup"><span data-stu-id="0cc93-108">22</span></span>  

<span data-ttu-id="0cc93-109">Questo parametro controlla la dimensione di una parte ausiliaria della cache delle pagine del database usata per simulare l'I/O della raccolta di dispersione quando non è disponibile in altro modo.</span><span class="sxs-lookup"><span data-stu-id="0cc93-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="0cc93-110">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-110">The size is in database pages.</span></span>

<span data-ttu-id="0cc93-111">**Windows XP e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-112">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-113">256</span><span class="sxs-lookup"><span data-stu-id="0cc93-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-114">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-115">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-116">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-117">0, 2 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="0cc93-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-118">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-119">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-120">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-121">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-122">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-123">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-124">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-125">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-126">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-127">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-128">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-129">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-130">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-131">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-132">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-133">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="0cc93-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="0cc93-135">41</span><span class="sxs-lookup"><span data-stu-id="0cc93-135">41</span></span>  

<span data-ttu-id="0cc93-136">Questo parametro può essere utilizzato per controllare le dimensioni della cache delle pagine del database in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0cc93-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="0cc93-137">In genere, la cache ne ottimizza automaticamente le dimensioni come funzione dei livelli di attività del database e del computer.</span><span class="sxs-lookup"><span data-stu-id="0cc93-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="0cc93-138">Se l'applicazione imposta questo parametro su zero, le dimensioni della cache vengono ottimizzate in questo modo.</span><span class="sxs-lookup"><span data-stu-id="0cc93-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="0cc93-139">Tuttavia, se l'applicazione imposta questo parametro su un valore diverso da zero, la cache si adatterà a tale dimensione di destinazione (nelle pagine del database).</span><span class="sxs-lookup"><span data-stu-id="0cc93-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="0cc93-140">La cache manterrà quindi le dimensioni a tale soglia fino a quando non vengono rilasciate nuove dimensioni o fino a quando non vengono rilasciate per scegliere le proprie dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0cc93-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="0cc93-141">**Nota**  Le dimensioni della cache sono comunque soggette ai limiti imposti da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="0cc93-142">Quando questo parametro viene letto, vengono restituite le dimensioni effettive della cache nelle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="0cc93-143">Questa dimensione può essere usata dall'applicazione come input per guidare la regolazione manuale della dimensione della cache.</span><span class="sxs-lookup"><span data-stu-id="0cc93-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-144">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-145">Speciali</span><span class="sxs-lookup"><span data-stu-id="0cc93-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-146">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-147">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-148">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-149"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="0cc93-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="0cc93-150"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-151">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-152">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-153">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-154">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-155">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-156">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-157">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-158">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-159">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-160">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-161">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-162">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-163">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-164">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-165">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-166">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="0cc93-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="0cc93-168">60</span><span class="sxs-lookup"><span data-stu-id="0cc93-168">60</span></span>  

<span data-ttu-id="0cc93-169">Questo parametro consente di configurare la dimensione minima della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="0cc93-170">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-170">The size is in database pages.</span></span>

<span data-ttu-id="0cc93-171">Per impostazione predefinita, le dimensioni della cache del database vengono regolate automaticamente tra i limiti impostati da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="0cc93-172">**Windows 2000:**  In Windows 2000, questo parametro deve essere impostato su un valore approssimativamente pari a quattro volte il numero di thread che saranno presenti all'interno dell'API ESE nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="0cc93-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="0cc93-173">Questa operazione è necessaria per evitare deadlock causati da un numero insufficiente di buffer della cache delle pagine del database per eseguire operazioni complesse come le divisioni dell'albero B +.</span><span class="sxs-lookup"><span data-stu-id="0cc93-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="0cc93-174">**Windows XP e versioni successive:**  Gestione cache imposterà automaticamente le dimensioni minime della cache per evitare deadlock.</span><span class="sxs-lookup"><span data-stu-id="0cc93-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-175">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-176"><strong>Windows 2000:</strong>  64</span><span class="sxs-lookup"><span data-stu-id="0cc93-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="0cc93-177"><strong>Windows XP:</strong>  1</span><span class="sxs-lookup"><span data-stu-id="0cc93-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-178">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-179">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-180">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-181"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="0cc93-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="0cc93-182"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-183">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-184">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-185">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-186"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="0cc93-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="0cc93-187"><strong>Windows XP:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-188">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-189"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="0cc93-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="0cc93-190"><strong>Windows XP:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-191">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-192">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-193">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-194">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-195">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-196">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-197">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-198">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-199">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-200">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="0cc93-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="0cc93-202">23</span><span class="sxs-lookup"><span data-stu-id="0cc93-202">23</span></span>  

<span data-ttu-id="0cc93-203">Questo parametro consente di configurare la dimensione massima della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="0cc93-204">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-204">The size is in database pages.</span></span>

<span data-ttu-id="0cc93-205">Per impostazione predefinita, le dimensioni della cache del database vengono regolate automaticamente tra i limiti impostati da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="0cc93-206">**Nota**   Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulle dimensioni della memoria fisica quando viene chiamato [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc93-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="0cc93-207">**Windows Vista:**  A partire da Windows Vista, il valore predefinito di questo parametro è stato modificato per chiarire questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="0cc93-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-208">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-209"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  512</span><span class="sxs-lookup"><span data-stu-id="0cc93-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="0cc93-210"><strong>Windows Vista:</strong>  2 miliardi</span><span class="sxs-lookup"><span data-stu-id="0cc93-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-211">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-212">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-213">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-214"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="0cc93-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="0cc93-215"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-216">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-217">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-218">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-219"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="0cc93-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="0cc93-220"><strong>Windows XP:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-221">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-222"><strong>Windows XP e windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="0cc93-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="0cc93-223"><strong>Windows Vista e Windows Server 2003:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-224">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-225">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-226">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-227">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-228">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-229">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-230">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-231">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-232">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-233">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="0cc93-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="0cc93-235">24</span><span class="sxs-lookup"><span data-stu-id="0cc93-235">24</span></span> 

<span data-ttu-id="0cc93-236">Questo parametro controlla il modo in cui le pagine del database vengono scaricate dalla cache delle pagine del database per ridurre al minimo il tempo necessario per il ripristino da un arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cc93-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="0cc93-237">Il parametro è una soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cc93-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="0cc93-238">Se la registrazione circolare è abilitata usando [JET_paramCircularLog](./transaction-log-parameters.md) , questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="0cc93-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="0cc93-239">È importante che il parametro non sia impostato su un livello troppo basso.</span><span class="sxs-lookup"><span data-stu-id="0cc93-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="0cc93-240">Poiché il valore di questo parametro si avvicina a zero, la cache diventa sempre più aggressiva quando si scaricano le pagine di database su disco.</span><span class="sxs-lookup"><span data-stu-id="0cc93-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="0cc93-241">In questo modo non solo si ottiene un numero maggiore di scritture nei file di database, ma anche indirettamente un numero maggiore di letture in tali file.</span><span class="sxs-lookup"><span data-stu-id="0cc93-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="0cc93-242">Questo può causare problemi di prestazioni molto significativi in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="0cc93-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="0cc93-243">Sfortunatamente, l'impostazione del valore ottimale più piccolo per questo parametro può essere eseguita solo usando la sperimentazione con l'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0cc93-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-244">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-245">20971520</span><span class="sxs-lookup"><span data-stu-id="0cc93-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-246">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-247">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-248">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-249"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="0cc93-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="0cc93-250"><strong>Windows Vista:</strong>  Tutti i valori</span><span class="sxs-lookup"><span data-stu-id="0cc93-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-251">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-252"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Questo parametro è globale.</span><span class="sxs-lookup"><span data-stu-id="0cc93-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="0cc93-253"><strong>Windows Vista:</strong>  Questo parametro è per istanza.</span><span class="sxs-lookup"><span data-stu-id="0cc93-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-254">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-255">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-256">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-257">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-258">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-259">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-260">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-261">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-262">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-263">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-264">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-265">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-266">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-267">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="0cc93-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="0cc93-269">135</span><span class="sxs-lookup"><span data-stu-id="0cc93-269">135</span></span>  

<span data-ttu-id="0cc93-270">Questo parametro controlla il numero massimo di scritture simultanee che verrà utilizzato dal motore di database per scaricare le pagine di database modificate allo scopo di avanzare il checkpoint.</span><span class="sxs-lookup"><span data-stu-id="0cc93-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="0cc93-271">Il valore di questo parametro può essere usato per bilanciare la velocità con cui il Checkpoint può essere avanzato rispetto all'impatto negativo che questo processo avrà sul tempo di risposta per le altre operazioni di I/O sui dischi che contengono il database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-272">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-273">96</span><span class="sxs-lookup"><span data-stu-id="0cc93-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-274">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-275">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-276">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-277">8-1024</span><span class="sxs-lookup"><span data-stu-id="0cc93-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-278">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-279">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-280">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-281">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-282">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-283">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-284">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-285">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-286">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-287">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-288">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-289">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-290">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-291">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-292">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-293">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="0cc93-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="0cc93-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="0cc93-295">127</span><span class="sxs-lookup"><span data-stu-id="0cc93-295">127</span></span>  

<span data-ttu-id="0cc93-296">Quando questo parametro è **true**, il motore di database utilizzerà i dati del database direttamente dalla cache dei file di Windows invece di copiare i dati memorizzati nella cache nella propria memoria privata.</span><span class="sxs-lookup"><span data-stu-id="0cc93-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="0cc93-297">Tutti i dati del database modificati verranno comunque memorizzati nella cache privata.</span><span class="sxs-lookup"><span data-stu-id="0cc93-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="0cc93-298">Lo scopo di questa modalità è ridurre ulteriormente la quantità di memoria privata utilizzata dal motore di database per memorizzare nella cache i dati del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="0cc93-299">La cache di visualizzazione può essere utilizzata solo se l'utilizzo della cache dei file di Windows viene abilitato impostando JET_paramEnableFileCache su **true**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-300">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-301">Falso</span><span class="sxs-lookup"><span data-stu-id="0cc93-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-302">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="0cc93-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-304">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-305">False, True</span><span class="sxs-lookup"><span data-stu-id="0cc93-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-306">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-307">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-308">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-309">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-310">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-311">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-312">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-313">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-314">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-315">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-316">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-317">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-318">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-319">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-320">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-321">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="0cc93-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="0cc93-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="0cc93-323">25</span><span class="sxs-lookup"><span data-stu-id="0cc93-323">25</span></span>  

<span data-ttu-id="0cc93-324">Questo parametro imposta l'intervallo di tempo in microsecondi rispetto al quale due accessi alle pagine del database sono considerati correlati.</span><span class="sxs-lookup"><span data-stu-id="0cc93-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="0cc93-325">Questo intervallo di correlazione controlla la riservatezza dell'algoritmo di sostituzione della pagina della cache (LRU-K) agli accessi successivi alle pagine.</span><span class="sxs-lookup"><span data-stu-id="0cc93-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="0cc93-326">Questo, a sua volta, avrà effetto sulle pagine che sceglie di memorizzare nella cache.</span><span class="sxs-lookup"><span data-stu-id="0cc93-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-327">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-328">128000</span><span class="sxs-lookup"><span data-stu-id="0cc93-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-329">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-330">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-331">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-332"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="0cc93-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="0cc93-333"><strong>Windows Vista:</strong>  Tutti i valori</span><span class="sxs-lookup"><span data-stu-id="0cc93-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-334">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-335">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-336">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-337">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-338">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-339">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-340">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-341">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-342">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-343">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-344">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-345">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-346">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-347">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-348">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-349">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="0cc93-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="0cc93-351">26</span><span class="sxs-lookup"><span data-stu-id="0cc93-351">26</span></span>  

<span data-ttu-id="0cc93-352">Questo parametro imposta il numero massimo di pagine del database non memorizzate nella cache per cui verranno conservati i tempi di accesso alle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="0cc93-353">Questi record della cronologia consentono all'algoritmo di sostituzione della pagina della cache (LRU-K) di rilevare più accuratamente le pagine popolari che sono state eliminate in modo errato dalla cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="0cc93-354">**Windows XP e Windows Server 2003:**  Questo parametro viene ignorato in Windows XP e Windows Server 2003 e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-355">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-356"><strong>Windows 2000:</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="0cc93-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="0cc93-357"><strong>Windows Vista:</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="0cc93-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-358">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-359">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-360">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-361"><strong>Windows 2000:</strong>  0 – 4194303</span><span class="sxs-lookup"><span data-stu-id="0cc93-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="0cc93-362"><strong>Windows Vista:</strong>  Tutti i valori</span><span class="sxs-lookup"><span data-stu-id="0cc93-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-363">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-364">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-365">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-366">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-367">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-368">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-369">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-370">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-371">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-372">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-373">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-374">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-375">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-376">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-377">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-378">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="0cc93-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="0cc93-380">27</span><span class="sxs-lookup"><span data-stu-id="0cc93-380">27</span></span>  

<span data-ttu-id="0cc93-381">Questo parametro configura il numero di accessi alle pagine del database considerati per determinare l'utilità della pagina.</span><span class="sxs-lookup"><span data-stu-id="0cc93-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="0cc93-382">Questo parametro è essenzialmente K in LRU-K, l'algoritmo di sostituzione della pagina della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-383">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-384">2</span><span class="sxs-lookup"><span data-stu-id="0cc93-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-385">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-386">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-387">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-388">Da 1 a 2</span><span class="sxs-lookup"><span data-stu-id="0cc93-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-389">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-390">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-391">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-392">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-393">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-394">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-395">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-396">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-397">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-398">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-399">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-400">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-401">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-402">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-403">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-404">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="0cc93-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="0cc93-406">28</span><span class="sxs-lookup"><span data-stu-id="0cc93-406">28</span></span>

<span data-ttu-id="0cc93-407">Questo parametro indica il periodo di tempo, in secondi, dopo il quale una pagina della cache delle pagine del database ha perso l'accesso a una pagina allo scopo di considerare l'utilità della pagina.</span><span class="sxs-lookup"><span data-stu-id="0cc93-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-408">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-409">100</span><span class="sxs-lookup"><span data-stu-id="0cc93-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-410">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-411">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-412">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-413"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="0cc93-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="0cc93-414"><strong>Windows Vista:</strong>   1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-415">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-416">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-417">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-418">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-419">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-420">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-421">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-422">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-423">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-424">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-425">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-426">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-427">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-428">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-429">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-430">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="0cc93-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="0cc93-432">29</span><span class="sxs-lookup"><span data-stu-id="0cc93-432">29</span></span>  

<span data-ttu-id="0cc93-433">Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="0cc93-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="0cc93-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="0cc93-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="0cc93-435">31</span><span class="sxs-lookup"><span data-stu-id="0cc93-435">31</span></span>  

<span data-ttu-id="0cc93-436">Questo parametro controlla quando la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="0cc93-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="0cc93-437">Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili.</span><span class="sxs-lookup"><span data-stu-id="0cc93-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="0cc93-438">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="0cc93-439">Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal **JET_paramStopFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="0cc93-440">L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0cc93-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="0cc93-441">Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere.</span><span class="sxs-lookup"><span data-stu-id="0cc93-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="0cc93-442">Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="0cc93-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-443">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-444"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="0cc93-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="0cc93-445"><strong>Windows Vista:</strong>  20 milioni (1%)</span><span class="sxs-lookup"><span data-stu-id="0cc93-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-446">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-447">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-448">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-449"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="0cc93-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="0cc93-450"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="0cc93-451"><strong>Windows Vista:</strong>  Tutti i valori</span><span class="sxs-lookup"><span data-stu-id="0cc93-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-452">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-453">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-454">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-455">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-456">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-457">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-458">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-459">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-460">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-461">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-462">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-463">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-464">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-465">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-466">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-467">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cc93-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="0cc93-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="0cc93-469">32</span><span class="sxs-lookup"><span data-stu-id="0cc93-469">32</span></span>  

<span data-ttu-id="0cc93-470">Questo parametro controlla quando la cache delle pagine del database termina la rimozione di pagine dalla cache per creare spazio per le pagine non memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="0cc93-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="0cc93-471">Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="0cc93-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="0cc93-472">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="0cc93-473">Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da **JET_paramStartFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="0cc93-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="0cc93-474">La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background.</span><span class="sxs-lookup"><span data-stu-id="0cc93-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="0cc93-475">Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate.</span><span class="sxs-lookup"><span data-stu-id="0cc93-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="0cc93-476">Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache della pagina del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="0cc93-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-477">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-478"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="0cc93-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="0cc93-479"><strong>Windows Vista:</strong>  40 milioni (2%)</span><span class="sxs-lookup"><span data-stu-id="0cc93-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-480">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0cc93-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-481">Integer</span><span class="sxs-lookup"><span data-stu-id="0cc93-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-482">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="0cc93-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-483"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="0cc93-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="0cc93-484"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="0cc93-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="0cc93-485"><strong>Windows Vista:</strong>  Tutti i valori</span><span class="sxs-lookup"><span data-stu-id="0cc93-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-486">Ambito:</span><span class="sxs-lookup"><span data-stu-id="0cc93-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-487">Globale</span><span class="sxs-lookup"><span data-stu-id="0cc93-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-488">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-489">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-490">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0cc93-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-491">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-492">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="0cc93-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-493">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-494">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-495">No</span><span class="sxs-lookup"><span data-stu-id="0cc93-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-496">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="0cc93-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-497">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-498">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="0cc93-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-499">Sì</span><span class="sxs-lookup"><span data-stu-id="0cc93-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-500">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="0cc93-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0cc93-501">Tutti</span><span class="sxs-lookup"><span data-stu-id="0cc93-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="0cc93-502">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cc93-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-503"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0cc93-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0cc93-504">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0cc93-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cc93-505"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0cc93-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0cc93-506">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0cc93-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cc93-507"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="0cc93-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0cc93-508">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="0cc93-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0cc93-509">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0cc93-509">See Also</span></span>

[<span data-ttu-id="0cc93-510">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0cc93-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0cc93-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="0cc93-511">JetInit</span></span>](./jetinit-function.md)
