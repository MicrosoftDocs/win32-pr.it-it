---
description: 'Altre informazioni su: funzione JetInit3'
title: Funzione JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350421"
---
# <a name="jetinit3-function"></a><span data-ttu-id="e0e2e-103">Funzione JetInit3</span><span class="sxs-lookup"><span data-stu-id="e0e2e-103">JetInit3 Function</span></span>


<span data-ttu-id="e0e2e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0e2e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="e0e2e-105">Funzione JetInit3</span><span class="sxs-lookup"><span data-stu-id="e0e2e-105">JetInit3 Function</span></span>

<span data-ttu-id="e0e2e-106">La funzione **JetInit3** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="e0e2e-107">Il motore deve essere già configurato correttamente per l'inizializzazione, operazione eseguita usando la funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2e-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="e0e2e-108">Si noti che il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="e0e2e-109">**Windows Vista:**  **JetInit3** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e0e2e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0e2e-110">Parameters</span></span>

<span data-ttu-id="e0e2e-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="e0e2e-111">*pinstance*</span></span>

<span data-ttu-id="e0e2e-112">Istanza di utilizzata per una particolare chiamata.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="e0e2e-113">L'uso di questo parametro dipende dalla modalità operativa del motore.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="e0e2e-114">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000), in cui è supportata una sola istanza, è possibile impostare questo parametro su **null** o su un buffer di output valido contenente **null** o JET_instanceNil, che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="e0e2e-115">Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="e0e2e-116">Se il motore funziona in modalità a istanze diverse, è necessario impostare questo parametro su un buffer di input valido contenente l'handle dell'istanza restituito dalla funzione [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzata.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="e0e2e-117">*prstInfo*</span><span class="sxs-lookup"><span data-stu-id="e0e2e-117">*prstInfo*</span></span>

<span data-ttu-id="e0e2e-118">Parametri di recupero aggiuntivi utilizzati per rimappare i database durante il ripristino, per impostare la posizione in cui il ripristino viene arrestato o per determinare lo stato di ripristino corrente.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="e0e2e-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e0e2e-119">*grbit*</span></span>

<span data-ttu-id="e0e2e-120">Gruppo di bit che specifica zero o più opzioni elencate e definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0e2e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e0e2e-121">Value</span></span></p></th>
<th><p><span data-ttu-id="e0e2e-122">Significato</span><span class="sxs-lookup"><span data-stu-id="e0e2e-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="e0e2e-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-124">Questo valore è riservato per l'uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="e0e2e-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-126">Questo valore è riservato per l'uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="e0e2e-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-128">Questo valore consente all'utente di eseguire il ripristino in un set di file di log, anche in assenza dei database collegati al set di file di log in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="e0e2e-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-130">Questo valore consente all'utente di eseguire il ripristino, ma solo fino alla fase di annullamento (e non inclusa).</span><span class="sxs-lookup"><span data-stu-id="e0e2e-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="e0e2e-131">Utilizzando questo valore, i log delle transazioni aggiuntivi possono essere copiati e applicati.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="e0e2e-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-133">Questo valore causa il troncamento dei file di log durante un ripristino soft.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="e0e2e-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-135">Questo valore causa la mancata impostazione predefinita di una voce di mapping del database nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="e0e2e-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-137">Questo valore causa la perdita dei log dalla fine del flusso di log da ignorare durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="e0e2e-138"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e0e2e-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0e2e-139">Return Value</span></span>

<span data-ttu-id="e0e2e-140">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="e0e2e-141">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2e-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="e0e2e-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0e2e-142">Remarks</span></span>

<span data-ttu-id="e0e2e-143">Un'istanza deve essere inizializzata con una chiamata alla funzione **JetInit3** prima che possa essere utilizzata da qualsiasi altra funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2e-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="e0e2e-144">Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata tramite la funzione [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2e-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="e0e2e-145">Un'istanza è l'unità di recupero per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="e0e2e-146">Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="e0e2e-147">Questi file includono il file del checkpoint e i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="e0e2e-148">Si noti che [JetTerm](./jetterm-function.md) non deve essere chiamato se la funzione **JetInit3** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="e0e2e-149">Tuttavia, [JetTerm](./jetterm-function.md) deve comunque essere chiamato per tutte le istanze create da **JetCreateInstance2** se **JetInit3** non è mai stato chiamato o se **JetInit3** ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="e0e2e-150">Se il ripristino viene eseguito in un set di log per cui non sono presenti tutti i database correlati (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, viene utilizzato l'errore JET_bitReplayIgnoreMissingDB per continuare il ripristino dei database disponibili.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="e0e2e-151">Poiché il ripristino dell'arresto anomalo del sistema non si verifica di solito nello stesso computer (e con la stessa configurazione) del momento in cui si è verificato l'arresto anomalo, un database non cambia in genere il percorso.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="e0e2e-152">In alcuni scenari, ad esempio lo stato di trasferimento di file in un computer diverso o il ripristino del backup di snapshot in posizioni diverse, questo non è più vero.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="e0e2e-153">La funzione **JetInit3** consente di specificare un mapping (usando le strutture [JET_RSTINFO](./jet-rstinfo-structure.md) e [JET_RSTMAP](./jet-rstmap-structure.md) ) tra il percorso del database precedente e la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="e0e2e-154">Infatti, è necessaria solo la nuova posizione purché i file di database siano presenti in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="e0e2e-155">Non appena si conoscono i percorsi dei database ripristinati, la firma del database verrà utilizzata per identificare il database durante il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="e0e2e-156">Il percorso del database originale sarà necessario solo se è necessario ricreare un database, nel qual caso la firma è nota.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="e0e2e-157">Inoltre, se è necessario arrestare un ripristino dopo un'operazione di annullamento, è possibile specificare una posizione di log specifica in corrispondenza della quale il ripristino viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="e0e2e-158">Si noti che ciò include la possibilità di arrestare alla fine di una particolare generazione del log se la posizione specificata fa parte della generazione ma oltre la fine del log effettivo.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="e0e2e-159">Per ulteriori informazioni, vedere la sezione "osservazioni" nell'argomento [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2e-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0e2e-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0e2e-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-161">Client</span><span class="sxs-lookup"><span data-stu-id="e0e2e-161">Client</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-162">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-163">Server</span><span class="sxs-lookup"><span data-stu-id="e0e2e-163">Server</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-164">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0e2e-165">Header</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-166">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-167">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0e2e-167">Library</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-168">USA ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e2e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e0e2e-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-170">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0e2e-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e2e-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="e0e2e-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="e0e2e-172">Implementato come <strong>JetInit3W</strong> (Unicode) e <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e0e2e-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0e2e-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e0e2e-173">See Also</span></span>

[<span data-ttu-id="e0e2e-174">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="e0e2e-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="e0e2e-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0e2e-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0e2e-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e0e2e-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e0e2e-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e0e2e-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e0e2e-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="e0e2e-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="e0e2e-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="e0e2e-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="e0e2e-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="e0e2e-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e0e2e-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="e0e2e-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="e0e2e-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="e0e2e-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="e0e2e-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="e0e2e-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e0e2e-184">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="e0e2e-184">Resource Parameters</span></span>](./resource-parameters.md)
