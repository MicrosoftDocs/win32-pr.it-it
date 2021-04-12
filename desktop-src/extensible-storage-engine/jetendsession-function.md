---
description: 'Altre informazioni su: funzione JetEndSession'
title: JetEndSession (funzione)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346666"
---
# <a name="jetendsession-function"></a><span data-ttu-id="9fbaa-103">JetEndSession (funzione)</span><span class="sxs-lookup"><span data-stu-id="9fbaa-103">JetEndSession Function</span></span>


<span data-ttu-id="9fbaa-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9fbaa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="9fbaa-105">JetEndSession (funzione)</span><span class="sxs-lookup"><span data-stu-id="9fbaa-105">JetEndSession Function</span></span>

<span data-ttu-id="9fbaa-106">La funzione **JetEndSession** termina la sessione e pulisce e dealloca le risorse associate alla sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9fbaa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fbaa-107">Parameters</span></span>

<span data-ttu-id="9fbaa-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9fbaa-108">*sesid*</span></span>

<span data-ttu-id="9fbaa-109">Sessione da terminare.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-109">The session to end.</span></span> <span data-ttu-id="9fbaa-110">Le risorse associate vengono rilasciate al termine della sessione.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="9fbaa-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9fbaa-111">*grbit*</span></span>

<span data-ttu-id="9fbaa-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-112">Reserved.</span></span> <span data-ttu-id="9fbaa-113">Questo parametro può contenere il flag di JET_bitForceSessionClosed, ma questo flag è riservato e l'impostazione non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="9fbaa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fbaa-114">Return Value</span></span>

<span data-ttu-id="9fbaa-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9fbaa-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="9fbaa-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9fbaa-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9fbaa-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="9fbaa-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fbaa-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9fbaa-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9fbaa-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-122">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9fbaa-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-124">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="9fbaa-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-126">La sessione non è una sessione JET valida.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9fbaa-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9fbaa-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-130">L'operazione non è riuscita perché non è stato possibile allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="9fbaa-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-132">Ciò significa che la sessione è stata usata in un altro thread o che la sessione non è stata impostata o reimpostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9fbaa-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9fbaa-135">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="9fbaa-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-137">Errore di sistema che indica che non sono presenti altri buffer.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9fbaa-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-139">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9fbaa-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9fbaa-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9fbaa-142">In seguito all'esito positivo, l'handle di sessione viene chiuso e non è disponibile e tutte le risorse correlate a questa sessione vengono pulite.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="9fbaa-143">In caso di errore, è possibile che si verifichino alcuni errori aggiuntivi come parte della chiusura della tabella di ordinamento, della chiusura del cursore e del rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="9fbaa-144">Questi errori sono piuttosto improbabili ed estremamente improbabili se le sessioni non vengono usate completamente quando viene chiamato **JetEndSession** .</span><span class="sxs-lookup"><span data-stu-id="9fbaa-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="9fbaa-145">Questi errori verranno restituiti se non è stato possibile pulire correttamente una parte della sessione.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9fbaa-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fbaa-146">Remarks</span></span>

<span data-ttu-id="9fbaa-147">Questa API esegue il rollback di tutte le transazioni aperte (non sottoposte a commit nel livello 0).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="9fbaa-148">Verranno puliti anche tutti i cursori associati alla sessione e le tabelle di ordinamento create o aperte.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9fbaa-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fbaa-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbaa-151">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbaa-153">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-154"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbaa-155">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbaa-156"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbaa-157">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbaa-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbaa-159">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9fbaa-160">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9fbaa-160">See Also</span></span>

[<span data-ttu-id="9fbaa-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9fbaa-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9fbaa-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9fbaa-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9fbaa-163">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="9fbaa-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="9fbaa-164">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9fbaa-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9fbaa-165">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9fbaa-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9fbaa-166">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9fbaa-166">JetStopService</span></span>](./jetstopservice-function.md)
