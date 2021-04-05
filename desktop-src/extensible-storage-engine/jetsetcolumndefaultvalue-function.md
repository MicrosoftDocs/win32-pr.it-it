---
description: 'Altre informazioni su: funzione JetSetColumnDefaultValue'
title: JetSetColumnDefaultValue (funzione)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878841"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="ee405-103">JetSetColumnDefaultValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee405-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="ee405-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee405-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="ee405-105">JetSetColumnDefaultValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee405-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="ee405-106">La funzione **JetSetColumnDefaultValue** può essere utilizzata per modificare il valore predefinito di una colonna esistente.</span><span class="sxs-lookup"><span data-stu-id="ee405-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ee405-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee405-107">Parameters</span></span>

<span data-ttu-id="ee405-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ee405-108">*sesid*</span></span>

<span data-ttu-id="ee405-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee405-109">The session to use for this call.</span></span>

<span data-ttu-id="ee405-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="ee405-110">*dbid*</span></span>

<span data-ttu-id="ee405-111">Database da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee405-111">The database to use for this call.</span></span>

<span data-ttu-id="ee405-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="ee405-112">*szTableName*</span></span>

<span data-ttu-id="ee405-113">Nome della tabella contenente la colonna interessata.</span><span class="sxs-lookup"><span data-stu-id="ee405-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="ee405-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="ee405-114">*szColumnName*</span></span>

<span data-ttu-id="ee405-115">Nome della colonna il cui valore predefinito verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="ee405-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="ee405-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="ee405-116">*pvData*</span></span>

<span data-ttu-id="ee405-117">Buffer di input contenente il nuovo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee405-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="ee405-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="ee405-118">*cbData*</span></span>

<span data-ttu-id="ee405-119">Dimensioni del buffer di input contenente il nuovo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee405-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="ee405-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ee405-120">*grbit*</span></span>

<span data-ttu-id="ee405-121">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ee405-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="ee405-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee405-122">Return Value</span></span>

<span data-ttu-id="ee405-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ee405-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ee405-124">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ee405-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee405-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ee405-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="ee405-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee405-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee405-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ee405-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ee405-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ee405-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ee405-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ee405-130">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ee405-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="ee405-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="ee405-132">Uguale a JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="ee405-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="ee405-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="ee405-134">Questa colonna specificata è attualmente utilizzata da un indice.</span><span class="sxs-lookup"><span data-stu-id="ee405-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="ee405-135"><strong>JetSetColumnDefaultValue</strong> non è in grado di modificare il valore predefinito di una colonna a cui si fa riferimento nella definizione di un indice.</span><span class="sxs-lookup"><span data-stu-id="ee405-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="ee405-136">Ciò è dovuto al fatto che questa operazione potrebbe modificare il contenuto dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ee405-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="ee405-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="ee405-138">Questa colonna specificata non esiste per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="ee405-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ee405-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ee405-140">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="ee405-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ee405-141">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee405-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ee405-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="ee405-143">L'ID database specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ee405-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ee405-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ee405-145">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="ee405-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="ee405-146">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="ee405-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="ee405-147">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee405-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee405-148">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="ee405-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="ee405-149">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="ee405-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="ee405-150">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="ee405-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="ee405-151">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="ee405-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="ee405-152">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="ee405-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="ee405-153">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="ee405-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="ee405-154">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee405-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="ee405-155">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="ee405-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ee405-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ee405-157">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="ee405-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="ee405-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="ee405-159">Impossibile impostare la colonna su NULL.</span><span class="sxs-lookup"><span data-stu-id="ee405-159">The column could not be set to NULL.</span></span> <span data-ttu-id="ee405-160">Questo errore si verifica per <strong>JetSetColumnDefaultValue</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="ee405-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee405-161"><em>cbData</em> è zero.</span><span class="sxs-lookup"><span data-stu-id="ee405-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="ee405-162"><strong>pvData</strong> è null.</span><span class="sxs-lookup"><span data-stu-id="ee405-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="ee405-163">Pertanto, non è possibile impostare il valore predefinito di una colonna (indietro) su NULL o su un valore di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="ee405-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="ee405-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="ee405-165">La tabella specificata non esiste per questo database.</span><span class="sxs-lookup"><span data-stu-id="ee405-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ee405-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee405-167">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="ee405-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ee405-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ee405-169">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="ee405-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ee405-170">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee405-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="ee405-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="ee405-172">Questa tabella specificata è utilizzata da un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="ee405-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="ee405-173"><strong>JetSetColumnDefaultValue</strong> richiede l'accesso esclusivo a una tabella per poter modificare il valore predefinito della colonna per le versioni precedenti a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ee405-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ee405-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee405-175">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="ee405-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee405-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ee405-177">Non è consentito tentare un aggiornamento quando si trova all'interno dell'ambito di una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ee405-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="ee405-178">Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ee405-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="ee405-179">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee405-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ee405-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ee405-181">Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee405-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="ee405-182">Il tentativo di aggiornamento da questa sessione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ee405-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee405-183">In seguito all'esito positivo, il valore predefinito della colonna specificata nella tabella specificata nel database specificato verrà modificato in modo permanente sul nuovo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee405-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="ee405-184">In caso di errore, non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="ee405-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ee405-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee405-185">Remarks</span></span>

<span data-ttu-id="ee405-186">Non è possibile modificare il valore predefinito di una colonna in una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="ee405-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="ee405-187">Il motore di database tronca automaticamente il valore predefinito di una colonna a 255 byte per il testo lungo e le colonne binarie lunghe.</span><span class="sxs-lookup"><span data-stu-id="ee405-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ee405-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee405-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee405-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-190">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ee405-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-192">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ee405-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-193"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-194">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ee405-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-195"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-196">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ee405-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee405-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-198">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ee405-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee405-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ee405-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ee405-200">Implementato come <strong>JetSetColumnDefaultValueW</strong> (Unicode) e <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ee405-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ee405-201">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ee405-201">See Also</span></span>

[<span data-ttu-id="ee405-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ee405-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ee405-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ee405-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ee405-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ee405-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ee405-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ee405-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ee405-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="ee405-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="ee405-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ee405-207">JetStopService</span></span>](./jetstopservice-function.md)
