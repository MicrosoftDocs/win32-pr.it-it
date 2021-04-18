---
description: 'Altre informazioni su: funzione JetBeginTransaction3'
title: Funzione JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305740"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="9c229-103">Funzione JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="9c229-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="9c229-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c229-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="9c229-105">La funzione **JetBeginTransaction3** fa sì che una sessione entri in una transazione e crei un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="9c229-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="9c229-106">Questa funzione può essere chiamata più volte in una singola sessione per creare punti di salvataggio aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9c229-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="9c229-107">Questi punti di salvataggio possono essere utilizzati in modo selettivo per conservare o annullare le modifiche apportate al database.</span><span class="sxs-lookup"><span data-stu-id="9c229-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="9c229-108">La funzione **JetBeginTransaction3** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9c229-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="9c229-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c229-109">Parameters</span></span>

<span data-ttu-id="9c229-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9c229-110">*sesid*</span></span>

<span data-ttu-id="9c229-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="9c229-111">The session to use for this call.</span></span>

<span data-ttu-id="9c229-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="9c229-112">*trxid*</span></span>

<span data-ttu-id="9c229-113">Identificatore facoltativo fornito dall'utente per identificare la transazione.</span><span class="sxs-lookup"><span data-stu-id="9c229-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="9c229-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9c229-114">*grbit*</span></span>

<span data-ttu-id="9c229-115">Gruppo di bit che specifica zero o più valori dell'opzione di chiamata elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9c229-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c229-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9c229-116">Value</span></span></p></th>
<th><p><span data-ttu-id="9c229-117">Significato</span><span class="sxs-lookup"><span data-stu-id="9c229-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c229-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="9c229-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9c229-119">Il database non viene modificato dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="9c229-119">The transaction will not modify the database.</span></span> <span data-ttu-id="9c229-120">Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con JET_errTransReadOnly codice di risposta.</span><span class="sxs-lookup"><span data-stu-id="9c229-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="9c229-121">Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già presente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="9c229-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="9c229-122">Questa opzione è disponibile nelle versioni del sistema operativo Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c229-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9c229-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c229-123">Return value</span></span>

<span data-ttu-id="9c229-124">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9c229-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="9c229-125">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="9c229-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c229-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9c229-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="9c229-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c229-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c229-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9c229-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9c229-129">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9c229-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9c229-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9c229-131">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="9c229-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c229-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9c229-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9c229-133">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="9c229-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9c229-134">Questo codice restituito viene restituito dalle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c229-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9c229-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9c229-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="9c229-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c229-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9c229-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c229-138">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="9c229-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9c229-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9c229-140">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="9c229-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9c229-141">Questo errore viene restituito dalle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c229-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c229-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9c229-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c229-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="9c229-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="9c229-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="9c229-145">Impossibile avviare una nuova transazione perché la sessione si trova già nella profondità massima del punto di salvataggio consentita dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="9c229-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c229-146">In seguito all'esito positivo, la sessione specificata si troverà all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="9c229-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="9c229-147">Se la sessione si trovava in precedenza all'interno di una transazione, verrà creato un nuovo punto di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="9c229-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="9c229-148">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="9c229-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="9c229-149">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="9c229-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9c229-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c229-150">Remarks</span></span>

<span data-ttu-id="9c229-151">Per ulteriori informazioni sul funzionamento delle transazioni, vedere [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="9c229-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9c229-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c229-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c229-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9c229-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c229-154">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9c229-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c229-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c229-156">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9c229-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c229-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9c229-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c229-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9c229-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c229-159"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="9c229-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9c229-160">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9c229-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c229-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9c229-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c229-162">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9c229-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9c229-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c229-163">See also</span></span>

[<span data-ttu-id="9c229-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9c229-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9c229-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9c229-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9c229-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9c229-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9c229-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="9c229-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="9c229-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9c229-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="9c229-169">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9c229-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="9c229-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="9c229-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="9c229-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9c229-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9c229-172">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="9c229-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="9c229-173">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="9c229-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
