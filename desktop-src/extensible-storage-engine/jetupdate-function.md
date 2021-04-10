---
description: 'Altre informazioni su: funzione JetUpdate'
title: Funzione JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879537"
---
# <a name="jetupdate-function"></a><span data-ttu-id="c061b-103">Funzione JetUpdate</span><span class="sxs-lookup"><span data-stu-id="c061b-103">JetUpdate Function</span></span>


<span data-ttu-id="c061b-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c061b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="c061b-105">Funzione JetUpdate</span><span class="sxs-lookup"><span data-stu-id="c061b-105">JetUpdate Function</span></span>

<span data-ttu-id="c061b-106">La funzione **JetUpdate** esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente.</span><span class="sxs-lookup"><span data-stu-id="c061b-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="c061b-107">L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="c061b-108">**JetUpdate** è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="c061b-109">L'aggiornamento viene avviato chiamando [JetPrepareUpdate](./jetprepareupdate-function.md) e chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="c061b-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="c061b-110">Infine, **JetUpdate** viene chiamato per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="c061b-111">Gli indici vengono aggiornati solo da **JetUpdate** o [JetUpdate2](./jetupdate2-function.md)e non durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="c061b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="c061b-112">Parameters</span></span>

<span data-ttu-id="c061b-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c061b-113">*sesid*</span></span>

<span data-ttu-id="c061b-114">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c061b-114">The session to use for this call.</span></span>

<span data-ttu-id="c061b-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c061b-115">*tableid*</span></span>

<span data-ttu-id="c061b-116">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c061b-116">The cursor to use for this call.</span></span>

<span data-ttu-id="c061b-117">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="c061b-117">*pvBookmark*</span></span>

<span data-ttu-id="c061b-118">Puntatore a un segnalibro restituito per una riga inserita.</span><span class="sxs-lookup"><span data-stu-id="c061b-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="c061b-119">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="c061b-119">*cbBookmark*</span></span>

<span data-ttu-id="c061b-120">Dimensioni del buffer a cui punta *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="c061b-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="c061b-121">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="c061b-121">*pcbActual*</span></span>

<span data-ttu-id="c061b-122">Dimensioni restituite del segnalibro per la riga inserita restituita in *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="c061b-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="c061b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c061b-123">Return Value</span></span>

<span data-ttu-id="c061b-124">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c061b-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c061b-125">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c061b-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c061b-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c061b-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="c061b-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c061b-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c061b-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c061b-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c061b-129">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c061b-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c061b-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c061b-131">Il buffer specificato per il segnalibro di record non è sufficientemente grande per l'archiviazione del segnalibro del record.</span><span class="sxs-lookup"><span data-stu-id="c061b-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c061b-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c061b-133">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c061b-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="c061b-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="c061b-135">Uguale a JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="c061b-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="c061b-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="c061b-137">L'operazione di aggiornamento richiede la crescita del file di database o l'allocazione dei file di log, ma l'unità disco in cui risiede il file di database o la serie di log è piena.</span><span class="sxs-lookup"><span data-stu-id="c061b-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="c061b-138">In alternativa, il file di database si trova in un volume formattato FAT32 e il file di database è già 4GBytes, il limite per file per FAT32.</span><span class="sxs-lookup"><span data-stu-id="c061b-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c061b-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c061b-140">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="c061b-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c061b-141"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c061b-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c061b-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c061b-143">Il parametro <em>Prep</em> specificato nella funzione <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> non è un flag valido.</span><span class="sxs-lookup"><span data-stu-id="c061b-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="c061b-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="c061b-145">Una chiave di indice per questo record è un duplicato di un'altra chiave di indice per un altro record già presente nella tabella e l'indice non consente duplicati.</span><span class="sxs-lookup"><span data-stu-id="c061b-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="c061b-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="c061b-147">Il record inserito o aggiornato presenta uno o più indici per i quali la chiave generata avrebbe superato le dimensioni massime consentite.</span><span class="sxs-lookup"><span data-stu-id="c061b-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="c061b-148">Di conseguenza, l'operazione non è riuscita a impedire il troncamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="c061b-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="c061b-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="c061b-150">Il record inserito o aggiornato ha una colonna multivalore indicizzata con due o più valori identici all'interno delle dimensioni della chiave di lunghezza massima impostate per l'indice.</span><span class="sxs-lookup"><span data-stu-id="c061b-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="c061b-151">Di conseguenza, nel record sono presenti due voci identiche nell'indice che non sono valide.</span><span class="sxs-lookup"><span data-stu-id="c061b-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c061b-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c061b-153">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c061b-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="c061b-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="c061b-155">Una o più colonne del record da inserire o nello stato aggiornato di un record da sostituire è <strong>null</strong> , che viola il vincolo definito per tali colonne.</span><span class="sxs-lookup"><span data-stu-id="c061b-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="c061b-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="c061b-157">Uno o più indici sono definiti per non consentire una chiave <strong>null</strong> e lo stato inserito o aggiornato di un record sostituito viola questo vincolo definito.</span><span class="sxs-lookup"><span data-stu-id="c061b-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="c061b-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="c061b-159">Un'operazione di sostituzione di record ha aggiornato la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="c061b-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="c061b-160">Gli aggiornamenti alle colonne chiave primaria devono essere eseguiti tramite l'eliminazione del record esistente e l'inserimento di un nuovo record con i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="c061b-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c061b-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c061b-162">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c061b-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c061b-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c061b-164">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c061b-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c061b-165"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c061b-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c061b-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c061b-167">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="c061b-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="c061b-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="c061b-169">Non è consentito tentare un aggiornamento quando si trova all'interno dell'ambito di una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c061b-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="c061b-170">Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="c061b-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="c061b-171"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c061b-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="c061b-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="c061b-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> è stato chiamato con JET_prepCancel ma il cursore non si trovava nello stato preparato.</span><span class="sxs-lookup"><span data-stu-id="c061b-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c061b-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c061b-175">Operazione non riuscita perché la memoria disponibile non è sufficiente per mantenere le informazioni transazionali sull'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="c061b-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="c061b-177">Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="c061b-178">Il tentativo di aggiornamento da questa sessione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c061b-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c061b-179">Al termine dell'operazione, l'operazione di apertura aggiornamento sul cursore viene completata.</span><span class="sxs-lookup"><span data-stu-id="c061b-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="c061b-180">Se per la tabella è definita una colonna con incremento automatico, questo valore viene impostato per i record inseriti.</span><span class="sxs-lookup"><span data-stu-id="c061b-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="c061b-181">Se per la tabella è definita una colonna della versione, il relativo valore viene inizializzato per i nuovi record inseriti o incrementato ogni volta che un record viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="c061b-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="c061b-182">Tutti gli indici, inclusi gli indici cluster e non cluster, vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="c061b-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="c061b-183">In caso di errore, non viene apportata alcuna modifica al database.</span><span class="sxs-lookup"><span data-stu-id="c061b-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="c061b-184">È possibile che siano state richiamate le funzioni di callback before INSERT e before, ma dopo che i callback di Replace e After non sono state richiamate, poiché quest'ultimo non può causare errori di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="c061b-185">Il buffer di copia del cursore viene lasciato nello stato preparato, in modo che esista un'opportunità per correggere in modo incrementale i problemi che hanno causato errori e ripetere l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c061b-186">Commenti</span><span class="sxs-lookup"><span data-stu-id="c061b-186">Remarks</span></span>

<span data-ttu-id="c061b-187">Le funzioni di callback possono essere registrate per essere chiamate prima o dopo l'inserimento e prima o dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c061b-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="c061b-188">Le limitazioni relative alle dimensioni dei record vengono applicate da [JetSetColumn](./jetsetcolumn-function.md)e non in generale da **JetUpdate**.</span><span class="sxs-lookup"><span data-stu-id="c061b-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="c061b-189">È importante comprendere l'effetto dell'esecuzione di un numero elevato di operazioni di aggiornamento all'interno di una singola transazione.</span><span class="sxs-lookup"><span data-stu-id="c061b-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="c061b-190">Ogni aggiornamento del database deve essere rilevato dal motore di database nell'archivio delle versioni.</span><span class="sxs-lookup"><span data-stu-id="c061b-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="c061b-191">L'archivio versione include un record live di tutte le diverse versioni di ogni voce di record o di indice nel database che possono essere visualizzate da tutte le transazioni attive.</span><span class="sxs-lookup"><span data-stu-id="c061b-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="c061b-192">Queste versioni vengono utilizzate per supportare il controllo della concorrenza multiversione utilizzato dal motore di database per supportare le transazioni mediante l'isolamento dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="c061b-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="c061b-193">Una volta che il motore di database ha esaurito le risorse usate per archiviare queste versioni, non può più accettare ulteriori modifiche fino a quando alcune transazioni non sono state terminate per consentire il ripristino di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="c061b-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="c061b-194">Quando il motore è in questo stato, tutti gli aggiornamenti avranno esito negativo con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c061b-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="c061b-195">Le risorse disponibili per il motore di database per archiviare queste versioni possono essere controllate utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramMaxVerPages](./resource-parameters.md) e [JET_paramGlobalMinVerPages](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c061b-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c061b-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c061b-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c061b-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c061b-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c061b-198">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c061b-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c061b-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c061b-200">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c061b-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-201"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c061b-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c061b-202">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c061b-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c061b-203"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c061b-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c061b-204">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c061b-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c061b-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c061b-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c061b-206">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c061b-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c061b-207">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c061b-207">See Also</span></span>

[<span data-ttu-id="c061b-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c061b-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c061b-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c061b-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c061b-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c061b-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c061b-211">JetDelete</span><span class="sxs-lookup"><span data-stu-id="c061b-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="c061b-212">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="c061b-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="c061b-213">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="c061b-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="c061b-214">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="c061b-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="c061b-215">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="c061b-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="c061b-216">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="c061b-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="c061b-217">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c061b-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="c061b-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c061b-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c061b-219">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="c061b-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
