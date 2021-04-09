---
description: 'Altre informazioni su: parametri del database'
title: Parametri del database
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130199"
---
# <a name="database-parameters"></a><span data-ttu-id="c1fe2-103">Parametri del database</span><span class="sxs-lookup"><span data-stu-id="c1fe2-103">Database Parameters</span></span>


<span data-ttu-id="c1fe2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c1fe2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="c1fe2-105">Parametri del database</span><span class="sxs-lookup"><span data-stu-id="c1fe2-105">Database Parameters</span></span>

<span data-ttu-id="c1fe2-106">Questo argomento contiene i parametri usati per il database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="c1fe2-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="c1fe2-108">44</span><span class="sxs-lookup"><span data-stu-id="c1fe2-108">44</span></span>  

<span data-ttu-id="c1fe2-109">Questo parametro, se impostato, comporterà la restituzione di un errore speciale da parte di [JetInit](./jetinit-function.md) quando viene aperto un database o un log delle transazioni di una versione precedente del motore di database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="c1fe2-110">Questi errori sono:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1fe2-111">Errore</span><span class="sxs-lookup"><span data-stu-id="c1fe2-111">Error</span></span></p></th>
<th><p><span data-ttu-id="c1fe2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1fe2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="c1fe2-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-114">I file di database e/o di log delle transazioni sono stati creati con il motore di database in Windows NT 3,51.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="c1fe2-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-116">I file di database e/o di log delle transazioni sono stati creati con il motore di database in una versione di prova precedente a Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="c1fe2-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-118">I file di database e/o di log delle transazioni sono stati creati con il motore di database in Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-119">**Windows Vista:**  Per Windows Vista e versioni successive, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-120">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-121">Vero</span><span class="sxs-lookup"><span data-stu-id="c1fe2-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-122">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-124">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-125">False, True</span><span class="sxs-lookup"><span data-stu-id="c1fe2-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-126">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-127">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-128">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-129">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-130">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-131">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-132">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-133">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-134">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-135">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-136">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-137">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-138">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-139">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-140">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-141">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="c1fe2-143">64</span><span class="sxs-lookup"><span data-stu-id="c1fe2-143">64</span></span>  

<span data-ttu-id="c1fe2-144">Questo parametro consente di configurare le dimensioni della pagina per il database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="c1fe2-145">La dimensione della pagina è la più piccola unità di allocazione dello spazio possibile per un file di database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="c1fe2-146">Anche le dimensioni della pagina del database sono molto importanti perché imposta il limite superiore per le dimensioni di un singolo record nel database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="c1fe2-147">**Nota** Al momento è supportata una sola dimensione della pagina del database per processo.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="c1fe2-148">Ciò significa che se ci si trova in un singolo processo che contiene applicazioni diverse che usano il motore di database, è necessario che tutti condividano le dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-149">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-150">4096</span><span class="sxs-lookup"><span data-stu-id="c1fe2-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-151">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-152">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-153">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="c1fe2-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-155">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-156">Globale</span><span class="sxs-lookup"><span data-stu-id="c1fe2-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-157">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-158">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-159">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-160">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-161">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-162">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-163">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-164">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-165">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-166">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-167">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-168">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-169">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-170">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="c1fe2-172">18</span><span class="sxs-lookup"><span data-stu-id="c1fe2-172">18</span></span>  

<span data-ttu-id="c1fe2-173">Questo parametro controlla la quantità di spazio che viene aggiunta a un file di database ogni volta che deve espandersi per contenere più dati.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="c1fe2-174">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-175">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-176">256</span><span class="sxs-lookup"><span data-stu-id="c1fe2-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-177">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-178">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-179">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-180">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1fe2-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-181">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-182">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-183">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-184">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-185">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-186">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-186">No</span></span></p>
<p><span data-ttu-id="c1fe2-187"><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-188">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-189">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-190">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-191">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-192">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-193">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-194">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-195">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-196">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-197">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="c1fe2-199">45</span><span class="sxs-lookup"><span data-stu-id="c1fe2-199">45</span></span>  

<span data-ttu-id="c1fe2-200">Quando questo parametro è impostato su true, ogni database viene controllato in fase di [JetAttachDatabase](./jetattachdatabase-function.md) per gli indici delle colonne chiave Unicode compilate con una versione precedente della libreria NLS nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="c1fe2-201">Questa operazione deve essere eseguita poiché il motore di database rende permanente le chiavi di ordinamento generate da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e il valore di queste chiavi di ordinamento viene modificato da release a Release.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="c1fe2-202">Se viene rilevato un indice primario in questo stato, [JetAttachDatabase](./jetattachdatabase-function.md) avrà sempre esito negativo con JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="c1fe2-203">Se vengono rilevati indici secondari in questo stato, esistono due possibili risultati.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="c1fe2-204">Se JET_bitDbDeleteCorruptIndexes è stato passato a [JetAttachDatabase](./jetattachdatabase-function.md) , questi indici verranno eliminati e JET_wrnCorruptIndexDeleted verranno restituiti da [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1fe2-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="c1fe2-205">Questi indici dovranno essere ricreati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="c1fe2-206">Se JET_bitDbDeleteCorruptIndexes non è stato passato a [JetAttachDatabase](./jetattachdatabase-function.md) , la chiamata avrà esito negativo con JET_errSecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="c1fe2-207">**Nota** Si consiglia vivamente di impostare questo parametro su true dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="c1fe2-208">**Nota** Si consiglia vivamente alle applicazioni di evitare l'utilizzo di colonne chiave Unicode negli indici di chiave primaria (cluster).</span><span class="sxs-lookup"><span data-stu-id="c1fe2-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-209">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fe2-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-211">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-213">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-214">False, True</span><span class="sxs-lookup"><span data-stu-id="c1fe2-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-215">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-216">Globale</span><span class="sxs-lookup"><span data-stu-id="c1fe2-216">Global</span></span></p>
<p><span data-ttu-id="c1fe2-217"><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-218">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-219">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-220">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-221">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-222">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-223">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-224">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-225">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-226">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-227">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-228">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-229">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-230">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-231">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="c1fe2-233">54</span><span class="sxs-lookup"><span data-stu-id="c1fe2-233">54</span></span>  

<span data-ttu-id="c1fe2-234">Quando questo parametro è impostato su true, il motore di database può eseguire automaticamente la pulizia degli indici sulle colonne chiave Unicode in [JetInit](./jetinit-function.md) momento, in base alle esigenze, per evitare modifiche al formato del database causate dalle modifiche apportate alla libreria NLS in Windows.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="c1fe2-235">Tali modifiche vengono apportate regolarmente alla libreria NLS per aggiungere il supporto per nuove lingue, per aggiungere caratteri mancanti a una lingua, per aggiungere un ordine delle regole di confronto a una lingua o per correggere i bug nell'ordine delle regole di confronto di una lingua.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="c1fe2-236">Queste modifiche interessano le chiavi di ordinamento prodotte da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) , che vengono rese permanente dal motore di database come componenti delle chiavi di indice.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="c1fe2-237">È importante tenere presente che è possibile che le modifiche apportate all'indice siano così eccezionali che non è possibile eseguire una pulizia incrementale.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="c1fe2-238">In questo caso, l'indice verrà gestito come previsto dal **JET_paramEnableIndexChecking**.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="c1fe2-239">**Nota** Si consiglia vivamente che questo parametro e **JET_paramEnableIndexChecking** siano impostati su **true** dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-240">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-241">Vero</span><span class="sxs-lookup"><span data-stu-id="c1fe2-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-242">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-244">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-245">False, True</span><span class="sxs-lookup"><span data-stu-id="c1fe2-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-246">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-247">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-248">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-249">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-250">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-251">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-251">No</span></span></p>
<p><span data-ttu-id="c1fe2-252"><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-253">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-254">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-255">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-256">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-257">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-258">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-259">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-260">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-261">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-262">Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="c1fe2-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="c1fe2-264">102</span><span class="sxs-lookup"><span data-stu-id="c1fe2-264">102</span></span>  

<span data-ttu-id="c1fe2-265">Quando questo parametro è true, è possibile aprire un solo database usando [JetOpenDatabase](./jetopendatabase-function.md) da una sessione specifica in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="c1fe2-266">Il database temporaneo è escluso da questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="c1fe2-267">**Windows XP e Windows Server 2003:**  Questo parametro è di sola scrittura in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="c1fe2-268">**Windows Vista:**  Questo parametro si comporta normalmente a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="c1fe2-269">**Nota**  Questo parametro è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-270">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-271">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fe2-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-272">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-274">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-275">False, True</span><span class="sxs-lookup"><span data-stu-id="c1fe2-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-276">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-277">Globale</span><span class="sxs-lookup"><span data-stu-id="c1fe2-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-278">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-279">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-279">No</span></span></p>
<p><span data-ttu-id="c1fe2-280"><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-281">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-282">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-283">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-284">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-285">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-286">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-287">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-288">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-289">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-290">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-291">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-292">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="c1fe2-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="c1fe2-294">35</span><span class="sxs-lookup"><span data-stu-id="c1fe2-294">35</span></span>  

<span data-ttu-id="c1fe2-295">Questo parametro controlla il comportamento della deframmentazione in linea quando viene avviato con [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1fe2-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="c1fe2-296">Per ulteriori informazioni, vedere [JetDefragment](./jetdefragment-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c1fe2-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="c1fe2-297">Windows 2000: su Windows 2000, questo parametro è un valore booleano semplice che consente di controllare la deframmentazione in linea quando viene avviata da [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1fe2-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="c1fe2-298">Se impostata su **true**, la deframmentazione in linea verrà eseguita sui record di ogni tabella del database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="c1fe2-299">**Windows XP:**  In Windows XP e versioni successive, questo parametro può essere impostato su una o più delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1fe2-300">Opzione</span><span class="sxs-lookup"><span data-stu-id="c1fe2-300">Option</span></span></p></th>
<th><p><span data-ttu-id="c1fe2-301">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1fe2-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="c1fe2-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-303">Non eseguire la deframmentazione in linea.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="c1fe2-304">Si tratta del file binario equivalente all'impostazione Windows 2000 di false per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="c1fe2-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-306">Eseguire la deframmentazione completa in linea.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-306">Perform full online defragmentation.</span></span> <span data-ttu-id="c1fe2-307">Si tratta del file binario equivalente all'impostazione di Windows 2000 true per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="c1fe2-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-309">Eseguire la deframmentazione in linea dei record di ogni tabella nel database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="c1fe2-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-311">Eseguire la deframmentazione in linea degli alberi dello spazio di ogni tabella nel database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="c1fe2-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-313">Questo parametro viene utilizzato per supportare l'infrastruttura di Microsoft Exchange e non può essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c1fe2-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-315">Eseguire la deframmentazione completa in linea.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-315">Perform full online defragmentation.</span></span> <span data-ttu-id="c1fe2-316">Si tratta dell'equivalente concettuale dell'impostazione di Windows 2000 true per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-317">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-318"><strong>Windows 2000:</strong>  True</span><span class="sxs-lookup"><span data-stu-id="c1fe2-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="c1fe2-319"><strong>Windows XP: per Windows XP e versioni successive:</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c1fe2-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-320">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-321"><strong>Windows 2000:</strong>  Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="c1fe2-322"><strong>Windows XP e versioni successive:</strong>  JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="c1fe2-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-323">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-324"><strong>Windows 2000:</strong>  False, true</span><span class="sxs-lookup"><span data-stu-id="c1fe2-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="c1fe2-325"><strong>Windows XP e versioni successive:</strong>  0-JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c1fe2-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-326">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-327">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-328">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-329">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-330">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-331">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-332">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-333">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-334">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-335">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-336">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-337">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-338">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-339">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-340">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-341">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="c1fe2-343">20</span><span class="sxs-lookup"><span data-stu-id="c1fe2-343">20</span></span>  

<span data-ttu-id="c1fe2-344">Questo parametro è la soglia utilizzata dal motore di database per controllare la frammentazione dello spazio libero.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="c1fe2-345">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-346">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-347">8</span><span class="sxs-lookup"><span data-stu-id="c1fe2-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-348">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-349">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-350">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-351">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1fe2-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-352">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-353">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-354">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-355">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-356">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-357">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-358">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-359">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-360">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-361">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-362">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-363">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-364">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-365">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-366">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-367">Tutti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="c1fe2-369">78</span><span class="sxs-lookup"><span data-stu-id="c1fe2-369">78</span></span>

<span data-ttu-id="c1fe2-370">Questo parametro controlla il modo in cui il gestore della cache delle pagine del database scrive una pagina di database sottoposta a una conversione del formato sul posto.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="c1fe2-371">Queste conversioni di formato si verificano in tempo reale durante il caricamento delle pagine da un database creato con il motore di database di Windows 2000 ma utilizzato da Windows XP o versione successiva del motore di database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-372">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-373">1</span><span class="sxs-lookup"><span data-stu-id="c1fe2-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-374">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-375">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-376">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-377">0-3</span><span class="sxs-lookup"><span data-stu-id="c1fe2-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-378">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-379">Globale</span><span class="sxs-lookup"><span data-stu-id="c1fe2-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-380">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-381">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-382">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-383">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-384">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-385">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-386">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-387">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-388">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-389">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-390">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-391">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-392">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-393">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="c1fe2-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="c1fe2-395">153</span><span class="sxs-lookup"><span data-stu-id="c1fe2-395">153</span></span>  

<span data-ttu-id="c1fe2-396">Latenza (nei log) dietro il registro di suggerimento/massimo di cui è stato eseguito il commit per rinviare gli scaricamenti della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="c1fe2-397">L'abilitazione di questa latenza può consentire il ripristino del database in caso di perdita irreversibile del file di log più recente.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="c1fe2-398">Vedere JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-399">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-400">0</span><span class="sxs-lookup"><span data-stu-id="c1fe2-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-401">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-402">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-403">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="c1fe2-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-405">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-406">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-407">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-408">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-409">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-410">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-411">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-412">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-413">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-414">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-415">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-416">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-417">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-418">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-419">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1fe2-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="c1fe2-422">160</span><span class="sxs-lookup"><span data-stu-id="c1fe2-422">160</span></span>  

<span data-ttu-id="c1fe2-423">Attiva/disattiva la deframmentazione automatica dell'albero B sequenziale.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-424">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-425">1</span><span class="sxs-lookup"><span data-stu-id="c1fe2-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-426">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fe2-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-428">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-429">0-1</span><span class="sxs-lookup"><span data-stu-id="c1fe2-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-430">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-431">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-432">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-433">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-434">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-435">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-436">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-437">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-438">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-439">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-440">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-441">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-442">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-443">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-444">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1fe2-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="c1fe2-447">161</span><span class="sxs-lookup"><span data-stu-id="c1fe2-447">161</span></span>  

<span data-ttu-id="c1fe2-448">Determina la frequenza di controllo della densità dell'albero B.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-449">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-450">10</span><span class="sxs-lookup"><span data-stu-id="c1fe2-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-451">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-452">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-453">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-454">0-numero intero massimo</span><span class="sxs-lookup"><span data-stu-id="c1fe2-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-455">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-456">Istanza</span><span class="sxs-lookup"><span data-stu-id="c1fe2-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-457">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-458">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-459">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-460">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-461">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-462">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-463">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-464">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-465">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-466">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-467">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-468">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-469">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1fe2-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1fe2-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="c1fe2-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="c1fe2-472">162</span><span class="sxs-lookup"><span data-stu-id="c1fe2-472">162</span></span>  

<span data-ttu-id="c1fe2-473">Tempo massimo, in millisecondi, durante il quale il meccanismo di limitazione delle operazioni di I/O fornisce un'attività da eseguire perché venga considerato "completato".</span><span class="sxs-lookup"><span data-stu-id="c1fe2-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-474">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-475">125</span><span class="sxs-lookup"><span data-stu-id="c1fe2-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-476">Digitare:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-477">Integer</span><span class="sxs-lookup"><span data-stu-id="c1fe2-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-478">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="c1fe2-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-480">Ambito:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-481">Globale</span><span class="sxs-lookup"><span data-stu-id="c1fe2-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-482">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-483">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-484">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-485">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-486">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-487">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-488">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-489">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-490">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-491">Sì</span><span class="sxs-lookup"><span data-stu-id="c1fe2-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-492">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-493">No</span><span class="sxs-lookup"><span data-stu-id="c1fe2-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-494">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="c1fe2-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1fe2-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1fe2-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c1fe2-496">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1fe2-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-497"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c1fe2-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c1fe2-498">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1fe2-499"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c1fe2-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c1fe2-500">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1fe2-501"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c1fe2-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c1fe2-502">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c1fe2-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c1fe2-503">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c1fe2-503">See Also</span></span>

[<span data-ttu-id="c1fe2-504">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="c1fe2-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="c1fe2-505">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c1fe2-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c1fe2-506">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="c1fe2-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="c1fe2-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="c1fe2-507">JetInit</span></span>](./jetinit-function.md)
