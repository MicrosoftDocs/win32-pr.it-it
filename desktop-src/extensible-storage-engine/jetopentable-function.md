---
description: 'Altre informazioni su: funzione JetOpenTable'
title: Funzione JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749706"
---
# <a name="jetopentable-function"></a><span data-ttu-id="04265-103">Funzione JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="04265-103">JetOpenTable Function</span></span>


<span data-ttu-id="04265-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="04265-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="04265-105">Funzione JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="04265-105">JetOpenTable Function</span></span>

<span data-ttu-id="04265-106">La funzione **JetOpenTable** apre un cursore su una tabella creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="04265-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="04265-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="04265-107">Parameters</span></span>

<span data-ttu-id="04265-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="04265-108">*sesid*</span></span>

<span data-ttu-id="04265-109">Contesto della sessione di database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="04265-109">The database session context to use.</span></span>

<span data-ttu-id="04265-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="04265-110">*dbid*</span></span>

<span data-ttu-id="04265-111">Identificatore del database da utilizzare per trovare la tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="04265-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="04265-112">*szTableName*</span></span>

<span data-ttu-id="04265-113">Nome della tabella da aprire.</span><span class="sxs-lookup"><span data-stu-id="04265-113">The name of the table to open.</span></span>

<span data-ttu-id="04265-114">*pvParameters*</span><span class="sxs-lookup"><span data-stu-id="04265-114">*pvParameters*</span></span>

<span data-ttu-id="04265-115">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04265-115">Deprecated.</span></span> <span data-ttu-id="04265-116">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="04265-116">Set to **NULL**.</span></span>

<span data-ttu-id="04265-117">*cbParameters*</span><span class="sxs-lookup"><span data-stu-id="04265-117">*cbParameters*</span></span>

<span data-ttu-id="04265-118">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04265-118">Deprecated.</span></span> <span data-ttu-id="04265-119">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="04265-119">Set to 0 (zero).</span></span>

<span data-ttu-id="04265-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="04265-120">*grbit*</span></span>

<span data-ttu-id="04265-121">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="04265-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04265-122">Valore</span><span class="sxs-lookup"><span data-stu-id="04265-122">Value</span></span></p></th>
<th><p><span data-ttu-id="04265-123">Significato</span><span class="sxs-lookup"><span data-stu-id="04265-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04265-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="04265-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="04265-125">Non è possibile aprire la tabella per l'accesso in lettura da parte di un'altra sessione di database.</span><span class="sxs-lookup"><span data-stu-id="04265-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="04265-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="04265-127">Non è possibile aprire la tabella per l'accesso in scrittura da parte di un'altra sessione di database.</span><span class="sxs-lookup"><span data-stu-id="04265-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="04265-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="04265-129">Non memorizzare nella cache le pagine per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="04265-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="04265-131">Consente la modifica DDL nelle tabelle contrassegnate come FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="04265-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="04265-132">Questa opzione deve essere utilizzata con l'opzione JET_bitTableDenyRead.</span><span class="sxs-lookup"><span data-stu-id="04265-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="04265-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="04265-134">Fornisce un suggerimento che la tabella non è probabilmente nella cache del buffer e che la pre-lettura può essere utile per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="04265-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="04265-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="04265-136">Richiede l'accesso in sola lettura alla tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="04265-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="04265-138">La tabella deve essere precaricata in modo molto aggressivo dal disco poiché verrà analizzata in sequenza dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="04265-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="04265-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="04265-140">Richiede l'accesso in scrittura alla tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="04265-141">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="04265-141">*ptableid*</span></span>

<span data-ttu-id="04265-142">In seguito all'esito positivo, punta all'identificatore della tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="04265-143">In caso di errore, il contenuto di *pTableID* non è definito.</span><span class="sxs-lookup"><span data-stu-id="04265-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="04265-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04265-144">Return Value</span></span>

<span data-ttu-id="04265-145">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="04265-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="04265-146">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="04265-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04265-147">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="04265-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="04265-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04265-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04265-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="04265-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="04265-150">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="04265-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="04265-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="04265-152"><em>dbid</em> non è un identificatore di database valido.</span><span class="sxs-lookup"><span data-stu-id="04265-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="04265-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="04265-154">È stata passata una combinazione non valida di <em>grbit</em> .</span><span class="sxs-lookup"><span data-stu-id="04265-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="04265-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="04265-156">Il nome specificato in <em>szTableName</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="04265-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="04265-157">Per ulteriori informazioni sui nomi di tabella validi, vedere il parametro <em>szTableName</em> in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span><span class="sxs-lookup"><span data-stu-id="04265-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="04265-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="04265-159">È stato effettuato un tentativo di aprire una tabella che non esiste nel database.</span><span class="sxs-lookup"><span data-stu-id="04265-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="04265-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="04265-161">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="04265-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="04265-162">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="04265-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="04265-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="04265-164">La tabella è utilizzata da un'altra operazione di database.</span><span class="sxs-lookup"><span data-stu-id="04265-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="04265-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="04265-166">Avviso non irreversibile che indica che la tabella è utilizzata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="04265-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="04265-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="04265-168">La tabella è bloccata da un'altra operazione di database.</span><span class="sxs-lookup"><span data-stu-id="04265-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="04265-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="04265-170">È stato effettuato un tentativo di apertura di un numero eccessivo di tabelle univoche in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="04265-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="04265-171">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="04265-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="04265-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="04265-172">Remarks</span></span>

<span data-ttu-id="04265-173">Le tabelle aperte con **JetOpenTable** devono essere in genere chiuse con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="04265-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="04265-174">L'eccezione a questa regola si verifica quando **JetOpenTable** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="04265-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="04265-175">Quando si esegue il rollback di una transazione, la tabella viene chiusa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="04265-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="04265-176">In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="04265-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="04265-177">È lecito aprire le tabelle di sistema con **JetOpenTable** , ad esempio MSysObjects, MSysUnicodeFixup.</span><span class="sxs-lookup"><span data-stu-id="04265-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="04265-178">È possibile che lo schema delle tabelle di sistema venga modificato, pertanto l'accesso alle tabelle di sistema è sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="04265-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="04265-179">Il numero di tabelle univoche che possono essere aperte contemporaneamente è interessato direttamente da *JET_paramMaxOpenTables*.</span><span class="sxs-lookup"><span data-stu-id="04265-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="04265-180">Se la tabella è attualmente aperta, verrà creato un nuovo cursore nella tabella.</span><span class="sxs-lookup"><span data-stu-id="04265-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="04265-181">Le risorse del cursore vengono configurate utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxCursors*.</span><span class="sxs-lookup"><span data-stu-id="04265-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="04265-182">Vedere anche [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="04265-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="04265-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04265-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04265-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="04265-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-185">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="04265-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="04265-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-187">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="04265-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-188"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="04265-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-189">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="04265-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-190"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="04265-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-191">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="04265-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04265-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="04265-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-193">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="04265-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04265-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="04265-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="04265-195">Implementato come <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="04265-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="04265-196">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="04265-196">See Also</span></span>

[<span data-ttu-id="04265-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="04265-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="04265-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="04265-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="04265-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="04265-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="04265-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="04265-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="04265-201">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="04265-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="04265-202">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="04265-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="04265-203">JetRollback</span><span class="sxs-lookup"><span data-stu-id="04265-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="04265-204">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="04265-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="04265-205">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="04265-205">Resource Parameters</span></span>](./resource-parameters.md)
