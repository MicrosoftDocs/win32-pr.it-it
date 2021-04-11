---
description: 'Altre informazioni su: parametri di database temporanei'
title: Parametri di database temporanei
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233352"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="432a4-103">Parametri di database temporanei</span><span class="sxs-lookup"><span data-stu-id="432a4-103">Temporary Database Parameters</span></span>


<span data-ttu-id="432a4-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="432a4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="432a4-105">Parametri di database temporanei</span><span class="sxs-lookup"><span data-stu-id="432a4-105">Temporary Database Parameters</span></span>

<span data-ttu-id="432a4-106">In questo argomento sono contenuti i parametri utilizzati per il database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="432a4-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="432a4-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="432a4-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="432a4-108">46</span><span class="sxs-lookup"><span data-stu-id="432a4-108">46</span></span>  

<span data-ttu-id="432a4-109">Questo parametro controlla l'utilizzo delle transazioni nelle tabelle temporanee.</span><span class="sxs-lookup"><span data-stu-id="432a4-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="432a4-110">Quando questo parametro è false, le tabelle temporanee saranno più veloci, ma non sarà possibile eseguire il rollback degli aggiornamenti effettuati in una transazione.</span><span class="sxs-lookup"><span data-stu-id="432a4-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="432a4-111">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="432a4-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="432a4-112">Vero</span><span class="sxs-lookup"><span data-stu-id="432a4-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="432a4-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="432a4-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="432a4-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-115">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="432a4-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="432a4-116">False, True</span><span class="sxs-lookup"><span data-stu-id="432a4-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-117">Ambito:</span><span class="sxs-lookup"><span data-stu-id="432a4-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="432a4-118">Istanza</span><span class="sxs-lookup"><span data-stu-id="432a4-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-119">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-120">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-121">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-122">No</span><span class="sxs-lookup"><span data-stu-id="432a4-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-123">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="432a4-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="432a4-124">No</span><span class="sxs-lookup"><span data-stu-id="432a4-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-125">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-126">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-127">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="432a4-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="432a4-128">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-129">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="432a4-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="432a4-130">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-131">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-132">Tutti</span><span class="sxs-lookup"><span data-stu-id="432a4-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="432a4-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="432a4-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="432a4-134">19</span><span class="sxs-lookup"><span data-stu-id="432a4-134">19</span></span>  

<span data-ttu-id="432a4-135">Questo parametro controlla la dimensione iniziale del database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="432a4-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="432a4-136">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="432a4-136">The size is in database pages.</span></span> <span data-ttu-id="432a4-137">Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale.</span><span class="sxs-lookup"><span data-stu-id="432a4-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="432a4-138">È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="432a4-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="432a4-139">L'impostazione di questo parametro su 14 consentirà di ottenere il database temporaneo più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="432a4-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="432a4-140">Si noti che è possibile eliminare completamente il database temporaneo impostando **JET_paramMaxTemporaryTables** su zero.</span><span class="sxs-lookup"><span data-stu-id="432a4-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="432a4-141">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="432a4-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="432a4-142">0</span><span class="sxs-lookup"><span data-stu-id="432a4-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-143">Digitare:</span><span class="sxs-lookup"><span data-stu-id="432a4-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="432a4-144">Integer</span><span class="sxs-lookup"><span data-stu-id="432a4-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-145">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="432a4-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="432a4-146">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="432a4-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-147">Ambito:</span><span class="sxs-lookup"><span data-stu-id="432a4-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="432a4-148">Istanza</span><span class="sxs-lookup"><span data-stu-id="432a4-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-149">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-150">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-151">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-152">No</span><span class="sxs-lookup"><span data-stu-id="432a4-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-153">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="432a4-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="432a4-154">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-155">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-156">No</span><span class="sxs-lookup"><span data-stu-id="432a4-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-157">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="432a4-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="432a4-158">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-159">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="432a4-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="432a4-160">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-161">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-162">Tutti</span><span class="sxs-lookup"><span data-stu-id="432a4-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="432a4-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="432a4-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="432a4-164">1</span><span class="sxs-lookup"><span data-stu-id="432a4-164">1</span></span>  

<span data-ttu-id="432a4-165">Questo parametro indica il percorso file system relativo o assoluto della cartella o del file che conterrà il database temporaneo per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="432a4-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="432a4-166">Se il percorso è una cartella che conterrà il database temporaneo, deve terminare con un carattere barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="432a4-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="432a4-167">Il database temporaneo viene utilizzato per contenere dati volatili generati durante il processo di gestione delle chiamate alle informazioni API ESE, creazione di indici o archiviazione del contenuto di una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="432a4-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="432a4-168">**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.</span><span class="sxs-lookup"><span data-stu-id="432a4-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="432a4-169">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="432a4-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="432a4-170">&quot;tmp. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="432a4-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-171">Digitare:</span><span class="sxs-lookup"><span data-stu-id="432a4-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="432a4-172">Path (stringa)</span><span class="sxs-lookup"><span data-stu-id="432a4-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-173">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="432a4-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="432a4-174">da 0 a 247 caratteri</span><span class="sxs-lookup"><span data-stu-id="432a4-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-175">Ambito:</span><span class="sxs-lookup"><span data-stu-id="432a4-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="432a4-176">Istanza</span><span class="sxs-lookup"><span data-stu-id="432a4-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-177">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-178">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-179">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="432a4-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="432a4-180">No</span><span class="sxs-lookup"><span data-stu-id="432a4-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-181">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="432a4-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="432a4-182">Sì</span><span class="sxs-lookup"><span data-stu-id="432a4-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-183">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-184">No</span><span class="sxs-lookup"><span data-stu-id="432a4-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-185">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="432a4-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="432a4-186">No</span><span class="sxs-lookup"><span data-stu-id="432a4-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-187">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="432a4-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="432a4-188">No</span><span class="sxs-lookup"><span data-stu-id="432a4-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-189">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="432a4-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="432a4-190">Tutti</span><span class="sxs-lookup"><span data-stu-id="432a4-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="432a4-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="432a4-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="432a4-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="432a4-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="432a4-193">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="432a4-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="432a4-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="432a4-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="432a4-195">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="432a4-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="432a4-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="432a4-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="432a4-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="432a4-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="432a4-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="432a4-198">See Also</span></span>

[<span data-ttu-id="432a4-199">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="432a4-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="432a4-200">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="432a4-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="432a4-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="432a4-201">JetInit</span></span>](./jetinit-function.md)
