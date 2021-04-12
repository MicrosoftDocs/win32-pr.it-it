---
description: 'Altre informazioni su: funzione JetDefragment'
title: JetDefragment (funzione)
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349936"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="a1f41-103">JetDefragment (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1f41-103">JetDefragment Function</span></span>


<span data-ttu-id="a1f41-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1f41-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="a1f41-105">JetDefragment (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1f41-105">JetDefragment Function</span></span>

<span data-ttu-id="a1f41-106">La funzione **JetDefragment** avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.</span><span class="sxs-lookup"><span data-stu-id="a1f41-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="a1f41-107">Questa operazione viene eseguita per limitare la crescita del database utilizzando l'allocazione dei dischi esistente in modo più efficiente all'interno del database.</span><span class="sxs-lookup"><span data-stu-id="a1f41-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="a1f41-108">Consente inoltre di ridurre working set assicurando che i dati vengano compressi in modo più accurato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="a1f41-109">Infine, può migliorare le prestazioni dell'applicazione velocizzando le operazioni comuni tramite una migliore organizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a1f41-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="a1f41-110">La deframmentazione del database è un'operazione online e non interrompe le normali attività di database, ad esempio le operazioni di query o gli aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="a1f41-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="a1f41-111">**JetDefragment** non esegue inoltre una copia di tutti i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="a1f41-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="a1f41-112">Al contrario, deframmenta un database sul posto.</span><span class="sxs-lookup"><span data-stu-id="a1f41-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="a1f41-113">Infine, **JetDefragment** ripristina lo spazio interno del database per riutilizzarlo, ma non rilascia spazio in eccesso al sistema operativo file System.</span><span class="sxs-lookup"><span data-stu-id="a1f41-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="a1f41-114">Il formato risultante dei dati può essere molto più efficiente, ma in genere non è ottimale.</span><span class="sxs-lookup"><span data-stu-id="a1f41-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="a1f41-115">La deframmentazione è limitata a rilasciare le pagine del database per riutilizzarle che contengono dati che sono già stati eliminati logicamente.</span><span class="sxs-lookup"><span data-stu-id="a1f41-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="a1f41-116">La deframmentazione rende inoltre disponibili le pagine del database da riutilizzare in alcuni casi combinando i dati di due pagine quando possono essere inseriti in una singola pagina.</span><span class="sxs-lookup"><span data-stu-id="a1f41-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="a1f41-117">Questa operazione è diversa da [JetCompact](./jetcompact-function.md) , che rende una copia di un database di sola lettura in un formato altamente ottimale.</span><span class="sxs-lookup"><span data-stu-id="a1f41-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a1f41-118">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1f41-118">Parameters</span></span>

<span data-ttu-id="a1f41-119">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a1f41-119">*sesid*</span></span>

<span data-ttu-id="a1f41-120">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a1f41-120">The session to use for this call.</span></span>

<span data-ttu-id="a1f41-121">*dbid*</span><span class="sxs-lookup"><span data-stu-id="a1f41-121">*dbid*</span></span>

<span data-ttu-id="a1f41-122">Database che verrà deframmentato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-122">The database that will be defragmented.</span></span>

<span data-ttu-id="a1f41-123">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="a1f41-123">*szTableName*</span></span>

<span data-ttu-id="a1f41-124">Parametro non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-124">Unused parameter.</span></span> <span data-ttu-id="a1f41-125">La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="a1f41-126">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="a1f41-126">*pcPasses*</span></span>

<span data-ttu-id="a1f41-127">Quando si avvia un'attività di deframmentazione in linea, questo parametro di input imposta il numero massimo di passaggi di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="a1f41-128">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul numero di passaggi eseguiti.</span><span class="sxs-lookup"><span data-stu-id="a1f41-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="a1f41-129">Quando questo parametro è impostato su NULL, il numero di sessioni di deframmentazione in linea è illimitato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="a1f41-130">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="a1f41-130">*pcSeconds*</span></span>

<span data-ttu-id="a1f41-131">Quando si avvia un'attività di deframmentazione in linea, questo parametro di input imposta il tempo massimo per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="a1f41-132">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="a1f41-133">Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="a1f41-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a1f41-134">*grbit*</span></span>

<span data-ttu-id="a1f41-135">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1f41-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1f41-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a1f41-136">Value</span></span></p></th>
<th><p><span data-ttu-id="a1f41-137">Significato</span><span class="sxs-lookup"><span data-stu-id="a1f41-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="a1f41-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="a1f41-139">Deframmenta la porzione di spazio disponibile nell'allocazione dello spazio del database ESE.</span><span class="sxs-lookup"><span data-stu-id="a1f41-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="a1f41-140">Lo spazio del database è suddiviso in due tipi, spazio di proprietà e spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="a1f41-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="a1f41-141">Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'utilizzo rispettivamente nella tabella o nell'indice.</span><span class="sxs-lookup"><span data-stu-id="a1f41-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="a1f41-142">Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea più che lo spazio di proprietà o i dati di tabella o di indice.</span><span class="sxs-lookup"><span data-stu-id="a1f41-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="a1f41-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="a1f41-144">Avvia una nuova attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="a1f41-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="a1f41-146">Arresta un'attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a1f41-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1f41-147">Return Value</span></span>

<span data-ttu-id="a1f41-148">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a1f41-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a1f41-149">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f41-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1f41-150">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a1f41-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="a1f41-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f41-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a1f41-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a1f41-153">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a1f41-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a1f41-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a1f41-155">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a1f41-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1f41-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a1f41-157">Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="a1f41-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="a1f41-159">La sessione specificata si trova nello stato pronto per il commit e non può avviare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a1f41-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a1f41-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a1f41-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="a1f41-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a1f41-162">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a1f41-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a1f41-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="a1f41-164">L'ID del database specificato non corrisponde a un database noto nell'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a1f41-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a1f41-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a1f41-166">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="a1f41-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a1f41-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1f41-168">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a1f41-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a1f41-170">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a1f41-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a1f41-171">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a1f41-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a1f41-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1f41-173">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="a1f41-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1f41-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a1f41-175">La sessione specificata ha solo privilegi di sola lettura e non può avviare un'attività che può eseguire un aggiornamento, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a1f41-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a1f41-177">Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a1f41-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="a1f41-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="a1f41-179">È stata passata l'opzione JET_bitDefragmentBatchStart, ma un'attività di deframmentazione sta già eseguendo la deframmentazione nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f41-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="a1f41-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="a1f41-181">È stata passata l'opzione JET_bitDefragmentBatchStop, ma l'attività di deframmentazione non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1f41-182">In caso di esito positivo, viene eseguita l'azione richiesta di avvio di un'attività di deframmentazione per i dati specificati con le opzioni specificate oppure viene eseguita l'azione di arresto di un'attività di deframmentazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a1f41-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="a1f41-183">In caso di errore, l'azione richiesta di avvio o arresto di un processo di deframmentazione in linea non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="a1f41-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="a1f41-184">Non si verificano altri effetti collaterali.</span><span class="sxs-lookup"><span data-stu-id="a1f41-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a1f41-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1f41-185">Remarks</span></span>

<span data-ttu-id="a1f41-186">La deframmentazione in linea viene controllata sia dall'impostazione di un parametro sia da questa API.</span><span class="sxs-lookup"><span data-stu-id="a1f41-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="a1f41-187">Il valore predefinito del parametro di sistema è JET_OnlineDefragAll, ovvero la deframmentazione è abilitata per tutte le strutture di dati supportate.</span><span class="sxs-lookup"><span data-stu-id="a1f41-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="a1f41-188">Tuttavia, utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione in linea o abilitarla selettivamente solo per gli alberi dello spazio del database, solo per i database, solo per i file di flusso o una combinazione di queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="a1f41-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="a1f41-189">Se l'impostazione di sistema per la deframmentazione in linea è impostata su un'impostazione obsoleta, **JetDefragment** considererà l'impostazione come JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="a1f41-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="a1f41-190">È possibile eseguire al massimo un'attività per ogni database.</span><span class="sxs-lookup"><span data-stu-id="a1f41-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="a1f41-191">L'attività viene eseguita come thread nel processo che ospita ESE.</span><span class="sxs-lookup"><span data-stu-id="a1f41-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="a1f41-192">La sessione utilizzata per avviare l'attività di deframmentazione in linea può essere successivamente utilizzata per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca la propria sessione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="a1f41-193">La sessione specificata viene utilizzata solo per verificare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente utilizzata per le operazioni di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="a1f41-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a1f41-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1f41-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-196">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a1f41-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-198">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a1f41-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-199"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-200">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a1f41-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-201"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-202">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a1f41-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-203"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-204">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a1f41-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-205"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-206">Implementato come <strong>JetDefragmentW</strong> (Unicode) e <strong>JetDefragmentA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a1f41-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a1f41-207">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a1f41-207">See Also</span></span>

[<span data-ttu-id="a1f41-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a1f41-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a1f41-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a1f41-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a1f41-210">JetCompact</span><span class="sxs-lookup"><span data-stu-id="a1f41-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="a1f41-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a1f41-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="a1f41-212">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a1f41-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a1f41-213">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a1f41-213">JetStopService</span></span>](./jetstopservice-function.md)
