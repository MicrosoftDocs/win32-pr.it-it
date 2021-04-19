---
description: 'Altre informazioni su: funzione JetRollback'
title: JetRollback (funzione)
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318083"
---
# <a name="jetrollback-function"></a><span data-ttu-id="edcef-103">JetRollback (funzione)</span><span class="sxs-lookup"><span data-stu-id="edcef-103">JetRollback Function</span></span>


<span data-ttu-id="edcef-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="edcef-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="edcef-105">JetRollback (funzione)</span><span class="sxs-lookup"><span data-stu-id="edcef-105">JetRollback Function</span></span>

<span data-ttu-id="edcef-106">La funzione **JetRollback** Annulla le modifiche apportate allo stato del database e torna all'ultimo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="edcef-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="edcef-107">**JetRollback** chiuderà anche tutti i cursori aperti durante il punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="edcef-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="edcef-108">Se il punto di salvataggio più esterno è annullato, la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="edcef-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="edcef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="edcef-109">Parameters</span></span>

<span data-ttu-id="edcef-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="edcef-110">*sesid*</span></span>

<span data-ttu-id="edcef-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="edcef-111">The session to use for this call.</span></span>

<span data-ttu-id="edcef-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="edcef-112">*grbit*</span></span>

<span data-ttu-id="edcef-113">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="edcef-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edcef-114">Valore</span><span class="sxs-lookup"><span data-stu-id="edcef-114">Value</span></span></p></th>
<th><p><span data-ttu-id="edcef-115">Significato</span><span class="sxs-lookup"><span data-stu-id="edcef-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edcef-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="edcef-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="edcef-117">Questa opzione richiede che vengano annullate tutte le modifiche apportate allo stato del database durante tutti i punti di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="edcef-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="edcef-118">Di conseguenza, la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="edcef-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="edcef-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edcef-119">Return Value</span></span>

<span data-ttu-id="edcef-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="edcef-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="edcef-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="edcef-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edcef-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="edcef-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="edcef-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edcef-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edcef-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="edcef-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="edcef-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="edcef-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="edcef-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="edcef-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="edcef-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="edcef-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="edcef-129">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="edcef-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="edcef-130">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="edcef-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="edcef-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="edcef-132">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="edcef-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="edcef-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="edcef-134">Operazione non riuscita perché la sessione specificata non è in una transazione.</span><span class="sxs-lookup"><span data-stu-id="edcef-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="edcef-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="edcef-136">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="edcef-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="edcef-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="edcef-138">Non è stato possibile eseguire il rollback delle modifiche a causa di un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="edcef-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="edcef-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="edcef-140">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="edcef-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="edcef-141">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="edcef-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="edcef-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="edcef-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="edcef-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edcef-144">In caso di esito positivo, tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata verranno annullate e il punto di salvataggio verrà terminato.</span><span class="sxs-lookup"><span data-stu-id="edcef-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="edcef-145">Se l'ultimo punto di salvataggio per la sessione è stato terminato, la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="edcef-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="edcef-146">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="edcef-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="edcef-147">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="edcef-147">No change to the database state will occur.</span></span> <span data-ttu-id="edcef-148">Un errore durante il rollback viene considerato un errore irreversibile del database.</span><span class="sxs-lookup"><span data-stu-id="edcef-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edcef-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="edcef-149">Remarks</span></span>

<span data-ttu-id="edcef-150">È necessario che una chiamata a [JetCommitTransaction](./jetcommittransaction-function.md) o **JetRollback** corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="edcef-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="edcef-151">Se, ad esempio, sono stati aperti cursori (usando [JetOpenTable](./jetopentable-function.md)) durante un punto di salvataggio di cui viene eseguito il rollback, il cursore verrà chiuso.</span><span class="sxs-lookup"><span data-stu-id="edcef-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="edcef-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edcef-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edcef-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="edcef-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="edcef-154">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="edcef-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="edcef-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="edcef-156">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="edcef-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="edcef-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="edcef-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="edcef-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcef-159"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="edcef-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="edcef-160">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="edcef-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcef-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="edcef-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="edcef-162">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="edcef-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="edcef-163">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="edcef-163">See Also</span></span>

[<span data-ttu-id="edcef-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="edcef-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="edcef-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="edcef-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="edcef-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="edcef-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="edcef-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="edcef-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="edcef-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="edcef-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
