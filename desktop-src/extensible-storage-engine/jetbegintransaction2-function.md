---
description: 'Altre informazioni su: funzione JetBeginTransaction2'
title: Funzione JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316456"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="5a33a-103">Funzione JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="5a33a-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="5a33a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a33a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="5a33a-105">Funzione JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="5a33a-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="5a33a-106">La funzione **JetBeginTransaction2** fa sì che una sessione entri in una transazione e crei un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="5a33a-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="5a33a-107">Questa funzione può essere chiamata più volte in una singola sessione per creare punti di salvataggio aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5a33a-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="5a33a-108">Questi punti di salvataggio possono essere utilizzati in modo selettivo per conservare o annullare le modifiche apportate al database.</span><span class="sxs-lookup"><span data-stu-id="5a33a-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5a33a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a33a-109">Parameters</span></span>

<span data-ttu-id="5a33a-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5a33a-110">*sesid*</span></span>

<span data-ttu-id="5a33a-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5a33a-111">The session to use for this call.</span></span>

<span data-ttu-id="5a33a-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5a33a-112">*grbit*</span></span>

<span data-ttu-id="5a33a-113">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a33a-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a33a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5a33a-114">Value</span></span></p></th>
<th><p><span data-ttu-id="5a33a-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5a33a-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="5a33a-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5a33a-117">Il database non viene modificato dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="5a33a-117">The transaction will not modify the database.</span></span> <span data-ttu-id="5a33a-118">Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con JET_errTransReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5a33a-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="5a33a-119">Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già presente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="5a33a-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="5a33a-120">Questa opzione è disponibile solo a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a33a-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5a33a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a33a-121">Return Value</span></span>

<span data-ttu-id="5a33a-122">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5a33a-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5a33a-123">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5a33a-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a33a-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a33a-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="5a33a-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a33a-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5a33a-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5a33a-127">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5a33a-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5a33a-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5a33a-129">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5a33a-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5a33a-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5a33a-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="5a33a-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5a33a-132">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a33a-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5a33a-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5a33a-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5a33a-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5a33a-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a33a-136">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5a33a-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5a33a-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5a33a-138">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="5a33a-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="5a33a-139">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a33a-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5a33a-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a33a-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="5a33a-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="5a33a-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="5a33a-143">Impossibile avviare una nuova transazione perché la sessione si trova già nella profondità massima del punto di salvataggio consentita dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="5a33a-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a33a-144">In seguito all'esito positivo, la sessione specificata si troverà all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="5a33a-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="5a33a-145">Se la sessione si trovava in precedenza all'interno di una transazione, viene creato un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="5a33a-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="5a33a-146">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="5a33a-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="5a33a-147">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="5a33a-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5a33a-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a33a-148">Remarks</span></span>

<span data-ttu-id="5a33a-149">Per ulteriori informazioni sul funzionamento delle transazioni, vedere [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="5a33a-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5a33a-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a33a-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5a33a-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a33a-152">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5a33a-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5a33a-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a33a-154">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a33a-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-155"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5a33a-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a33a-156">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5a33a-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a33a-157"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5a33a-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5a33a-158">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5a33a-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a33a-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5a33a-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5a33a-160">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5a33a-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5a33a-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5a33a-161">See Also</span></span>

[<span data-ttu-id="5a33a-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a33a-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a33a-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a33a-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a33a-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5a33a-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5a33a-165">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="5a33a-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="5a33a-166">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="5a33a-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="5a33a-167">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="5a33a-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="5a33a-168">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="5a33a-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="5a33a-169">JetRollback</span><span class="sxs-lookup"><span data-stu-id="5a33a-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="5a33a-170">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="5a33a-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="5a33a-171">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="5a33a-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
