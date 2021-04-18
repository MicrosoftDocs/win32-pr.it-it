---
description: 'Altre informazioni su: parametri del log delle transazioni'
title: Parametri del log delle transazioni
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315610"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="ccadc-103">Parametri del log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="ccadc-103">Transaction Log Parameters</span></span>


<span data-ttu-id="ccadc-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ccadc-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="ccadc-105">**In questo articolo**</span><span class="sxs-lookup"><span data-stu-id="ccadc-105">**In this article**</span></span>  
<span data-ttu-id="ccadc-106">Parametri del log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="ccadc-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="ccadc-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccadc-107">Requirements</span></span>  
<span data-ttu-id="ccadc-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ccadc-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="ccadc-109">Parametri del log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="ccadc-109">Transaction Log Parameters</span></span>

<span data-ttu-id="ccadc-110">Questo argomento contiene i parametri usati per i log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="ccadc-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="ccadc-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="ccadc-112">3</span><span class="sxs-lookup"><span data-stu-id="ccadc-112">3</span></span>  

<span data-ttu-id="ccadc-113">Questo parametro imposta il prefisso di tre lettere usato per molti dei file usati dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="ccadc-114">Il file del checkpoint, ad esempio, è denominato EDB. CHK per impostazione predefinita, perché EDB è il nome di base predefinito.</span><span class="sxs-lookup"><span data-stu-id="ccadc-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="ccadc-115">Il nome di base può essere utilizzato per distinguere facilmente tra i set di file che appartengono a istanze diverse o a applicazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="ccadc-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-116">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-117">&quot;edb&quot;</span><span class="sxs-lookup"><span data-stu-id="ccadc-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-118">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-119">string</span><span class="sxs-lookup"><span data-stu-id="ccadc-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-120">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-121">3 caratteri</span><span class="sxs-lookup"><span data-stu-id="ccadc-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-122">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-123">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-124">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-125">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-126">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-127">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-128">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-129">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-130">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-131">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-132">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-133">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-134">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-135">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-136">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-137">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="ccadc-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="ccadc-139">17</span><span class="sxs-lookup"><span data-stu-id="ccadc-139">17</span></span>  

<span data-ttu-id="ccadc-140">Questo parametro consente di configurare il modo in cui i file di log delle transazioni vengono gestiti dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="ccadc-141">Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono conservati su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="ccadc-142">In questa modalità è possibile eseguire il ripristino da un backup precedente e riprodurlo attraverso tutti i file di log delle transazioni conservati, in modo che nessun dato venga perso a causa dell'emergenza che ha forzato il ripristino.</span><span class="sxs-lookup"><span data-stu-id="ccadc-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="ccadc-143">Sono necessari backup completi regolari per impedire che il disco si riempia con i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="ccadc-144">Quando la registrazione circolare è attiva, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="ccadc-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="ccadc-145">Il vantaggio di questa modalità è che non è necessario che i backup ritirino i vecchi file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="ccadc-146">Il compromesso è che il ripristino di una perdita di dati pari a zero non è più possibile.</span><span class="sxs-lookup"><span data-stu-id="ccadc-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-147">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-148">Falso</span><span class="sxs-lookup"><span data-stu-id="ccadc-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-149">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccadc-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-151">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-152">False, True</span><span class="sxs-lookup"><span data-stu-id="ccadc-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-153">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-154">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-155">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-156">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-157">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-158">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-159">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-160">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-161">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-162">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-163">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-164">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-165">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-166">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-167">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-168">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="ccadc-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="ccadc-170">16</span><span class="sxs-lookup"><span data-stu-id="ccadc-170">16</span></span>  

<span data-ttu-id="ccadc-171">Questo parametro controlla l'azione predefinita eseguita quando viene eseguito il commit della transazione più esterna in una sessione.</span><span class="sxs-lookup"><span data-stu-id="ccadc-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="ccadc-172">Qualsiasi opzione valida che può essere passata a [JetCommitTransaction](./jetcommittransaction-function.md) può essere impostata anche come predefinita per tutte le sessioni in un'istanza e/o per una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="ccadc-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="ccadc-173">Per ulteriori informazioni su queste opzioni, vedere [JetCommitTransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ccadc-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="ccadc-174">Questo parametro ha un effetto sull'affidabilità e sulle prestazioni delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="ccadc-175">Per ulteriori informazioni, vedere [JetCommitTransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ccadc-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-176">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-177">0</span><span class="sxs-lookup"><span data-stu-id="ccadc-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-178">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-179">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ccadc-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-180">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-181">Opzione valida per JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="ccadc-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-182">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-183">Istanza o sessione</span><span class="sxs-lookup"><span data-stu-id="ccadc-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-184">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-185">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-186">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-187">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-188">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-189">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-190">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-191">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-192">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-193">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-194">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-195">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-196">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-197">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="ccadc-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="ccadc-199">48</span><span class="sxs-lookup"><span data-stu-id="ccadc-199">48</span></span>  

<span data-ttu-id="ccadc-200">Se questo parametro è true e i file di log delle transazioni a cui fa riferimento il percorso del file di log (**JET_paramLogFilePath**) sono di una versione obsoleta, i file di log delle transazioni verranno automaticamente eliminati.</span><span class="sxs-lookup"><span data-stu-id="ccadc-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="ccadc-201">**Windows 2000:**  È necessario prestare attenzione con l'utilizzo di questo parametro quando si aggiorna un database da Windows NT a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ccadc-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="ccadc-202">Se il database non è in uno stato coerente e i file di log obsoleti vengono eliminati, il contenuto del database andrà perso.</span><span class="sxs-lookup"><span data-stu-id="ccadc-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-203">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-204"><strong>Windows 2000:</strong>  False</span><span class="sxs-lookup"><span data-stu-id="ccadc-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="ccadc-205"><strong>Windows XP:</strong>  True</span><span class="sxs-lookup"><span data-stu-id="ccadc-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-206">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccadc-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-208">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-209">False, True</span><span class="sxs-lookup"><span data-stu-id="ccadc-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-210">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-211">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-212">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-213">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-214">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-215">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-216">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-217">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-218">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-219">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-220">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-221">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-222">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-223">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-224">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-225">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="ccadc-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="ccadc-227">47</span><span class="sxs-lookup"><span data-stu-id="ccadc-227">47</span></span>  

<span data-ttu-id="ccadc-228">Se questo parametro è true, il motore di database non convaliderà il numero di versione del file di log delle transazioni durante [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="ccadc-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="ccadc-229">**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-230">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-231">Falso</span><span class="sxs-lookup"><span data-stu-id="ccadc-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-232">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccadc-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-234">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-235">False, True</span><span class="sxs-lookup"><span data-stu-id="ccadc-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-236">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-237">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-238">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-239">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-240">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-241">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-242">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-243">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-244">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-245">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-246">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-247">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-248">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-249">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-250">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-251">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="ccadc-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="ccadc-253">136</span><span class="sxs-lookup"><span data-stu-id="ccadc-253">136</span></span>  

<span data-ttu-id="ccadc-254">Questo parametro fornisce la compatibilità con le versioni precedenti con le convenzioni di denominazione dei file delle versioni precedenti del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="ccadc-255">Attualmente sono supportate le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccadc-255">The following options are currently supported:</span></span>

<span data-ttu-id="ccadc-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ccadc-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="ccadc-257">Quando questa opzione è presente, il motore di database utilizzerà le convenzioni di denominazione seguenti per i file:</span><span class="sxs-lookup"><span data-stu-id="ccadc-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="ccadc-258">I file di log delle transazioni utilizzeranno. LOG per l'estensione di file</span><span class="sxs-lookup"><span data-stu-id="ccadc-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="ccadc-259">I file del checkpoint utilizzeranno. CHK per la relativa estensione di file</span><span class="sxs-lookup"><span data-stu-id="ccadc-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-260">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ccadc-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-262">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-263">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ccadc-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-264">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ccadc-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-266">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-267">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-268">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-269">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-270">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-271">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-272">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-273">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-274">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-275">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-276">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-277">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-278">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-279">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-280">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-281">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="ccadc-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="ccadc-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="ccadc-283">12</span><span class="sxs-lookup"><span data-stu-id="ccadc-283">12</span></span>  

<span data-ttu-id="ccadc-284">Questo parametro consente di configurare la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="ccadc-285">L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="ccadc-286">La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità.</span><span class="sxs-lookup"><span data-stu-id="ccadc-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="ccadc-287">Questo parametro ha un effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="ccadc-288">Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ccadc-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="ccadc-289">Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato.</span><span class="sxs-lookup"><span data-stu-id="ccadc-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="ccadc-290">Il valore predefinito è troppo piccolo per questo caso.</span><span class="sxs-lookup"><span data-stu-id="ccadc-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="ccadc-291">**Windows XP e windows 2000:**  In Windows XP e nelle versioni precedenti non è consigliabile impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-292">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-293"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80</span><span class="sxs-lookup"><span data-stu-id="ccadc-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="ccadc-294"><strong>Windows Vista:</strong>  126</span><span class="sxs-lookup"><span data-stu-id="ccadc-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-295">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-296">Integer</span><span class="sxs-lookup"><span data-stu-id="ccadc-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-297">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-298"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ccadc-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="ccadc-299"><strong>Windows Vista:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ccadc-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-300">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-301">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-302">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-303">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-304">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-305">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-306">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-307">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-308">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-309">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-310">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-311">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-312">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-313">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-314">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-315">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="ccadc-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="ccadc-317">14</span><span class="sxs-lookup"><span data-stu-id="ccadc-317">14</span></span>  

<span data-ttu-id="ccadc-318">Questo parametro configura il motore di database per l'esecuzione di un checkpoint quando è stato generato il numero specificato di settori dei file di log.</span><span class="sxs-lookup"><span data-stu-id="ccadc-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="ccadc-319">**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-320">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-321">1024</span><span class="sxs-lookup"><span data-stu-id="ccadc-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-322">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-323">Integer</span><span class="sxs-lookup"><span data-stu-id="ccadc-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-324">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-325">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ccadc-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-326">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-327">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-328">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-329">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-330">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-331">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-332">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-333">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-334">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-335">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-336">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-337">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-338">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-339">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-340">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-341">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="ccadc-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="ccadc-343">69</span><span class="sxs-lookup"><span data-stu-id="ccadc-343">69</span></span>  

<span data-ttu-id="ccadc-344">Quando questo parametro è impostato su true, il motore di database creerà il file di log delle transazioni successivo mentre viene utilizzato il file di log delle transazioni corrente.</span><span class="sxs-lookup"><span data-stu-id="ccadc-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="ccadc-345">Lo scopo è ridurre al minimo il tempo impiegato per passare da un file di log delle transazioni a quello successivo in un carico di aggiornamento intenso.</span><span class="sxs-lookup"><span data-stu-id="ccadc-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-346">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-347">Vero</span><span class="sxs-lookup"><span data-stu-id="ccadc-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-348">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="ccadc-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-350">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-351">False, True</span><span class="sxs-lookup"><span data-stu-id="ccadc-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-352">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-353">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-354">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-355">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-356">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-357">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-358">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-359">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-360">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-361">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-362">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-363">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-364">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-365">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-366">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-367">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="ccadc-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="ccadc-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="ccadc-369">2</span><span class="sxs-lookup"><span data-stu-id="ccadc-369">2</span></span> 

<span data-ttu-id="ccadc-370">Questo parametro indica il percorso file system relativo o assoluto della cartella che conterrà i log delle transazioni per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="ccadc-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="ccadc-371">Il percorso deve terminare con un carattere barra rovesciata, che indica che il percorso di destinazione è una cartella.</span><span class="sxs-lookup"><span data-stu-id="ccadc-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="ccadc-372">I file di log delle transazioni contengono le informazioni necessarie per portare i file di database in uno stato coerente dopo un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="ccadc-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="ccadc-373">In genere sono denominate EDB \* . LOG.</span><span class="sxs-lookup"><span data-stu-id="ccadc-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="ccadc-374">Il contenuto dei file di log delle transazioni è altrettanto importante (in caso contrario) rispetto ai file di database stessi.</span><span class="sxs-lookup"><span data-stu-id="ccadc-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="ccadc-375">Per proteggerli, è necessario effettuare tutte le operazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="ccadc-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="ccadc-376">Saranno disponibili anche altri file di log riservati denominati RES1. LOG e RES2. LOG archiviato insieme ai file di log ordinari.</span><span class="sxs-lookup"><span data-stu-id="ccadc-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="ccadc-377">Il contenuto di questi file non è importante perché il loro unico scopo è quello di riservare spazio su disco per consentire al motore di arrestarsi normalmente in uno scenario con un disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ccadc-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="ccadc-378">Si tratta anche di un file di log temporaneo in genere denominato EDBTMP. ACCEDERE alla stessa cartella.</span><span class="sxs-lookup"><span data-stu-id="ccadc-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="ccadc-379">Il contenuto di questo file non è importante.</span><span class="sxs-lookup"><span data-stu-id="ccadc-379">The contents of this file are not important either.</span></span> <span data-ttu-id="ccadc-380">Questo file è un nuovo file di log preparato per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ccadc-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="ccadc-381">Le proprietà del volume host dei file di log delle transazioni e della relativa posizione rispetto agli altri file utilizzati dal motore di database possono avere un impatto significativo sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="ccadc-382">**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-383">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-384">&quot;.\& quot</span><span class="sxs-lookup"><span data-stu-id="ccadc-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-385">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-386">Percorso cartella (stringa)</span><span class="sxs-lookup"><span data-stu-id="ccadc-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-387">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-388">da 0 a 246 caratteri</span><span class="sxs-lookup"><span data-stu-id="ccadc-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-389">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-390">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-391">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-392">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-393">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-394">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-395">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-396">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-397">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-398">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-399">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-400">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-401">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-402">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-403">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-404">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="ccadc-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="ccadc-406">11</span><span class="sxs-lookup"><span data-stu-id="ccadc-406">11</span></span>  

<span data-ttu-id="ccadc-407">Questo parametro consente di configurare le dimensioni dei file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="ccadc-408">Ogni file di log delle transazioni è a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="ccadc-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="ccadc-409">La dimensione è uguale all'impostazione del parametro di sistema in unità di 1024 byte.</span><span class="sxs-lookup"><span data-stu-id="ccadc-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="ccadc-410">Questo parametro ha un effetto sull'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="ccadc-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="ccadc-411">Se l'impostazione è troppo piccola, il numero massimo di file di log (1048575) verrà raggiunto molto più velocemente.</span><span class="sxs-lookup"><span data-stu-id="ccadc-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="ccadc-412">Quando si verifica questa situazione, è necessario che l'istanza venga arrestata in modo corretto, che i file di log esistenti vengano eliminati e che sia necessario riavviare l'istanza.</span><span class="sxs-lookup"><span data-stu-id="ccadc-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="ccadc-413">Questa azione non solo riduce la disponibilità dell'applicazione, ma invalida anche eventuali backup precedenti del database dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ccadc-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="ccadc-414">Questo parametro ha un effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ccadc-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="ccadc-415">Se l'impostazione è molto grande, [JetInit](./jetinit-function.md) sarà lento perché il motore di database deve leggere il file di log più recente (come minimo) al momento dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ccadc-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="ccadc-416">Se l'impostazione è molto grande, sarà necessario più tempo per passare da un file di log all'altro.</span><span class="sxs-lookup"><span data-stu-id="ccadc-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="ccadc-417">Se l'impostazione è molto piccola, sarà necessario creare più file di log per un determinato numero di aggiornamenti che aggiungono ulteriore sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="ccadc-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-418">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-419">5120</span><span class="sxs-lookup"><span data-stu-id="ccadc-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-420">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-421">Integer</span><span class="sxs-lookup"><span data-stu-id="ccadc-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-422">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-423"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="ccadc-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="ccadc-424"><strong>Windows Vista:</strong>  64-32768</span><span class="sxs-lookup"><span data-stu-id="ccadc-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-425">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-426">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-427">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-428">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-429">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-430">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-431">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-432">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-433">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-434">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-435">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-436">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-437">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-438">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-439">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-440">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="ccadc-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="ccadc-442">15</span><span class="sxs-lookup"><span data-stu-id="ccadc-442">15</span></span>  

<span data-ttu-id="ccadc-443">Questo parametro tenta di ottimizzare lo svuotamento del buffer del log causato da un commit durevole attendendo che un numero specificato di sessioni attenda un commit durevole prima di forzare l'esecuzione di uno scaricamento nella speranza che un'altra transazione possa condividere lo scaricamento.</span><span class="sxs-lookup"><span data-stu-id="ccadc-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="ccadc-444">**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-445">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-446">3</span><span class="sxs-lookup"><span data-stu-id="ccadc-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-447">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-448">Integer</span><span class="sxs-lookup"><span data-stu-id="ccadc-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-449">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-450">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ccadc-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-451">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-452">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-453">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-454">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-455">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-456">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-457">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-458">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-459">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-460">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-461">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-462">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-463">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-464">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-465">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-466">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="ccadc-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="ccadc-468">34</span><span class="sxs-lookup"><span data-stu-id="ccadc-468">34</span></span>  

<span data-ttu-id="ccadc-469">Questo parametro è l'opzione master che controlla il ripristino di arresto anomalo del sistema per un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ccadc-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="ccadc-470">Se questo parametro è impostato su "on", verrà usato il ripristino dello stile Ariete per portare tutti i database nell'istanza in uno stato coerente in caso di arresto anomalo di un processo o di un computer.</span><span class="sxs-lookup"><span data-stu-id="ccadc-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="ccadc-471">Se questo parametro è impostato su "off", tutti i database nell'istanza verranno gestiti senza il vantaggio del ripristino dell'arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="ccadc-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="ccadc-472">Ciò significa che se l'istanza non viene arrestata in modo corretto utilizzando [JetTerm](./jetterm-function.md) prima dell'uscita del processo o dell'arresto del computer, il contenuto di tutti i database in tale istanza sarà danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ccadc-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="ccadc-473">La disabilitazione del ripristino è utile in casi speciali in cui è noto che il contenuto di un database non è utile in caso di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="ccadc-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="ccadc-474">Il ripristino deve essere abilitato per tutti gli altri casi.</span><span class="sxs-lookup"><span data-stu-id="ccadc-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-475">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-476">&quot;On&quot;</span><span class="sxs-lookup"><span data-stu-id="ccadc-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-477">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-478">string</span><span class="sxs-lookup"><span data-stu-id="ccadc-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-479">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-480">da 0 a 259 caratteri</span><span class="sxs-lookup"><span data-stu-id="ccadc-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-481">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-482">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-483">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-484">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-485">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-486">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-487">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-488">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-489">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-490">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-491">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-492">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-493">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-494">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-495">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-496">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="ccadc-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="ccadc-498">0</span><span class="sxs-lookup"><span data-stu-id="ccadc-498">0</span></span>  

<span data-ttu-id="ccadc-499">Questo parametro indica il percorso file system relativo o assoluto della cartella che conterrà il file del checkpoint per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="ccadc-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="ccadc-500">Il percorso deve terminare con un carattere barra rovesciata, che indica che il percorso di destinazione è una cartella.</span><span class="sxs-lookup"><span data-stu-id="ccadc-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="ccadc-501">Il file del checkpoint è un file semplice mantenuto per ogni istanza che ricorda il file di log delle transazioni meno recente che deve essere riprodotto per portare tutti i database di tale istanza in uno stato coerente dopo un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="ccadc-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="ccadc-502">Il file del checkpoint è in genere denominato EDB. CHK.</span><span class="sxs-lookup"><span data-stu-id="ccadc-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="ccadc-503">**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-504">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-505">&quot;.\& quot</span><span class="sxs-lookup"><span data-stu-id="ccadc-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-506">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-507">Percorso cartella (stringa)</span><span class="sxs-lookup"><span data-stu-id="ccadc-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-508">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-509">da 0 a 246 caratteri</span><span class="sxs-lookup"><span data-stu-id="ccadc-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-510">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-511">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-512">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-513">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-514">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-515">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-516">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-517">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-518">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-519">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-520">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-521">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-522">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-523">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-524">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-525">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="ccadc-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="ccadc-527">13</span><span class="sxs-lookup"><span data-stu-id="ccadc-527">13</span></span> 

<span data-ttu-id="ccadc-528">Questo parametro tenta di ottimizzare lo svuotamento del buffer del log causato da un commit durevole attendendo un periodo di tempo specificato prima di forzare l'esecuzione di uno scaricamento nella speranza che un'altra transazione condivida lo scaricamento.</span><span class="sxs-lookup"><span data-stu-id="ccadc-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="ccadc-529">**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ccadc-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-530">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-531">0</span><span class="sxs-lookup"><span data-stu-id="ccadc-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-532">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-533">Integer</span><span class="sxs-lookup"><span data-stu-id="ccadc-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-534">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-535">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="ccadc-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-536">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-537">Istanza o sessione</span><span class="sxs-lookup"><span data-stu-id="ccadc-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-538">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-539">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-540">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-541">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-542">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-543">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-544">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-545">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-546">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-547">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-548">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-549">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-550">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-551">Tutti</span><span class="sxs-lookup"><span data-stu-id="ccadc-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccadc-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="ccadc-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="ccadc-553">136</span><span class="sxs-lookup"><span data-stu-id="ccadc-553">136</span></span>  

<span data-ttu-id="ccadc-554">Questo parametro viene usato per specificare le funzionalità di compatibilità per la denominazione dei file da gestire con Windows Server 2003 e lo schema di denominazione dei file precedenti.</span><span class="sxs-lookup"><span data-stu-id="ccadc-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="ccadc-555">Per ulteriori informazioni sui diversi file e i relativi nomi, vedere [file del motore di archiviazione estensibile](./extensible-storage-engine-files.md).</span><span class="sxs-lookup"><span data-stu-id="ccadc-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="ccadc-556">Il JET_bitESE98FileNames garantisce l'estensione di file utilizzata nei file di log delle transazioni e il file del checkpoint corrisponde a quello utilizzato in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ccadc-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="ccadc-557">Nota: se si esegue l'aggiornamento da Windows Server 2003, non è ancora necessario specificare questo bit perché il motore aggiornerà automaticamente le estensioni di file se JET_paramCircularLog è impostato su **true** o se JET_paramCircularLog è **false**, mantenere l'estensione di log precedente.</span><span class="sxs-lookup"><span data-stu-id="ccadc-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="ccadc-558">**Nota**  Per impostare un bit, il valore deve prima essere recuperato, quindi "or" nel bit di compatibilità desiderato.</span><span class="sxs-lookup"><span data-stu-id="ccadc-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-559">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ccadc-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-561">Digitare:</span><span class="sxs-lookup"><span data-stu-id="ccadc-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-562">JET_GRBIT (Integer)</span><span class="sxs-lookup"><span data-stu-id="ccadc-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-563">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="ccadc-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="ccadc-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-565">Ambito:</span><span class="sxs-lookup"><span data-stu-id="ccadc-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-566">Istanza</span><span class="sxs-lookup"><span data-stu-id="ccadc-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-567">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-568">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-569">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ccadc-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-570">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-571">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="ccadc-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-572">Sì</span><span class="sxs-lookup"><span data-stu-id="ccadc-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-573">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-574">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-575">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="ccadc-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-576">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-577">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="ccadc-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-578">No</span><span class="sxs-lookup"><span data-stu-id="ccadc-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-579">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="ccadc-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ccadc-580">A partire da Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccadc-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="ccadc-581">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccadc-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-582"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ccadc-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ccadc-583">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ccadc-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccadc-584"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ccadc-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ccadc-585">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ccadc-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccadc-586"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ccadc-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ccadc-587">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ccadc-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ccadc-588">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ccadc-588">See Also</span></span>

[<span data-ttu-id="ccadc-589">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="ccadc-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="ccadc-590">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="ccadc-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="ccadc-591">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="ccadc-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="ccadc-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="ccadc-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ccadc-593">JetTerm</span><span class="sxs-lookup"><span data-stu-id="ccadc-593">JetTerm</span></span>](./jetterm-function.md)
