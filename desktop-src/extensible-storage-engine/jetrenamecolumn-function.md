---
description: 'Altre informazioni su: funzione JetRenameColumn'
title: JetRenameColumn (funzione)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317342"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="4006e-103">JetRenameColumn (funzione)</span><span class="sxs-lookup"><span data-stu-id="4006e-103">JetRenameColumn Function</span></span>


<span data-ttu-id="4006e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4006e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="4006e-105">JetRenameColumn (funzione)</span><span class="sxs-lookup"><span data-stu-id="4006e-105">JetRenameColumn Function</span></span>

<span data-ttu-id="4006e-106">La funzione **JetRenameColumn** può essere utilizzata per modificare il nome di una colonna esistente in una tabella.</span><span class="sxs-lookup"><span data-stu-id="4006e-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="4006e-107">**Windows XP:**  **JetRenameColumn** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4006e-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4006e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4006e-108">Parameters</span></span>

<span data-ttu-id="4006e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4006e-109">*sesid*</span></span>

<span data-ttu-id="4006e-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="4006e-110">The session to use for this call.</span></span>

<span data-ttu-id="4006e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4006e-111">*tableid*</span></span>

<span data-ttu-id="4006e-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="4006e-112">The cursor to use for this call.</span></span>

<span data-ttu-id="4006e-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="4006e-113">*szName*</span></span>

<span data-ttu-id="4006e-114">Nome corrente della colonna che verrà rinominata.</span><span class="sxs-lookup"><span data-stu-id="4006e-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="4006e-115">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="4006e-115">*szNameNew*</span></span>

<span data-ttu-id="4006e-116">Nuovo nome per la colonna che verrà rinominata.</span><span class="sxs-lookup"><span data-stu-id="4006e-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="4006e-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4006e-117">*grbit*</span></span>

<span data-ttu-id="4006e-118">Questo parametro deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="4006e-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="4006e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4006e-119">Return Value</span></span>

<span data-ttu-id="4006e-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="4006e-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4006e-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="4006e-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4006e-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4006e-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="4006e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4006e-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4006e-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4006e-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4006e-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="4006e-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4006e-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4006e-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4006e-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="4006e-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="4006e-129">Questa colonna specificata non esiste per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="4006e-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="4006e-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="4006e-131">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="4006e-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="4006e-132">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="4006e-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="4006e-133">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="4006e-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="4006e-134">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="4006e-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="4006e-135">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="4006e-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="4006e-136">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="4006e-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="4006e-137">I nomi degli oggetti non possono iniziare con un nome di oggetto spazio. non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="4006e-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="4006e-138">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="4006e-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="4006e-139">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4006e-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="4006e-140">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="4006e-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4006e-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4006e-142">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="4006e-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4006e-143">Questo problema può verificarsi per <strong>JetRenameColumn</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="4006e-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="4006e-144"><em>szName</em> è null.</span><span class="sxs-lookup"><span data-stu-id="4006e-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="4006e-145"><em>szNameNew</em> è null.</span><span class="sxs-lookup"><span data-stu-id="4006e-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4006e-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4006e-147">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="4006e-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4006e-148">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4006e-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="4006e-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="4006e-150">Questa operazione può essere eseguita solo quando la sessione non si trova attualmente all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="4006e-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4006e-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4006e-152">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="4006e-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4006e-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4006e-154">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="4006e-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4006e-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4006e-156">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="4006e-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="4006e-157">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4006e-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4006e-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4006e-159">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="4006e-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="4006e-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4006e-161">Non è possibile eseguire un aggiornamento all'interno dell'ambito di una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4006e-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="4006e-162">Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="4006e-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="4006e-163">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4006e-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4006e-164">In seguito all'esito positivo, il nome della colonna specificata nella tabella associata al cursore viene impostato in modo permanente sul nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="4006e-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="4006e-165">Verranno aggiornati anche tutti gli indici che fanno riferimento a tale colonna.</span><span class="sxs-lookup"><span data-stu-id="4006e-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="4006e-166">In caso di errore, non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="4006e-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4006e-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="4006e-167">Remarks</span></span>

<span data-ttu-id="4006e-168">L'operazione di ridenominazione delle colonne è insolita perché, a differenza di altre operazioni dello schema, non viene eseguita come transazione.</span><span class="sxs-lookup"><span data-stu-id="4006e-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="4006e-169">Quando una colonna in una determinata tabella viene rinominata in una sessione, qualsiasi altra sessione che utilizza tale tabella visualizzerà immediatamente la modifica, anche se si trovano in una transazione che impedisce a tale sessione di visualizzare le altre modifiche apportate dalla sessione durante l'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="4006e-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="4006e-170">L'ID di colonna di una colonna non è influenzato dall'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="4006e-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4006e-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4006e-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4006e-172"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-173">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4006e-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-174"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-175">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4006e-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-176"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-177">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="4006e-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-178"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-179">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4006e-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4006e-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-181">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4006e-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4006e-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4006e-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4006e-183">Implementato come <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4006e-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4006e-184">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4006e-184">See Also</span></span>

[<span data-ttu-id="4006e-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4006e-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4006e-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4006e-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4006e-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4006e-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4006e-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4006e-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4006e-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="4006e-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
