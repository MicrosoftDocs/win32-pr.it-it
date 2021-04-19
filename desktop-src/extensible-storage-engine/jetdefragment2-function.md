---
description: 'Altre informazioni su: funzione JetDefragment2'
title: JetDefragment2 (funzione)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323810"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="443fa-103">JetDefragment2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="443fa-103">JetDefragment2 Function</span></span>


<span data-ttu-id="443fa-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="443fa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="443fa-105">JetDefragment2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="443fa-105">JetDefragment2 Function</span></span>

<span data-ttu-id="443fa-106">La funzione **JetDefragment2** consente di avviare e arrestare le attività di deframmentazione del database che consentono di migliorare l'organizzazione dei dati all'interno di un database, con un parametro di callback disponibile per segnalare lo stato della deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="443fa-107">Questa operazione viene eseguita per limitare la crescita del database utilizzando l'allocazione dei dischi esistente in modo più efficiente all'interno del database.</span><span class="sxs-lookup"><span data-stu-id="443fa-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="443fa-108">Consente inoltre di ridurre working set assicurando che i dati vengano compressi in modo più accurato.</span><span class="sxs-lookup"><span data-stu-id="443fa-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="443fa-109">Infine, può migliorare le prestazioni dell'applicazione velocizzando le operazioni comuni tramite una migliore organizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="443fa-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="443fa-110">**Windows XP:**  **JetDefragment2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="443fa-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="443fa-111">**JetDefragment2** contiene anche un parametro della funzione di callback che viene usato per segnalare lo stato di avanzamento del processo di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="443fa-112">La deframmentazione del database è un'operazione online e non interrompe le normali attività del database, ad esempio le operazioni di query o gli aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="443fa-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="443fa-113">**JetDefragment2** non esegue inoltre una copia di tutti i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="443fa-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="443fa-114">Al contrario, deframmenta un database sul posto.</span><span class="sxs-lookup"><span data-stu-id="443fa-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="443fa-115">Infine, **JetDefragment2** ripristina lo spazio interno del database per riutilizzarlo, ma non rilascia spazio in eccesso al sistema operativo file System.</span><span class="sxs-lookup"><span data-stu-id="443fa-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="443fa-116">Il formato risultante dei dati può essere molto più efficiente, ma in genere non è ottimale.</span><span class="sxs-lookup"><span data-stu-id="443fa-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="443fa-117">La deframmentazione è limitata a rilasciare le pagine del database per riutilizzarle che contengono dati che sono già stati eliminati logicamente.</span><span class="sxs-lookup"><span data-stu-id="443fa-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="443fa-118">La deframmentazione rende inoltre disponibili le pagine del database da riutilizzare in alcuni casi combinando i dati di due pagine quando possono essere inseriti in una singola pagina.</span><span class="sxs-lookup"><span data-stu-id="443fa-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="443fa-119">Questa operazione è diversa da [JetCompact](./jetcompact-function.md) , che rende una copia di un database di sola lettura in un formato altamente ottimale.</span><span class="sxs-lookup"><span data-stu-id="443fa-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="443fa-120">Parametri</span><span class="sxs-lookup"><span data-stu-id="443fa-120">Parameters</span></span>

<span data-ttu-id="443fa-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="443fa-121">*sesid*</span></span>

<span data-ttu-id="443fa-122">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="443fa-122">The session to use for this call.</span></span>

<span data-ttu-id="443fa-123">*dbid*</span><span class="sxs-lookup"><span data-stu-id="443fa-123">*dbid*</span></span>

<span data-ttu-id="443fa-124">Database da deframmentare.</span><span class="sxs-lookup"><span data-stu-id="443fa-124">The database to defragment.</span></span>

<span data-ttu-id="443fa-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="443fa-125">*szTableName*</span></span>

<span data-ttu-id="443fa-126">Parametro non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="443fa-126">Unused parameter.</span></span> <span data-ttu-id="443fa-127">La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.</span><span class="sxs-lookup"><span data-stu-id="443fa-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="443fa-128">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="443fa-128">*pcPasses*</span></span>

<span data-ttu-id="443fa-129">Quando si avvia un'attività di deframmentazione in linea, questo parametro di input facoltativo imposta il numero massimo di passaggi di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="443fa-130">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output facoltativo viene impostato sul numero di passaggi eseguiti.</span><span class="sxs-lookup"><span data-stu-id="443fa-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="443fa-131">Quando questo parametro è impostato su NULL, il numero di sessioni di deframmentazione in linea è illimitato.</span><span class="sxs-lookup"><span data-stu-id="443fa-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="443fa-132">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="443fa-132">*pcSeconds*</span></span>

<span data-ttu-id="443fa-133">Quando si avvia un'attività di deframmentazione in linea, questo parametro di input facoltativo imposta il tempo massimo per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="443fa-134">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output facoltativo viene impostato sul periodo di tempo utilizzato per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="443fa-135">Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.</span><span class="sxs-lookup"><span data-stu-id="443fa-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="443fa-136">*callback*</span><span class="sxs-lookup"><span data-stu-id="443fa-136">*callback*</span></span>

<span data-ttu-id="443fa-137">Funzione di callback che la deframmentazione chiama regolarmente per segnalare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="443fa-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="443fa-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="443fa-138">*grbit*</span></span>

<span data-ttu-id="443fa-139">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="443fa-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="443fa-140">Valore</span><span class="sxs-lookup"><span data-stu-id="443fa-140">Value</span></span></p></th>
<th><p><span data-ttu-id="443fa-141">Significato</span><span class="sxs-lookup"><span data-stu-id="443fa-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="443fa-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="443fa-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="443fa-143">Questa opzione consente di deframmentare la porzione di spazio disponibile nell'allocazione dello spazio del database ESE.</span><span class="sxs-lookup"><span data-stu-id="443fa-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="443fa-144">Lo spazio del database è suddiviso in due tipi, spazio di proprietà e spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="443fa-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="443fa-145">Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'utilizzo rispettivamente nella tabella o nell'indice.</span><span class="sxs-lookup"><span data-stu-id="443fa-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="443fa-146">Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea in modo più che spazio di proprietà o dati di tabella o di indice.</span><span class="sxs-lookup"><span data-stu-id="443fa-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="443fa-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="443fa-148">Questa opzione viene usata per avviare una nuova attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="443fa-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="443fa-150">Questa opzione viene utilizzata per arrestare un'attività di deframmentazione avviata esistente.</span><span class="sxs-lookup"><span data-stu-id="443fa-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="443fa-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="443fa-152">Questa opzione viene utilizzata per deframmentare un albero B.</span><span class="sxs-lookup"><span data-stu-id="443fa-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="443fa-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="443fa-153">Return Value</span></span>

<span data-ttu-id="443fa-154">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="443fa-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="443fa-155">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="443fa-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="443fa-156">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="443fa-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="443fa-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="443fa-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="443fa-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="443fa-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="443fa-159">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="443fa-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="443fa-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="443fa-161">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="443fa-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="443fa-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="443fa-163">Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="443fa-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="443fa-165">La sessione specificata si trova nello stato pronto per il commit e non può avviare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="443fa-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="443fa-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="443fa-167">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="443fa-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="443fa-168">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="443fa-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="443fa-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="443fa-170">L'ID del database specificato non corrisponde a un database noto nell'istanza di.</span><span class="sxs-lookup"><span data-stu-id="443fa-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="443fa-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="443fa-172">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="443fa-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="443fa-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="443fa-174">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="443fa-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="443fa-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="443fa-176">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="443fa-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="443fa-177">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="443fa-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="443fa-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="443fa-179">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="443fa-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="443fa-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="443fa-181">La sessione specificata ha solo privilegi di sola lettura e non può avviare un'attività che può eseguire un aggiornamento, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="443fa-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="443fa-183">Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="443fa-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="443fa-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="443fa-185">È stata passata l'opzione JET_bitDefragmentBatchStart, ma un'attività di deframmentazione sta già eseguendo la deframmentazione nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="443fa-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="443fa-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="443fa-187">È stata passata l'opzione JET_bitDefragmentBatchStop, ma l'attività di deframmentazione non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="443fa-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="443fa-188">In caso di esito positivo, viene eseguita l'azione richiesta di avvio di un'attività di deframmentazione per i dati specificati con le opzioni specificate oppure viene eseguita l'azione di arresto di un'attività di deframmentazione esistente.</span><span class="sxs-lookup"><span data-stu-id="443fa-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="443fa-189">In caso di errore, l'azione richiesta di avvio o arresto di un processo di deframmentazione in linea non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="443fa-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="443fa-190">Non si verificano altri effetti collaterali.</span><span class="sxs-lookup"><span data-stu-id="443fa-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="443fa-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="443fa-191">Remarks</span></span>

<span data-ttu-id="443fa-192">La deframmentazione in linea viene controllata sia dall'impostazione di un parametro sia da questa API.</span><span class="sxs-lookup"><span data-stu-id="443fa-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="443fa-193">Il valore predefinito del parametro di sistema è JET_OnlineDefragAll, ovvero la deframmentazione è abilitata per tutte le strutture di dati supportate.</span><span class="sxs-lookup"><span data-stu-id="443fa-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="443fa-194">Tuttavia, utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione in linea o abilitarla selettivamente solo per gli alberi dello spazio del database, solo per i database, solo per i file di flusso o una combinazione di queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="443fa-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="443fa-195">Se l'impostazione di sistema per la deframmentazione in linea è di un'impostazione obsoleta, **JetDefragment2** considererà l'impostazione come JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="443fa-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="443fa-196">È possibile eseguire al massimo un'attività per ogni database.</span><span class="sxs-lookup"><span data-stu-id="443fa-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="443fa-197">L'attività viene eseguita come thread nel processo che ospita ESE.</span><span class="sxs-lookup"><span data-stu-id="443fa-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="443fa-198">La sessione utilizzata per avviare l'attività di deframmentazione in linea può essere successivamente utilizzata per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca la propria sessione.</span><span class="sxs-lookup"><span data-stu-id="443fa-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="443fa-199">La sessione specificata viene utilizzata solo per verificare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente utilizzata per le operazioni di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="443fa-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="443fa-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="443fa-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="443fa-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-202">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="443fa-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-204">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="443fa-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-205"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-206">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="443fa-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-207"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-208">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="443fa-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="443fa-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-210">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="443fa-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="443fa-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="443fa-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="443fa-212">Implementato come <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="443fa-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="443fa-213">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="443fa-213">See Also</span></span>

[<span data-ttu-id="443fa-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="443fa-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="443fa-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="443fa-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="443fa-216">JetCompact</span><span class="sxs-lookup"><span data-stu-id="443fa-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="443fa-217">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="443fa-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="443fa-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="443fa-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="443fa-219">JetStopService</span><span class="sxs-lookup"><span data-stu-id="443fa-219">JetStopService</span></span>](./jetstopservice-function.md)
