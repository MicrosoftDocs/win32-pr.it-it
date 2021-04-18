---
description: 'Altre informazioni su: funzione JetSetTableSequential'
title: JetSetTableSequential (funzione)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306212"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="5a054-103">JetSetTableSequential (funzione)</span><span class="sxs-lookup"><span data-stu-id="5a054-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="5a054-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a054-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="5a054-105">JetSetTableSequential (funzione)</span><span class="sxs-lookup"><span data-stu-id="5a054-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="5a054-106">La funzione **JetSetTableSequential** notifica al motore di database che l'applicazione esegue l'analisi dell'intero indice corrente contenente un determinato cursore.</span><span class="sxs-lookup"><span data-stu-id="5a054-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="5a054-107">Di conseguenza, i metodi usati per accedere ai dati dell'indice verranno ottimizzati per rendere questo scenario il più rapido possibile.</span><span class="sxs-lookup"><span data-stu-id="5a054-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="5a054-108">**Windows XP:**  **JetSetTableSequential** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a054-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5a054-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a054-109">Parameters</span></span>

<span data-ttu-id="5a054-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5a054-110">*sesid*</span></span>

<span data-ttu-id="5a054-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5a054-111">The session to use for this call.</span></span>

<span data-ttu-id="5a054-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5a054-112">*tableid*</span></span>

<span data-ttu-id="5a054-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5a054-113">The cursor to use for this call.</span></span>

<span data-ttu-id="5a054-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5a054-114">*grbit*</span></span>

<span data-ttu-id="5a054-115">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a054-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a054-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5a054-116">Value</span></span></p></th>
<th><p><span data-ttu-id="5a054-117">Significato</span><span class="sxs-lookup"><span data-stu-id="5a054-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a054-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="5a054-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="5a054-119">Questa opzione viene utilizzata per eseguire l'indicizzazione nella direzione avanti.</span><span class="sxs-lookup"><span data-stu-id="5a054-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="5a054-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a054-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a054-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="5a054-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="5a054-122">Questa opzione viene utilizzata per eseguire l'indicizzazione nella direzione all'indietro.</span><span class="sxs-lookup"><span data-stu-id="5a054-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="5a054-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a054-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5a054-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a054-124">Return Value</span></span>

<span data-ttu-id="5a054-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5a054-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5a054-126">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5a054-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a054-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a054-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="5a054-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a054-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a054-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5a054-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5a054-130">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state inattivo in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5a054-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a054-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5a054-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5a054-132">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="5a054-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5a054-133"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a054-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a054-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5a054-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5a054-135">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5a054-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a054-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5a054-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a054-137">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5a054-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a054-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5a054-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a054-139">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5a054-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a054-140">Se questa funzione ha esito positivo, l'indice corrente del cursore viene ottimizzato per un'analisi sequenziale dell'intero indice.</span><span class="sxs-lookup"><span data-stu-id="5a054-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="5a054-141">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="5a054-141">No change to the database state will occur.</span></span>

<span data-ttu-id="5a054-142">Se questa funzione ha esito negativo, non verrà apportata alcuna modifica alla configurazione del cursore.</span><span class="sxs-lookup"><span data-stu-id="5a054-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="5a054-143">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="5a054-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5a054-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a054-144">Remarks</span></span>

<span data-ttu-id="5a054-145">Se l'applicazione deve eseguire un'analisi efficiente di un subset noto di un indice, viene anche eseguita un'ottimizzazione simile ogni volta che viene stabilito un intervallo di indice usando [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="5a054-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="5a054-146">Questa ottimizzazione è disponibile solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a054-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="5a054-147">Se l'applicazione deve eseguire un'analisi efficiente di un subset sconosciuto di un indice, non è necessario eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="5a054-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="5a054-148">Il motore può rilevare automaticamente il comportamento di analisi e recuperare i dati in anticipo.</span><span class="sxs-lookup"><span data-stu-id="5a054-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="5a054-149">Questo comportamento non è tuttavia troppo aggressivo.</span><span class="sxs-lookup"><span data-stu-id="5a054-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="5a054-150">Questa ottimizzazione renderà più efficiente l'analisi dell'indice primario e renderà efficiente l'analisi dei dati delle voci di indice in un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="5a054-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="5a054-151">Non effettuerà l'analisi di un indice secondario durante il recupero dei dati del record in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="5a054-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="5a054-152">Questo perché il motore non esegue un read-ahead sui dati del record.</span><span class="sxs-lookup"><span data-stu-id="5a054-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5a054-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a054-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a054-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5a054-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a054-155">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a054-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a054-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5a054-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a054-157">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a054-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a054-158"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5a054-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a054-159">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5a054-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a054-160"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5a054-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5a054-161">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5a054-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a054-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5a054-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5a054-163">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5a054-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5a054-164">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5a054-164">See Also</span></span>

[<span data-ttu-id="5a054-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a054-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a054-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a054-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a054-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5a054-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5a054-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5a054-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5a054-169">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="5a054-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="5a054-170">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5a054-170">JetStopService</span></span>](./jetstopservice-function.md)
