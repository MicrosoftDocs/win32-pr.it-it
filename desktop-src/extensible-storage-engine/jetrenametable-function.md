---
description: 'Altre informazioni su: funzione JetRenameTable'
title: JetRenameTable (funzione)
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348766"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="09a17-103">JetRenameTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="09a17-103">JetRenameTable Function</span></span>


<span data-ttu-id="09a17-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09a17-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="09a17-105">JetRenameTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="09a17-105">JetRenameTable Function</span></span>

<span data-ttu-id="09a17-106">La funzione **JetRenameTable** può essere utilizzata per modificare il nome di una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="09a17-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="09a17-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="09a17-107">Parameters</span></span>

<span data-ttu-id="09a17-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="09a17-108">*sesid*</span></span>

<span data-ttu-id="09a17-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="09a17-109">The session to use for this call.</span></span>

<span data-ttu-id="09a17-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="09a17-110">*dbid*</span></span>

<span data-ttu-id="09a17-111">Database da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="09a17-111">The database to use for this call.</span></span>

<span data-ttu-id="09a17-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="09a17-112">*szName*</span></span>

<span data-ttu-id="09a17-113">Nome corrente della tabella che verrà rinominata.</span><span class="sxs-lookup"><span data-stu-id="09a17-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="09a17-114">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="09a17-114">*szNameNew*</span></span>

<span data-ttu-id="09a17-115">Nuovo nome della tabella che verrà rinominata.</span><span class="sxs-lookup"><span data-stu-id="09a17-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="09a17-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09a17-116">Return Value</span></span>

<span data-ttu-id="09a17-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="09a17-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="09a17-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="09a17-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09a17-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="09a17-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="09a17-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09a17-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a17-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="09a17-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="09a17-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="09a17-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="09a17-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="09a17-124">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="09a17-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="09a17-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="09a17-126">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="09a17-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="09a17-127">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09a17-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="09a17-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="09a17-129">Il database specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="09a17-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="09a17-130">Questo errore viene restituito solo in Windows 2000 quando si tenta di eseguire un'operazione di ridenominazione della tabella nel database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="09a17-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="09a17-131">JET_errInvalidDatabaseId viene restituito per questo caso nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09a17-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="09a17-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="09a17-133">L'ID database specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="09a17-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="09a17-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="09a17-135">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="09a17-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="09a17-136">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="09a17-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="09a17-137">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="09a17-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="09a17-138">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="09a17-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="09a17-139">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="09a17-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="09a17-140">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="09a17-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="09a17-141">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="09a17-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="09a17-142">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="09a17-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="09a17-143">I nomi degli oggetti non possono contenere un punto esclamativo (!), punto (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]), una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09a17-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="09a17-144">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="09a17-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="09a17-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="09a17-146">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="09a17-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="09a17-147">Questo problema può verificarsi per <strong>JetRenameTable</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="09a17-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="09a17-148"><em>szName</em> è null.</span><span class="sxs-lookup"><span data-stu-id="09a17-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="09a17-149"><em>szNameNew</em> è null.</span><span class="sxs-lookup"><span data-stu-id="09a17-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="09a17-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="09a17-151">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="09a17-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="09a17-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="09a17-153">La tabella specificata non esiste per questo database.</span><span class="sxs-lookup"><span data-stu-id="09a17-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="09a17-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="09a17-155">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="09a17-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="09a17-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="09a17-157">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="09a17-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="09a17-158">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09a17-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="09a17-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="09a17-160">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="09a17-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="09a17-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="09a17-162">Non è possibile eseguire un aggiornamento all'interno dell'ambito di una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="09a17-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="09a17-163">Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="09a17-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="09a17-164">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09a17-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09a17-165">In seguito all'esito positivo, il nome della tabella specificata nel database specificato verrà modificato in modo permanente nel nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="09a17-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="09a17-166">In caso di errore, non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="09a17-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="09a17-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09a17-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a17-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-169">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="09a17-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-171">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09a17-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-172"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-173">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="09a17-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-174"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-175">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="09a17-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a17-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-177">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="09a17-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a17-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="09a17-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="09a17-179">Implementato come <strong>JetRenameTableW</strong> (Unicode) e <strong>JetRenameTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="09a17-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="09a17-180">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="09a17-180">See Also</span></span>

[<span data-ttu-id="09a17-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="09a17-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="09a17-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="09a17-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="09a17-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="09a17-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="09a17-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="09a17-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
