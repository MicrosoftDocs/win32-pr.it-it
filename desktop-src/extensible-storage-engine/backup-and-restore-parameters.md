---
description: 'Altre informazioni su: backup e ripristino di parametri'
title: Parametri di backup e ripristino
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530115"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="64747-103">Parametri di backup e ripristino</span><span class="sxs-lookup"><span data-stu-id="64747-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="64747-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="64747-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="64747-105">Parametri di backup e ripristino</span><span class="sxs-lookup"><span data-stu-id="64747-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="64747-106">Questo argomento contiene i parametri usati per il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="64747-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="64747-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="64747-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="64747-108">113</span><span class="sxs-lookup"><span data-stu-id="64747-108">113</span></span>  

<span data-ttu-id="64747-109">Il percorso completo di ogni database viene reso permanente nei log delle transazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="64747-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="64747-110">In genere, è necessario che questi database rimangano nel percorso originale affinché la riproduzione delle transazioni funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="64747-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="64747-111">Questo parametro può essere utilizzato per forzare il ripristino dell'arresto anomalo del sistema o un'operazione di ripristino per la ricerca dei database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="64747-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-112">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="64747-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="64747-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="64747-114">Percorso cartella (stringa)</span><span class="sxs-lookup"><span data-stu-id="64747-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-115">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="64747-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="64747-116">da 0 a 246 caratteri</span><span class="sxs-lookup"><span data-stu-id="64747-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-117">Ambito:</span><span class="sxs-lookup"><span data-stu-id="64747-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="64747-118">Istanza</span><span class="sxs-lookup"><span data-stu-id="64747-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-119">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-120">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-121">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-122">No</span><span class="sxs-lookup"><span data-stu-id="64747-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-123">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="64747-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="64747-124">No</span><span class="sxs-lookup"><span data-stu-id="64747-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-125">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="64747-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="64747-126">No</span><span class="sxs-lookup"><span data-stu-id="64747-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-127">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="64747-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="64747-128">No</span><span class="sxs-lookup"><span data-stu-id="64747-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-129">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="64747-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="64747-130">No</span><span class="sxs-lookup"><span data-stu-id="64747-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-131">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="64747-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="64747-132">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="64747-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64747-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="64747-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="64747-134">77</span><span class="sxs-lookup"><span data-stu-id="64747-134">77</span></span>  

<span data-ttu-id="64747-135">Questo parametro controlla il risultato di [JetInit](./jetinit-function.md) quando il motore di database è configurato per iniziare a utilizzare i file di log delle transazioni su disco con dimensioni diverse da quelle configurate.</span><span class="sxs-lookup"><span data-stu-id="64747-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="64747-136">In genere, [JetInit](./jetinit-function.md) ripristinerà correttamente i database, ma avrà esito negativo con JET_errLogFileSizeMismatchDatabasesConsistent per indicare che le dimensioni del file di log non sono configurate correttamente.</span><span class="sxs-lookup"><span data-stu-id="64747-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="64747-137">Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i vecchi file di log, avvierà un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate e restituirà JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="64747-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="64747-138">Questo parametro è utile quando l'applicazione desidera modificare in modo trasparente le dimensioni del file del log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.</span><span class="sxs-lookup"><span data-stu-id="64747-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-139">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="64747-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="64747-140">Falso</span><span class="sxs-lookup"><span data-stu-id="64747-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-141">Digitare:</span><span class="sxs-lookup"><span data-stu-id="64747-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="64747-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="64747-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-143">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="64747-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="64747-144">False, True</span><span class="sxs-lookup"><span data-stu-id="64747-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-145">Ambito:</span><span class="sxs-lookup"><span data-stu-id="64747-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="64747-146">Istanza</span><span class="sxs-lookup"><span data-stu-id="64747-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-147">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-148">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-149">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-150">No</span><span class="sxs-lookup"><span data-stu-id="64747-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-151">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="64747-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="64747-152">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-153">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="64747-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="64747-154">No</span><span class="sxs-lookup"><span data-stu-id="64747-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-155">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="64747-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="64747-156">No</span><span class="sxs-lookup"><span data-stu-id="64747-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-157">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="64747-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="64747-158">No</span><span class="sxs-lookup"><span data-stu-id="64747-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-159">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="64747-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="64747-160">Tutti</span><span class="sxs-lookup"><span data-stu-id="64747-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64747-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="64747-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="64747-162">52</span><span class="sxs-lookup"><span data-stu-id="64747-162">52</span></span>  

<span data-ttu-id="64747-163">Quando questo parametro è impostato su true, tutti i file di log delle transazioni trovati sul disco che non fanno parte della sequenza di file di log corrente verranno eliminati da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="64747-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="64747-164">Questo può essere usato per pulire automaticamente i file di log estranei dopo un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="64747-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="64747-165">**Windows XP:**  Introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64747-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-166">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="64747-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="64747-167">Falso</span><span class="sxs-lookup"><span data-stu-id="64747-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-168">Digitare:</span><span class="sxs-lookup"><span data-stu-id="64747-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="64747-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="64747-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-170">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="64747-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="64747-171">False, True</span><span class="sxs-lookup"><span data-stu-id="64747-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-172">Ambito:</span><span class="sxs-lookup"><span data-stu-id="64747-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="64747-173">Istanza</span><span class="sxs-lookup"><span data-stu-id="64747-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-174">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-175">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-176">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-177">No</span><span class="sxs-lookup"><span data-stu-id="64747-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-178">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="64747-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="64747-179">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-180">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="64747-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="64747-181">No</span><span class="sxs-lookup"><span data-stu-id="64747-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-182">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="64747-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="64747-183">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-184">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="64747-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="64747-185">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-186">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="64747-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="64747-187">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="64747-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64747-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="64747-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="64747-189">82</span><span class="sxs-lookup"><span data-stu-id="64747-189">82</span></span>  

<span data-ttu-id="64747-190">Questo parametro configura la quantità di tempo consentita tra una chiamata a [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) prima che si verifichi un timeout.</span><span class="sxs-lookup"><span data-stu-id="64747-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="64747-191">Per ulteriori informazioni, vedere [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="64747-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="64747-192">Il timeout è espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="64747-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-193">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="64747-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="64747-194">20000 (Windows XP e Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="64747-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="64747-195">70000 (Windows Server 2003 SP1)</span><span class="sxs-lookup"><span data-stu-id="64747-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-196">Digitare:</span><span class="sxs-lookup"><span data-stu-id="64747-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="64747-197">Integer</span><span class="sxs-lookup"><span data-stu-id="64747-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-198">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="64747-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="64747-199">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="64747-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-200">Ambito:</span><span class="sxs-lookup"><span data-stu-id="64747-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="64747-201">Globale</span><span class="sxs-lookup"><span data-stu-id="64747-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-202">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-203">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-204">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-205">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-206">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="64747-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="64747-207">No</span><span class="sxs-lookup"><span data-stu-id="64747-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-208">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="64747-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="64747-209">No</span><span class="sxs-lookup"><span data-stu-id="64747-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-210">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="64747-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="64747-211">No</span><span class="sxs-lookup"><span data-stu-id="64747-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-212">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="64747-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="64747-213">No</span><span class="sxs-lookup"><span data-stu-id="64747-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-214">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="64747-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="64747-215">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="64747-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64747-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="64747-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="64747-217">71</span><span class="sxs-lookup"><span data-stu-id="64747-217">71</span></span>  

<span data-ttu-id="64747-218">Quando questo parametro è impostato su true, ogni pagina in un database in cui viene utilizzato un backup di flusso verrà ripulita dei dati eliminati.</span><span class="sxs-lookup"><span data-stu-id="64747-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="64747-219">È importante sottolineare che le pagine del database da pulire si trovano su disco.</span><span class="sxs-lookup"><span data-stu-id="64747-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="64747-220">Viene eseguito il backup del set di dati completo prima del processo di pulizia.</span><span class="sxs-lookup"><span data-stu-id="64747-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-221">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="64747-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="64747-222">Falso</span><span class="sxs-lookup"><span data-stu-id="64747-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-223">Digitare:</span><span class="sxs-lookup"><span data-stu-id="64747-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="64747-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="64747-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-225">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="64747-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="64747-226">False, True</span><span class="sxs-lookup"><span data-stu-id="64747-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-227">Ambito:</span><span class="sxs-lookup"><span data-stu-id="64747-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="64747-228">Istanza</span><span class="sxs-lookup"><span data-stu-id="64747-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-229">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-230">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-231">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="64747-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="64747-232">No</span><span class="sxs-lookup"><span data-stu-id="64747-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-233">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="64747-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="64747-234">No</span><span class="sxs-lookup"><span data-stu-id="64747-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-235">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="64747-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="64747-236">No</span><span class="sxs-lookup"><span data-stu-id="64747-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-237">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="64747-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="64747-238">Sì</span><span class="sxs-lookup"><span data-stu-id="64747-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-239">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="64747-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="64747-240">No</span><span class="sxs-lookup"><span data-stu-id="64747-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-241">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="64747-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="64747-242">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="64747-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="64747-243">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64747-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64747-244"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="64747-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="64747-245">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="64747-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64747-246"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="64747-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="64747-247">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="64747-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64747-248"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="64747-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="64747-249">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="64747-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="64747-250">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="64747-250">See Also</span></span>

[<span data-ttu-id="64747-251">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="64747-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="64747-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="64747-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="64747-253">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="64747-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="64747-254">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="64747-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
