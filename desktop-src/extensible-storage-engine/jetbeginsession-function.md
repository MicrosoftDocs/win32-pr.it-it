---
description: 'Altre informazioni su: funzione JetBeginSession'
title: Funzione JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318095"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="253c6-103">Funzione JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="253c6-103">JetBeginSession Function</span></span>


<span data-ttu-id="253c6-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="253c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="253c6-105">Funzione JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="253c6-105">JetBeginSession Function</span></span>

<span data-ttu-id="253c6-106">La funzione **JetBeginSession** avvia una sessione e Inizializza e restituisce un handle di sessione ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="253c6-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="253c6-107">Le sessioni controllano l'accesso al database e vengono utilizzate per controllare l'ambito delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="253c6-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="253c6-108">La sessione può essere utilizzata per avviare, eseguire il commit o interrompere le transazioni.</span><span class="sxs-lookup"><span data-stu-id="253c6-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="253c6-109">La sessione viene inoltre utilizzata per il fissaggio, la creazione o l'apertura di un database.</span><span class="sxs-lookup"><span data-stu-id="253c6-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="253c6-110">La sessione viene utilizzata come contesto per tutte le operazioni DDL e DML.</span><span class="sxs-lookup"><span data-stu-id="253c6-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="253c6-111">Per aumentare la concorrenza e l'accesso parallelo al database, è possibile iniziare più sessioni.</span><span class="sxs-lookup"><span data-stu-id="253c6-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="253c6-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="253c6-112">Parameters</span></span>

<span data-ttu-id="253c6-113">*istanza*</span><span class="sxs-lookup"><span data-stu-id="253c6-113">*instance*</span></span>

<span data-ttu-id="253c6-114">Istanza di database da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="253c6-114">The database instance to use for this call.</span></span>

<span data-ttu-id="253c6-115">*psesid*</span><span class="sxs-lookup"><span data-stu-id="253c6-115">*psesid*</span></span>

<span data-ttu-id="253c6-116">Puntatore alla variabile che l'handle di sessione Inizializza in una corretta restituzione.</span><span class="sxs-lookup"><span data-stu-id="253c6-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="253c6-117">*szUserName*</span><span class="sxs-lookup"><span data-stu-id="253c6-117">*szUserName*</span></span>

<span data-ttu-id="253c6-118">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="253c6-118">This parameter is reserved.</span></span>

<span data-ttu-id="253c6-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="253c6-119">*szPassword*</span></span>

<span data-ttu-id="253c6-120">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="253c6-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="253c6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="253c6-121">Return Value</span></span>

<span data-ttu-id="253c6-122">Questa funzione consente la restituzione di tutti i [JET_ERR](./jet-err.md)definiti in questa API.</span><span class="sxs-lookup"><span data-stu-id="253c6-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="253c6-123">Per altre informazioni sugli errori di Jet, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.</span><span class="sxs-lookup"><span data-stu-id="253c6-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="253c6-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="253c6-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="253c6-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="253c6-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="253c6-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="253c6-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="253c6-127">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="253c6-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="253c6-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="253c6-129">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="253c6-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="253c6-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="253c6-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="253c6-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="253c6-132">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="253c6-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="253c6-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="253c6-134">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="253c6-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="253c6-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="253c6-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="253c6-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="253c6-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="253c6-138">L'operazione non è riuscita perché non è stato possibile allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="253c6-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="253c6-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="253c6-140">Il numero di sessioni consentite dal motore per l'avvio del client è limitato.</span><span class="sxs-lookup"><span data-stu-id="253c6-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="253c6-141">Questo valore può essere modificato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la costante JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="253c6-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="253c6-142">Il numero predefinito di sessioni è 16.</span><span class="sxs-lookup"><span data-stu-id="253c6-142">The default number of sessions is 16.</span></span> <span data-ttu-id="253c6-143">Per informazioni dettagliate sui JET_paramMaxSessions, vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a> .</span><span class="sxs-lookup"><span data-stu-id="253c6-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="253c6-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="253c6-145">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="253c6-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="253c6-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="253c6-147">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="253c6-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="253c6-148">In seguito all'esito positivo, l'handle di sessione viene inizializzato e può essere utilizzato per le operazioni di database.</span><span class="sxs-lookup"><span data-stu-id="253c6-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="253c6-149">In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="253c6-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="253c6-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="253c6-150">Remarks</span></span>

<span data-ttu-id="253c6-151">Quando si utilizzano sessioni tra thread diversi, è necessario prestare particolare attenzione.</span><span class="sxs-lookup"><span data-stu-id="253c6-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="253c6-152">Una sessione rileva il thread in cui è stato usato durante [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)o [JetRollback](./jetrollback-function.md)e genera un errore se usato su più thread con una transazione aperta.</span><span class="sxs-lookup"><span data-stu-id="253c6-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="253c6-153">Il [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) può modificare questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="253c6-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="253c6-154">Poiché la sessione è ancora un contesto serializzato e non è possibile eseguire più operazioni di database in una singola sessione simultaneamente, solo in serie.</span><span class="sxs-lookup"><span data-stu-id="253c6-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="253c6-155">Tuttavia, è possibile utilizzare più sessioni per ottenere l'accesso al database simultaneo.</span><span class="sxs-lookup"><span data-stu-id="253c6-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="253c6-156">Le sessioni possono essere utilizzate all'interno di una transazione tra thread impostando e reimpostando i contesti di sessione.</span><span class="sxs-lookup"><span data-stu-id="253c6-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="253c6-157">È necessario chiudere l'handle della sessione con [JetEndSession](./jetendsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="253c6-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="253c6-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="253c6-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="253c6-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-160">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="253c6-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-162">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="253c6-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-163"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-164">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="253c6-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-165"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-166">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="253c6-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="253c6-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-168">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="253c6-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="253c6-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="253c6-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="253c6-170">Implementato come <strong>JetBeginSessionW</strong> (Unicode) e <strong>JetBeginSessionA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="253c6-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="253c6-171">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="253c6-171">See Also</span></span>

[<span data-ttu-id="253c6-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="253c6-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="253c6-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="253c6-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="253c6-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="253c6-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="253c6-175">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="253c6-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="253c6-176">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="253c6-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="253c6-177">JetDupSession</span><span class="sxs-lookup"><span data-stu-id="253c6-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="253c6-178">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="253c6-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="253c6-179">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="253c6-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="253c6-180">JetRollback</span><span class="sxs-lookup"><span data-stu-id="253c6-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="253c6-181">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="253c6-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="253c6-182">JetStopService</span><span class="sxs-lookup"><span data-stu-id="253c6-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="253c6-183">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="253c6-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
