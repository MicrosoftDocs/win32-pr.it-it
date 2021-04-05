---
description: 'Altre informazioni su: funzione JetInit2'
title: Funzione JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969540"
---
# <a name="jetinit2-function"></a><span data-ttu-id="ec945-103">Funzione JetInit2</span><span class="sxs-lookup"><span data-stu-id="ec945-103">JetInit2 Function</span></span>


<span data-ttu-id="ec945-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec945-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="ec945-105">Funzione JetInit2</span><span class="sxs-lookup"><span data-stu-id="ec945-105">JetInit2 Function</span></span>

<span data-ttu-id="ec945-106">La funzione **JetInit2** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec945-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="ec945-107">Il motore deve essere già configurato correttamente per l'inizializzazione tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec945-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="ec945-108">Il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ec945-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="ec945-109">**Windows XP:**  **JetInit2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ec945-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="ec945-110">questa funzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="ec945-110">This function is obsolete.</span></span> <span data-ttu-id="ec945-111">In alternativa, usare [JetInit3](./jetinit3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ec945-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="ec945-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec945-112">Parameters</span></span>

<span data-ttu-id="ec945-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="ec945-113">*pinstance*</span></span>

<span data-ttu-id="ec945-114">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="ec945-114">The instance to use for this call.</span></span>

<span data-ttu-id="ec945-115">Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.</span><span class="sxs-lookup"><span data-stu-id="ec945-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="ec945-116">Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore.</span><span class="sxs-lookup"><span data-stu-id="ec945-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="ec945-117">Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL o può essere impostato su un buffer di output valido che contiene NULL o JET_instanceNil che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ec945-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="ec945-118">Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ec945-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="ec945-119">Se il motore funziona in modalità a istanze diverse, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle dell'istanza restituito da [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="ec945-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="ec945-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ec945-120">*grbit*</span></span>

<span data-ttu-id="ec945-121">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ec945-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec945-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ec945-122">Value</span></span></p></th>
<th><p><span data-ttu-id="ec945-123">Significato</span><span class="sxs-lookup"><span data-stu-id="ec945-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec945-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="ec945-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="ec945-125">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ec945-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec945-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="ec945-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="ec945-127">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ec945-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec945-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="ec945-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="ec945-129">Questa opzione consente all'utente di eseguire il ripristino in un set di file di log, senza che tutti i database presenti siano collegati in un punto del set di log.</span><span class="sxs-lookup"><span data-stu-id="ec945-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec945-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="ec945-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="ec945-131">Eseguire il ripristino, ma arrestare la fase di rollback.</span><span class="sxs-lookup"><span data-stu-id="ec945-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="ec945-132">Ciò consente la copia e l'applicazione dei log delle transazioni aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ec945-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec945-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="ec945-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="ec945-134">Al completamento del ripristino, troncare i file di log.</span><span class="sxs-lookup"><span data-stu-id="ec945-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec945-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="ec945-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="ec945-136">Impostazione predefinita per la voce della mappa di database non presente nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="ec945-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec945-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="ec945-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="ec945-138">Ignorare i log persi alla fine del flusso di log.</span><span class="sxs-lookup"><span data-stu-id="ec945-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="ec945-139"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ec945-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ec945-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec945-140">Return Value</span></span>

<span data-ttu-id="ec945-141">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ec945-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ec945-142">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ec945-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="ec945-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec945-143">Remarks</span></span>

<span data-ttu-id="ec945-144">Un'istanza deve essere inizializzata con una chiamata a **JetInit2** prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec945-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="ec945-145">Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec945-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="ec945-146">Un'istanza è l'unità di recupero per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="ec945-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="ec945-147">Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database.</span><span class="sxs-lookup"><span data-stu-id="ec945-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="ec945-148">Questi file includono il file del checkpoint e i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ec945-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="ec945-149">Se il ripristino viene eseguito in un set di log, per cui non sono presenti tutti i database (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, il JET_ bitReplayIgnoreMissingDB viene utilizzato per continuare il ripristino dei database disponibili.</span><span class="sxs-lookup"><span data-stu-id="ec945-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="ec945-150">Per ulteriori informazioni, vedere la sezione Osservazioni in [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ec945-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ec945-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec945-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec945-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec945-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec945-153">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ec945-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec945-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec945-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec945-155">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ec945-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec945-156"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ec945-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec945-157">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ec945-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec945-158"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ec945-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ec945-159">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ec945-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec945-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ec945-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ec945-161">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ec945-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ec945-162">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec945-162">See Also</span></span>

[<span data-ttu-id="ec945-163">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="ec945-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="ec945-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ec945-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ec945-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ec945-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ec945-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ec945-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ec945-167">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="ec945-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="ec945-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="ec945-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ec945-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="ec945-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="ec945-170">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="ec945-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="ec945-171">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="ec945-171">Resource Parameters</span></span>](./resource-parameters.md)
