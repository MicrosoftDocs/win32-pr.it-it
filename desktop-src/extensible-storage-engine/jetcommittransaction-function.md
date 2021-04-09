---
description: 'Altre informazioni su: funzione JetCommitTransaction'
title: Funzione JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968433"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="131b2-103">Funzione JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="131b2-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="131b2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="131b2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="131b2-105">Funzione JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="131b2-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="131b2-106">La funzione **JetCommitTransaction** esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente.</span><span class="sxs-lookup"><span data-stu-id="131b2-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="131b2-107">Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="131b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="131b2-108">Parameters</span></span>

<span data-ttu-id="131b2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="131b2-109">*sesid*</span></span>

<span data-ttu-id="131b2-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="131b2-110">The session to use for this call.</span></span>

<span data-ttu-id="131b2-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="131b2-111">*grbit*</span></span>

<span data-ttu-id="131b2-112">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="131b2-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="131b2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="131b2-113">Value</span></span></p></th>
<th><p><span data-ttu-id="131b2-114">Significato</span><span class="sxs-lookup"><span data-stu-id="131b2-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="131b2-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="131b2-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="131b2-116">Viene eseguito il commit della transazione in modo normale, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="131b2-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="131b2-117">Questo riduce drasticamente la durata di un'operazione di commit al costo della durabilità.</span><span class="sxs-lookup"><span data-stu-id="131b2-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="131b2-118">Qualsiasi transazione non scaricata nel log prima di un arresto anomalo verrà automaticamente interrotta durante il ripristino dell'arresto anomalo durante la chiamata successiva a <a href="gg294068(v=exchg.10).md">JetInit</a>.</span><span class="sxs-lookup"><span data-stu-id="131b2-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="131b2-119">Se si specifica JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="131b2-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="131b2-120">Se la chiamata a <strong>JetCommitTransaction</strong> non corrisponde alla prima chiamata a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> per questa sessione, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="131b2-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="131b2-121">Ciò è dovuto al fatto che l'azione finale che si verifica nel punto di salvataggio più esterno è il fattore determinante se l'intera transazione è effettivamente vincolata al disco.</span><span class="sxs-lookup"><span data-stu-id="131b2-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="131b2-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="131b2-123">Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="131b2-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="131b2-124">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="131b2-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="131b2-125">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="131b2-126">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="131b2-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="131b2-127">Questa opzione è disponibile solo a partire da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="131b2-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="131b2-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="131b2-129">Se la sessione ha precedentemente eseguito il commit di tutte le transazioni che non sono ancora state scaricate nel file di log delle transazioni, è necessario scaricarle immediatamente.</span><span class="sxs-lookup"><span data-stu-id="131b2-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="131b2-130">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="131b2-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="131b2-131">Questa operazione è utile se l'applicazione ha precedentemente eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</span><span class="sxs-lookup"><span data-stu-id="131b2-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="131b2-132">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="131b2-133">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="131b2-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="131b2-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="131b2-134">Return Value</span></span>

<span data-ttu-id="131b2-135">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="131b2-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="131b2-136">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="131b2-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="131b2-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="131b2-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="131b2-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="131b2-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="131b2-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="131b2-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="131b2-140">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="131b2-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="131b2-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="131b2-142">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="131b2-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="131b2-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="131b2-144">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="131b2-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="131b2-145">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="131b2-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="131b2-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="131b2-147">Una delle opzioni richieste non è valida o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="131b2-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="131b2-148">Questo errore viene restituito da <strong>JetCommitTransaction</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="131b2-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="131b2-149">È stato specificato un <em>grbit</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="131b2-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="131b2-150">JET_bitWaitLastLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="131b2-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="131b2-151">JET_bitWaitAllLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="131b2-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="131b2-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="131b2-153">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="131b2-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="131b2-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="131b2-155">Operazione non riuscita perché la sessione specificata non è in una transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="131b2-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="131b2-157">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="131b2-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="131b2-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="131b2-159">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="131b2-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="131b2-160">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="131b2-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="131b2-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="131b2-162">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="131b2-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="131b2-163">In caso di esito positivo, verrà eseguito il commit di tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata e il punto di salvataggio verrà terminato.</span><span class="sxs-lookup"><span data-stu-id="131b2-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="131b2-164">Se l'ultimo punto di salvataggio per la sessione è stato terminato, la transazione verrà scaricata facoltativamente nel file di log delle transazioni e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="131b2-165">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="131b2-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="131b2-166">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="131b2-166">No change to the database state will occur.</span></span> <span data-ttu-id="131b2-167">L'applicazione deve chiamare [JetRollback](./jetrollback-function.md) per interrompere la transazione.</span><span class="sxs-lookup"><span data-stu-id="131b2-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="131b2-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="131b2-168">Remarks</span></span>

<span data-ttu-id="131b2-169">È necessario che una chiamata a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="131b2-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="131b2-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="131b2-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="131b2-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="131b2-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="131b2-172">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="131b2-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="131b2-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="131b2-174">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="131b2-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-175"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="131b2-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="131b2-176">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="131b2-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="131b2-177"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="131b2-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="131b2-178">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="131b2-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="131b2-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="131b2-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="131b2-180">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="131b2-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="131b2-181">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="131b2-181">See Also</span></span>

[<span data-ttu-id="131b2-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="131b2-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="131b2-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="131b2-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="131b2-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="131b2-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="131b2-185">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="131b2-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="131b2-186">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="131b2-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="131b2-187">JetRollback</span><span class="sxs-lookup"><span data-stu-id="131b2-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="131b2-188">JetStopService</span><span class="sxs-lookup"><span data-stu-id="131b2-188">JetStopService</span></span>](./jetstopservice-function.md)
