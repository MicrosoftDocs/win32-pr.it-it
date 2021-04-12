---
description: 'Altre informazioni su: funzione JetComputeStats'
title: JetComputeStats (funzione)
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234094"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="69d26-103">JetComputeStats (funzione)</span><span class="sxs-lookup"><span data-stu-id="69d26-103">JetComputeStats Function</span></span>


<span data-ttu-id="69d26-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="69d26-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="69d26-105">JetComputeStats (funzione)</span><span class="sxs-lookup"><span data-stu-id="69d26-105">JetComputeStats Function</span></span>

<span data-ttu-id="69d26-106">La funzione **JetComputeStats** percorre ogni indice di una tabella per calcolare esattamente il numero di voci in un indice e il numero di chiavi distinte in un indice.</span><span class="sxs-lookup"><span data-stu-id="69d26-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="69d26-107">Queste informazioni, insieme al numero di pagine di database allocate per un indice e all'ora corrente del calcolo, vengono archiviate nei metadati dell'indice nel database.</span><span class="sxs-lookup"><span data-stu-id="69d26-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="69d26-108">Questi dati possono essere successivamente recuperati con le operazioni relative alle informazioni.</span><span class="sxs-lookup"><span data-stu-id="69d26-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="69d26-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="69d26-109">Parameters</span></span>

<span data-ttu-id="69d26-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="69d26-110">*sesid*</span></span>

<span data-ttu-id="69d26-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="69d26-111">The session to use for this call.</span></span>

<span data-ttu-id="69d26-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="69d26-112">*tableid*</span></span>

<span data-ttu-id="69d26-113">Cursore che verrà utilizzato per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="69d26-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="69d26-114">Descrive la tabella in cui calcolare le statistiche.</span><span class="sxs-lookup"><span data-stu-id="69d26-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="69d26-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69d26-115">Return Value</span></span>

<span data-ttu-id="69d26-116">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="69d26-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="69d26-117">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="69d26-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69d26-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="69d26-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="69d26-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69d26-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69d26-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="69d26-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="69d26-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="69d26-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="69d26-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="69d26-123">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="69d26-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69d26-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="69d26-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="69d26-125">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="69d26-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="69d26-126">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="69d26-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="69d26-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="69d26-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="69d26-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69d26-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="69d26-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="69d26-130">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="69d26-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="69d26-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="69d26-132">Si è verificato un errore che richiede l'esecuzione del rollback di tutte le modifiche, ma il rollback della transazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="69d26-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69d26-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="69d26-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="69d26-134">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="69d26-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="69d26-135">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="69d26-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="69d26-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="69d26-137">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="69d26-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69d26-138">In seguito all'esito positivo, le statistiche aggiornate vengono archiviate nei cataloghi del database per la tabella descritta con il cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="69d26-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="69d26-139">In caso di errore, non viene eseguito alcun aggiornamento del tipo di dati al database.</span><span class="sxs-lookup"><span data-stu-id="69d26-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="69d26-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="69d26-140">Remarks</span></span>

<span data-ttu-id="69d26-141">Questa operazione può essere un consumo di risorse perché ogni indice di una tabella deve essere analizzato interamente.</span><span class="sxs-lookup"><span data-stu-id="69d26-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="69d26-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) può essere utilizzato per ottenere una stima approssimativa del numero di voci in un indice, ma non può stimare il numero di valori distinct in un indice.</span><span class="sxs-lookup"><span data-stu-id="69d26-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="69d26-143">I dati calcolati da questa operazione iniziano a diventare obsoleti e la tabella viene aggiornata successivamente.</span><span class="sxs-lookup"><span data-stu-id="69d26-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="69d26-144">Gli aggiornamenti al database creati da **JetComputeStats** vengono eseguiti in modo lazy.</span><span class="sxs-lookup"><span data-stu-id="69d26-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="69d26-145">Ciò significa che nessuno scaricamento del log sarà accompagnato da questa operazione e un arresto anomalo del sistema successivo a un ritorno di JET_errSuccess da **JetComputeStats** può comunque causare la perdita di questi aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="69d26-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="69d26-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69d26-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69d26-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="69d26-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="69d26-148">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="69d26-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="69d26-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="69d26-150">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="69d26-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69d26-151"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="69d26-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="69d26-152">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="69d26-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69d26-153"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="69d26-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="69d26-154">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="69d26-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69d26-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="69d26-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="69d26-156">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="69d26-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="69d26-157">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="69d26-157">See Also</span></span>

[<span data-ttu-id="69d26-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="69d26-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="69d26-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="69d26-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="69d26-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="69d26-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="69d26-161">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="69d26-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="69d26-162">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="69d26-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="69d26-163">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="69d26-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="69d26-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="69d26-164">JetStopService</span></span>](./jetstopservice-function.md)
