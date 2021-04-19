---
description: 'Altre informazioni su: funzione JetCommitTransaction2'
title: JetCommitTransaction2 (funzione)
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318094"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="1c092-103">JetCommitTransaction2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c092-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="1c092-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1c092-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="1c092-105">La funzione **JetCommitTransaction2** esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1c092-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="1c092-106">Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="1c092-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="1c092-107">La funzione **JetCommitTransaction2** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c092-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="1c092-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c092-108">Parameters</span></span>

<span data-ttu-id="1c092-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1c092-109">*sesid*</span></span>

<span data-ttu-id="1c092-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1c092-110">The session to use for this call.</span></span>

<span data-ttu-id="1c092-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1c092-111">*grbit*</span></span>

<span data-ttu-id="1c092-112">Gruppo di bit che specifica zero o più valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1c092-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c092-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1c092-113">Value</span></span></p></th>
<th><p><span data-ttu-id="1c092-114">Significato</span><span class="sxs-lookup"><span data-stu-id="1c092-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c092-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="1c092-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="1c092-116">Viene eseguito il commit della transazione in modo normale, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1c092-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="1c092-117">Questo riduce drasticamente la durata di un'operazione di commit al costo della durabilità.</span><span class="sxs-lookup"><span data-stu-id="1c092-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="1c092-118">Qualsiasi transazione non scaricata nel log prima di un arresto anomalo verrà automaticamente interrotta durante il ripristino dell'arresto anomalo del sistema durante la chiamata successiva alla funzione <a href="gg294068(v=exchg.10).md">JetInit</a> .</span><span class="sxs-lookup"><span data-stu-id="1c092-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="1c092-119">Se si specifica JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="1c092-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="1c092-120">Se la chiamata a <strong>JetCommitTransaction2</strong> non corrisponde alla prima chiamata alla funzione <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> per questa sessione, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="1c092-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="1c092-121">Ciò è dovuto al fatto che l'azione finale che si verifica nel punto di salvataggio più esterno è il fattore determinante se l'intera transazione è effettivamente vincolata al disco.</span><span class="sxs-lookup"><span data-stu-id="1c092-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="1c092-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="1c092-123">Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="1c092-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="1c092-124">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1c092-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="1c092-125">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="1c092-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="1c092-126">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="1c092-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="1c092-127">Questa opzione è disponibile nelle versioni del sistema operativo Windows Server a partire da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1c092-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="1c092-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="1c092-129">Se la sessione ha precedentemente eseguito il commit di tutte le transazioni che non sono ancora state scaricate nel file di log delle transazioni, è necessario scaricarle immediatamente.</span><span class="sxs-lookup"><span data-stu-id="1c092-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="1c092-130">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1c092-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="1c092-131">Questa operazione è utile se l'applicazione ha precedentemente eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</span><span class="sxs-lookup"><span data-stu-id="1c092-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="1c092-132">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="1c092-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="1c092-133">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="1c092-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c092-134">*cmsecDurableCommit*</span><span class="sxs-lookup"><span data-stu-id="1c092-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="1c092-135">Durata del commit di una transazione Lazy.</span><span class="sxs-lookup"><span data-stu-id="1c092-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="1c092-136">*pCommitID*</span><span class="sxs-lookup"><span data-stu-id="1c092-136">*pCommitID*</span></span>

<span data-ttu-id="1c092-137">ID di commit associato al record di commit.</span><span class="sxs-lookup"><span data-stu-id="1c092-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="1c092-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c092-138">Return value</span></span>

<span data-ttu-id="1c092-139">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1c092-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="1c092-140">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1c092-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c092-141">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1c092-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="1c092-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c092-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c092-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1c092-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1c092-144">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1c092-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1c092-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1c092-146">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="1c092-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1c092-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1c092-148">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="1c092-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1c092-149">Questo errore viene restituito solo dalle versioni del sistema operativo Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c092-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="1c092-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="1c092-151">Una delle opzioni richieste non è valida o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="1c092-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="1c092-152">Questo errore verrà restituito dalla funzione <strong>JetCommitTransaction2</strong> quando si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1c092-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c092-153">È stato specificato un <em>grbit</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="1c092-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="1c092-154">JET_bitWaitLastLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="1c092-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="1c092-155">JET_bitWaitAllLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="1c092-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1c092-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1c092-157">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="1c092-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="1c092-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1c092-159">Operazione non riuscita perché la sessione specificata non è in una transazione.</span><span class="sxs-lookup"><span data-stu-id="1c092-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1c092-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1c092-161">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1c092-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1c092-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1c092-163">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="1c092-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1c092-164">Questo errore viene restituito solo dalle versioni del sistema operativo Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c092-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1c092-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1c092-166">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="1c092-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c092-167">In caso di esito positivo, verrà eseguito il commit di tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata e il punto di salvataggio verrà terminato.</span><span class="sxs-lookup"><span data-stu-id="1c092-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="1c092-168">Se l'ultimo punto di salvataggio per la sessione è stato terminato, la transazione verrà scaricata facoltativamente nel file di log delle transazioni e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="1c092-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="1c092-169">In caso di errore, lo stato transazionale della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="1c092-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="1c092-170">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="1c092-170">No change to the database state will occur.</span></span> <span data-ttu-id="1c092-171">Per interrompere la transazione, l'applicazione deve chiamare la funzione [JetRollback](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1c092-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1c092-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c092-172">Remarks</span></span>

<span data-ttu-id="1c092-173">È necessario che una chiamata a **JetCommitTransaction2** o [JetRollback](./jetrollback-function.md) corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="1c092-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1c092-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c092-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c092-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1c092-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1c092-176">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c092-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1c092-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1c092-178">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1c092-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-179"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1c092-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1c092-180">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1c092-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c092-181"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1c092-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1c092-182">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1c092-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c092-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1c092-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1c092-184">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1c092-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1c092-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c092-185">See also</span></span>

[<span data-ttu-id="1c092-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1c092-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1c092-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1c092-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1c092-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1c092-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1c092-189">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="1c092-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="1c092-190">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="1c092-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="1c092-191">JetRollback</span><span class="sxs-lookup"><span data-stu-id="1c092-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="1c092-192">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1c092-192">JetStopService</span></span>](./jetstopservice-function.md)
