---
description: 'Altre informazioni su: funzione JetGetLS'
title: JetGetLS (funzione)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318092"
---
# <a name="jetgetls-function"></a><span data-ttu-id="9894f-103">JetGetLS (funzione)</span><span class="sxs-lookup"><span data-stu-id="9894f-103">JetGetLS Function</span></span>


<span data-ttu-id="9894f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9894f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="9894f-105">JetGetLS (funzione)</span><span class="sxs-lookup"><span data-stu-id="9894f-105">JetGetLS Function</span></span>

<span data-ttu-id="9894f-106">La funzione **JetGetLS** consente all'applicazione di recuperare l'handle di contesto noto come archiviazione locale associato a un cursore o alla tabella associata a tale cursore.</span><span class="sxs-lookup"><span data-stu-id="9894f-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="9894f-107">Questo handle di contesto deve essere stato impostato in precedenza utilizzando [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="9894f-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="9894f-108">**JetGetLS** può essere utilizzato anche per recuperare contemporaneamente l'handle del contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9894f-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="9894f-109">**Windows XP: JetGetLS** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9894f-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9894f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9894f-110">Parameters</span></span>

<span data-ttu-id="9894f-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9894f-111">*sesid*</span></span>

<span data-ttu-id="9894f-112">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="9894f-112">The session to use for this call.</span></span>

<span data-ttu-id="9894f-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9894f-113">*tableid*</span></span>

<span data-ttu-id="9894f-114">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="9894f-114">The cursor to use for this call.</span></span>

<span data-ttu-id="9894f-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="9894f-115">*pls*</span></span>

<span data-ttu-id="9894f-116">Buffer di output che riceve l'handle di contesto attualmente associato al cursore o alla tabella.</span><span class="sxs-lookup"><span data-stu-id="9894f-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="9894f-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9894f-117">*grbit*</span></span>

<span data-ttu-id="9894f-118">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9894f-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9894f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9894f-119">Value</span></span></p></th>
<th><p><span data-ttu-id="9894f-120">Significato</span><span class="sxs-lookup"><span data-stu-id="9894f-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9894f-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="9894f-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="9894f-122">Indica che è necessario recuperare l'handle di contesto associato al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="9894f-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="9894f-123">Se non viene specificato né JET_bitLSCursor né JET_bitLSTable, JET_bitLSCursor si presume.</span><span class="sxs-lookup"><span data-stu-id="9894f-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="9894f-124">Questa opzione non può essere utilizzata con JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="9894f-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="9894f-125">L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9894f-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="9894f-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="9894f-127">Indica che è necessario recuperare l'handle di contesto associato alla tabella che contiene il cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="9894f-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="9894f-128">Non è consentito usare questa opzione con JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="9894f-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="9894f-129">L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9894f-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="9894f-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="9894f-131">Indica che l'handle del contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="9894f-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="9894f-132">Il valore corrente dell'handle di contesto viene restituito nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="9894f-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9894f-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9894f-133">Return Value</span></span>

<span data-ttu-id="9894f-134">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="9894f-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9894f-135">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="9894f-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9894f-136">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9894f-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="9894f-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9894f-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9894f-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9894f-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9894f-139">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9894f-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9894f-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9894f-141">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9894f-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9894f-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9894f-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="9894f-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9894f-144">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9894f-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9894f-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9894f-146">Una delle opzioni richieste non è valida, è stata usata in modo non valido o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="9894f-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="9894f-147">Questo problema può verificarsi per <strong>JetGetLS</strong> quando vengono impostati sia JET_bitLSCursor che JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="9894f-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="9894f-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="9894f-149">Non è stato possibile restituire l'handle del contesto perché all'oggetto richiesto non è attualmente associato alcun handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9894f-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="9894f-150"><strong>Nota  </strong> Questo errore non viene restituito se JET_bitLSReset è specificato ma non è stato associato alcun handle di contesto all'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="9894f-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9894f-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9894f-152">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="9894f-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9894f-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9894f-154">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="9894f-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9894f-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9894f-156">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="9894f-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9894f-157">In caso di esito positivo, l'handle di contesto è stato recuperato dall'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="9894f-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="9894f-158">Se JET_bitLSReset è stato specificato, anche tale handle di contesto è stato rimosso correttamente dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9894f-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="9894f-159">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="9894f-159">No change to the database state will occur.</span></span>

<span data-ttu-id="9894f-160">In caso di errore, non sono state apportate modifiche allo stato dell'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="9894f-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="9894f-161">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="9894f-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9894f-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9894f-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9894f-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9894f-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9894f-164">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9894f-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9894f-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9894f-166">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9894f-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-167"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9894f-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9894f-168">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9894f-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9894f-169"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="9894f-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9894f-170">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9894f-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9894f-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9894f-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9894f-172">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9894f-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9894f-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9894f-173">See Also</span></span>

[<span data-ttu-id="9894f-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9894f-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9894f-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9894f-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9894f-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="9894f-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="9894f-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9894f-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9894f-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9894f-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9894f-179">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="9894f-179">JetSetLS</span></span>](./jetsetls-function.md)
