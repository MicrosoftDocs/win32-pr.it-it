---
description: Altre informazioni sulla funzione JetDefragment2
title: Funzione JetDefragment2
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
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838805"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="1ea33-103">Funzione JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="1ea33-103">JetDefragment2 Function</span></span>


<span data-ttu-id="1ea33-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1ea33-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="1ea33-105">Funzione JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="1ea33-105">JetDefragment2 Function</span></span>

<span data-ttu-id="1ea33-106">La **funzione JetDefragment2** avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database, con un parametro di callback disponibile per segnalare lo stato di avanzamento della deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="1ea33-107">Questa operazione viene eseguita per limitare l'aumento delle dimensioni del database usando l'allocazione dei dischi esistente in modo più efficiente all'interno del database.</span><span class="sxs-lookup"><span data-stu-id="1ea33-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="1ea33-108">Può anche ridurre i working set assicurando che i dati sono più imballati.</span><span class="sxs-lookup"><span data-stu-id="1ea33-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="1ea33-109">Infine, può migliorare le prestazioni dell'applicazione accelerando le operazioni comuni tramite una migliore organizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1ea33-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="1ea33-110">**Windows XP:**  **JetDefragment2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ea33-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="1ea33-111">**JetDefragment2** contiene anche un parametro della funzione di callback usato per segnalare lo stato del processo di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="1ea33-112">La deframmentazione del database è un'operazione online e non interrompe la normale attività del database, ad esempio operazioni di query o aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="1ea33-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="1ea33-113">**JetDefragment2** non crea inoltre una copia di tutti i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="1ea33-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="1ea33-114">Al contrario, deframmenta un database sul posto.</span><span class="sxs-lookup"><span data-stu-id="1ea33-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="1ea33-115">Infine, **JetDefragment2** recupera lo spazio interno del database per il nuovo utilizzo, ma non rilascia spazio in eccesso al sistema operativo file system.</span><span class="sxs-lookup"><span data-stu-id="1ea33-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="1ea33-116">Il formato risultante dei dati può essere molto più efficiente, ma non è in genere ottimale.</span><span class="sxs-lookup"><span data-stu-id="1ea33-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="1ea33-117">La deframmentazione è limitata al rilascio di pagine di database per il nuovo utilizzo che contengono dati già eliminati logicamente.</span><span class="sxs-lookup"><span data-stu-id="1ea33-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="1ea33-118">La deframmentazione rende anche disponibili le pagine di database per il nuovo uso in alcuni casi combinando i dati di due pagine quando possono essere adattati a una singola pagina.</span><span class="sxs-lookup"><span data-stu-id="1ea33-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="1ea33-119">Questa operazione è diversa [da JetCompact,](./jetcompact-function.md) che rende una copia di un database di sola lettura in un formato altamente ottimale.</span><span class="sxs-lookup"><span data-stu-id="1ea33-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="1ea33-120">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ea33-120">Parameters</span></span>

<span data-ttu-id="1ea33-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1ea33-121">*sesid*</span></span>

<span data-ttu-id="1ea33-122">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1ea33-122">The session to use for this call.</span></span>

<span data-ttu-id="1ea33-123">*Dbid*</span><span class="sxs-lookup"><span data-stu-id="1ea33-123">*dbid*</span></span>

<span data-ttu-id="1ea33-124">Database da deframmentare.</span><span class="sxs-lookup"><span data-stu-id="1ea33-124">The database to defragment.</span></span>

<span data-ttu-id="1ea33-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="1ea33-125">*szTableName*</span></span>

<span data-ttu-id="1ea33-126">A *volte szTableName* è obbligatorio e talvolta non è consentito:</span><span class="sxs-lookup"><span data-stu-id="1ea33-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="1ea33-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1ea33-127">*grbit*</span></span> | <span data-ttu-id="1ea33-128">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="1ea33-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="1ea33-129">Deve essere `NULL`.</span><span class="sxs-lookup"><span data-stu-id="1ea33-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="1ea33-130">Specifica il nome della tabella o dell'oggetto B da deframmentare.</span><span class="sxs-lookup"><span data-stu-id="1ea33-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="1ea33-131">*Altro*</span><span class="sxs-lookup"><span data-stu-id="1ea33-131">*other*</span></span> | <span data-ttu-id="1ea33-132">Deve essere `NULL`.</span><span class="sxs-lookup"><span data-stu-id="1ea33-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="1ea33-133">La deframmentazione viene eseguita per l'intero database descritto dall'ID database specificato.</span><span class="sxs-lookup"><span data-stu-id="1ea33-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="1ea33-134">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="1ea33-134">*pcPasses*</span></span>

<span data-ttu-id="1ea33-135">Quando si avvia un'attività di deframmentazione online, questo parametro di input facoltativo imposta il numero massimo di passaggi di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="1ea33-136">Quando si arresta un'attività di deframmentazione online, questo buffer di output facoltativo viene impostato sul numero di passaggi eseguiti.</span><span class="sxs-lookup"><span data-stu-id="1ea33-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="1ea33-137">Quando questo parametro è impostato su NULL, il numero di passaggi di deframmentazione online è illimitato.</span><span class="sxs-lookup"><span data-stu-id="1ea33-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="1ea33-138">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="1ea33-138">*pcSeconds*</span></span>

<span data-ttu-id="1ea33-139">Quando si avvia un'attività di deframmentazione online, questo parametro di input facoltativo imposta il tempo massimo per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="1ea33-140">Quando si arresta un'attività di deframmentazione online, questo buffer di output facoltativo viene impostato sul periodo di tempo utilizzato per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="1ea33-141">Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.</span><span class="sxs-lookup"><span data-stu-id="1ea33-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="1ea33-142">*callback*</span><span class="sxs-lookup"><span data-stu-id="1ea33-142">*callback*</span></span>

<span data-ttu-id="1ea33-143">Funzione di callback che la deframmentazione chiama regolarmente per segnalare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="1ea33-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="1ea33-144">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1ea33-144">*grbit*</span></span> | <span data-ttu-id="1ea33-145">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="1ea33-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="1ea33-146">Deve essere `NULL`.</span><span class="sxs-lookup"><span data-stu-id="1ea33-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="1ea33-147">Deve essere `NULL`.</span><span class="sxs-lookup"><span data-stu-id="1ea33-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="1ea33-148">*Altro*</span><span class="sxs-lookup"><span data-stu-id="1ea33-148">*other*</span></span> | <span data-ttu-id="1ea33-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1ea33-149">Optional.</span></span>


<span data-ttu-id="1ea33-150">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1ea33-150">*grbit*</span></span>

<span data-ttu-id="1ea33-151">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ea33-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea33-152">Valore</span><span class="sxs-lookup"><span data-stu-id="1ea33-152">Value</span></span></p></th>
<th><p><span data-ttu-id="1ea33-153">Significato</span><span class="sxs-lookup"><span data-stu-id="1ea33-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="1ea33-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea33-155">Questa opzione viene usata per deframmentare la parte di spazio disponibile dell'allocazione dello spazio del database ESE.</span><span class="sxs-lookup"><span data-stu-id="1ea33-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="1ea33-156">Lo spazio del database è suddiviso in due tipi, lo spazio di proprietà e lo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="1ea33-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="1ea33-157">Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'uso rispettivamente all'interno della tabella o dell'indice.</span><span class="sxs-lookup"><span data-stu-id="1ea33-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="1ea33-158">Lo spazio disponibile è molto più dinamico nel comportamento e richiede più deframmentazione online rispetto allo spazio di proprietà, alla tabella o ai dati dell'indice.</span><span class="sxs-lookup"><span data-stu-id="1ea33-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="1ea33-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="1ea33-160">Questa opzione viene usata per avviare una nuova attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="1ea33-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="1ea33-162">Questa opzione viene usata per arrestare un'attività di deframmentazione avviata esistente.</span><span class="sxs-lookup"><span data-stu-id="1ea33-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="1ea33-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="1ea33-164">Questa opzione viene usata per deframmentare un albero B, specificato da szTableName.</span><span class="sxs-lookup"><span data-stu-id="1ea33-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="1ea33-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="1ea33-166">Questa opzione viene usata per chiamare OLD2 sull'intero database.</span><span class="sxs-lookup"><span data-stu-id="1ea33-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1ea33-167">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ea33-167">Return Value</span></span>

<span data-ttu-id="1ea33-168">Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ea33-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1ea33-169">Per altre informazioni sui possibili errori ESE, vedere Errori del motore di archiviazione [estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1ea33-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea33-170">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1ea33-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="1ea33-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ea33-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1ea33-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1ea33-173">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1ea33-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1ea33-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1ea33-175">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></span><span class="sxs-lookup"><span data-stu-id="1ea33-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="1ea33-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea33-177">Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="1ea33-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="1ea33-179">La sessione specificata è nello stato pronto per il commit e non può iniziare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1ea33-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1ea33-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1ea33-181">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</span><span class="sxs-lookup"><span data-stu-id="1ea33-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="1ea33-182">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1ea33-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="1ea33-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="1ea33-184">L'ID di database specificato non corrisponde a un database noto nell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1ea33-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1ea33-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1ea33-186">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="1ea33-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1ea33-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1ea33-188">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1ea33-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1ea33-190">La stessa sessione non può essere usata per più thread contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1ea33-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="1ea33-191">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1ea33-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1ea33-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1ea33-193">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="1ea33-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea33-195">La sessione specificata ha solo privilegi di sola lettura e non può avviare un'attività che può eseguire un aggiornamento, inclusa la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1ea33-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1ea33-197">Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="1ea33-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="1ea33-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="1ea33-199">L JET_bitDefragmentBatchStart è stata passata, ma un'attività di deframmentazione sta già eseguendo la deframmentazione nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="1ea33-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="1ea33-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="1ea33-201">L JET_bitDefragmentBatchStop è stata passata, ma non è attualmente in esecuzione alcuna attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ea33-202">In caso di esito positivo, viene eseguita l'azione richiesta di avvio di un'attività di deframmentazione per dati con opzioni specificate oppure viene eseguita l'azione di arresto di un'attività di deframmentazione esistente.</span><span class="sxs-lookup"><span data-stu-id="1ea33-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="1ea33-203">In caso di errore, l'azione richiesta di avvio o arresto di un processo di deframmentazione online non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="1ea33-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="1ea33-204">Non si verificano altri effetti collaterali.</span><span class="sxs-lookup"><span data-stu-id="1ea33-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1ea33-205">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ea33-205">Remarks</span></span>

<span data-ttu-id="1ea33-206">La deframmentazione online è controllata sia da un'impostazione di parametro che da questa API.</span><span class="sxs-lookup"><span data-stu-id="1ea33-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="1ea33-207">Il valore predefinito del parametro di sistema JET_OnlineDefragAll, ovvero la deframmentazione è abilitata per tutte le strutture di dati supportate.</span><span class="sxs-lookup"><span data-stu-id="1ea33-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="1ea33-208">Tuttavia, usando [JetSetSystemParameter,](./jetsetsystemparameter-function.md)è possibile disabilitare la deframmentazione online o abilitarla in modo selettivo solo per gli alberi dello spazio del database, solo per i database, solo per i file di streaming o per qualsiasi combinazione di queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="1ea33-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="1ea33-209">Se l'impostazione di sistema per la deframmentazione in linea è su un'impostazione obsoleta, **JetDefragment2** considera l'impostazione JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="1ea33-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="1ea33-210">Può essere presente al massimo un'attività in esecuzione per ogni database.</span><span class="sxs-lookup"><span data-stu-id="1ea33-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="1ea33-211">L'attività viene eseguita come thread nel processo che ospita ESE.</span><span class="sxs-lookup"><span data-stu-id="1ea33-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="1ea33-212">La sessione usata per avviare l'attività di deframmentazione online può essere usata successivamente per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca la propria sessione.</span><span class="sxs-lookup"><span data-stu-id="1ea33-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="1ea33-213">La sessione specificata viene usata solo per controllare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente usata per le operazioni di deframmentazione stesse.</span><span class="sxs-lookup"><span data-stu-id="1ea33-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1ea33-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ea33-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-215"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-216">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ea33-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-217"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-218">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1ea33-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-219"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-220">Dichiarato in Esent.h.</span><span class="sxs-lookup"><span data-stu-id="1ea33-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-221"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-222">Usare ESENT.lib.</span><span class="sxs-lookup"><span data-stu-id="1ea33-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea33-223"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-224">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1ea33-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea33-225"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1ea33-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea33-226">Implementato come <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1ea33-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1ea33-227">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1ea33-227">See Also</span></span>

[<span data-ttu-id="1ea33-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1ea33-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1ea33-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1ea33-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1ea33-230">JetCompact</span><span class="sxs-lookup"><span data-stu-id="1ea33-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="1ea33-231">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="1ea33-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="1ea33-232">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="1ea33-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="1ea33-233">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1ea33-233">JetStopService</span></span>](./jetstopservice-function.md)
