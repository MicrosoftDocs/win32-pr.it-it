---
description: 'Altre informazioni su: funzione JetBeginTransaction'
title: Funzione JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342666"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="c9bf4-103">Funzione JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="c9bf4-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="c9bf4-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c9bf4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="c9bf4-105">Funzione JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="c9bf4-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="c9bf4-106">La funzione **JetBeginTransaction** fa sì che una sessione entri in una transazione e crei un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="c9bf4-107">Questa funzione può essere chiamata più volte in una singola sessione per provocare la creazione di punti di salvataggio aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="c9bf4-108">Questi punti di salvataggio possono essere utilizzati per conservare o annullare selettivamente le modifiche apportate allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="c9bf4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9bf4-109">Parameters</span></span>

<span data-ttu-id="c9bf4-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c9bf4-110">*sesid*</span></span>

<span data-ttu-id="c9bf4-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="c9bf4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9bf4-112">Return Value</span></span>

<span data-ttu-id="c9bf4-113">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c9bf4-114">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c9bf4-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9bf4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c9bf4-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="c9bf4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9bf4-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c9bf4-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c9bf4-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-120">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c9bf4-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-122">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c9bf4-123">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c9bf4-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-125">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c9bf4-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-127">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c9bf4-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-129">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c9bf4-130">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c9bf4-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-132">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="c9bf4-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="c9bf4-134">Impossibile avviare una nuova transazione perché la sessione si trova già nella profondità massima del punto di salvataggio consentita dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9bf4-135">In seguito all'esito positivo, la sessione specificata si troverà all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="c9bf4-136">Se la sessione si trovava in precedenza all'interno di una transazione, viene creato un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="c9bf4-137">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="c9bf4-138">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c9bf4-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9bf4-139">Remarks</span></span>

<span data-ttu-id="c9bf4-140">Il motore di database fornisce un modello di isolamento dello snapshot per le transazioni.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="c9bf4-141">Ciò significa che, quando una sessione entra per la prima volta in uno stato transazionale, la sessione visualizzerà l'intero database bloccato nel tempo all'inizio della transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="c9bf4-142">Una sessione non deve leggere il blocco dei dati perché può sempre accedere alla versione appropriata di tali dati.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="c9bf4-143">Ciò significa che una sessione che aggiorna i dati non bloccherà mai una sessione diversa dalla lettura dei dati.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="c9bf4-144">Un'altra implicazione dell'utilizzo dell'isolamento dello snapshot è il modello di blocco utilizzato per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="c9bf4-145">Il motore di database assegnerà un blocco di scrittura su una determinata parte di dati alla prima sessione che la richiede.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="c9bf4-146">Questo blocco di scrittura viene rilasciato quando viene eseguito il commit o l'interruzione completa della transazione in modo che la sessione non si trovi più in una transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="c9bf4-147">Mentre una sessione include un blocco di scrittura, qualsiasi altra sessione che richiede lo stesso blocco di scrittura non verrà bloccata fino a quando non sarà disponibile il blocco di scrittura.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="c9bf4-148">La seconda sessione avrà invece immediatamente esito negativo con JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="c9bf4-149">Per risolvere questo conflitto, è necessario che la seconda sessione interrompa (o Esegui il commit) la transazione, attenda un periodo di tempo limitato per la prima sessione per eseguire il commit o interrompere la transazione e quindi riavviarla.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="c9bf4-150">A supporto dell'isolamento dello snapshot, il motore di database archivia tutte le versioni di tutti i dati modificati in memoria dal momento in cui è stata avviata per la prima volta la transazione attiva meno recente in una sessione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="c9bf4-151">Questa operazione ha implicazioni importanti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-151">This has important implications for your application.</span></span> <span data-ttu-id="c9bf4-152">Qualsiasi comportamento che causa la compilazione di un numero elevato di versioni in memoria può causare l'esaurimento delle dimensioni massime dell'archivio versione (vedere [JET_paramMaxVerPages](./resource-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md) per ulteriori informazioni).</span><span class="sxs-lookup"><span data-stu-id="c9bf4-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="c9bf4-153">Questo comportamento include, tuttavia, non è limitato a aggiornamenti di dimensioni molto elevate in una singola transazione e transazioni con esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="c9bf4-154">Di conseguenza, è molto importante configurare correttamente le dimensioni dell'archivio versioni per il carico transazionale previsto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="c9bf4-155">È anche importante prestare molta attenzione a limitare il numero di aggiornamenti eseguiti in una singola transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="c9bf4-156">Inoltre, è importante fare in modo che le transazioni vengano eseguite nel minor tempo possibile in scenari con carico elevato.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="c9bf4-157">È consigliabile che l'applicazione sia sempre nel contesto di una transazione quando si chiamano le API ESE che recuperano o aggiornano i dati.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="c9bf4-158">Se questa operazione non viene eseguita, il motore di database eseguirà automaticamente il wrapping di ogni chiamata API ESE di questo tipo in una transazione per conto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="c9bf4-159">Il costo di queste transazioni molto brevi può essere aggiunto rapidamente in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="c9bf4-160">Il comportamento predefinito del motore consiste nel limitare l'uso di una sessione allo stesso thread dal momento in cui la prima chiamata a **JetBeginTransaction** viene effettuata fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c9bf4-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="c9bf4-161">Questo comportamento può essere modificato per rimuovere questa restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="c9bf4-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="c9bf4-162">Il motore di database supporta inoltre le modifiche dello schema transazionale.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="c9bf4-163">È ad esempio possibile avviare una nuova transazione, creare una tabella, aggiungere alcune colonne, creare un indice o due, quindi interrompere la transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="c9bf4-164">Gli elementi dello schema appena aggiunti verranno rimossi dal database.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="c9bf4-165">È inoltre possibile combinare le modifiche dello schema e gli aggiornamenti ordinari del database nella stessa transazione.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c9bf4-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9bf4-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c9bf4-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c9bf4-168">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c9bf4-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c9bf4-170">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-171"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c9bf4-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c9bf4-172">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9bf4-173"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c9bf4-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c9bf4-174">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9bf4-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c9bf4-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c9bf4-176">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c9bf4-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c9bf4-177">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c9bf4-177">See Also</span></span>

[<span data-ttu-id="c9bf4-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c9bf4-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c9bf4-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c9bf4-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c9bf4-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c9bf4-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c9bf4-181">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="c9bf4-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="c9bf4-182">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c9bf4-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="c9bf4-183">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="c9bf4-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="c9bf4-184">JetRollback</span><span class="sxs-lookup"><span data-stu-id="c9bf4-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="c9bf4-185">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="c9bf4-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="c9bf4-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c9bf4-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c9bf4-187">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="c9bf4-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
