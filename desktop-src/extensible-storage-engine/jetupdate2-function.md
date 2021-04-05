---
description: 'Altre informazioni su: funzione JetUpdate2'
title: Funzione JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750474"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="8afb2-103">Funzione JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="8afb2-103">JetUpdate2 Function</span></span>


<span data-ttu-id="8afb2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8afb2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="8afb2-105">Funzione JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="8afb2-105">JetUpdate2 Function</span></span>

<span data-ttu-id="8afb2-106">La funzione **JetUpdate2** esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente.</span><span class="sxs-lookup"><span data-stu-id="8afb2-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="8afb2-107">Questa funzione contiene un elenco di opzioni di *grbit* che possono essere impostate durante l'esecuzione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="8afb2-108">L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="8afb2-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="8afb2-109">**Windows server 2003: JetUpdate2** è stato introdotto in windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8afb2-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="8afb2-110">**JetUpdate2** è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="8afb2-111">L'aggiornamento viene avviato chiamando [JetPrepareUpdate](./jetprepareupdate-function.md) e chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="8afb2-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="8afb2-112">Infine, **JetUpdate2** viene chiamato per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="8afb2-113">Gli indici vengono aggiornati solo da [JetUpdate](./jetupdate-function.md) o **JetUpdate2** e non durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="8afb2-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8afb2-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="8afb2-114">Parameters</span></span>

<span data-ttu-id="8afb2-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8afb2-115">*sesid*</span></span>

<span data-ttu-id="8afb2-116">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="8afb2-116">The session to use for this call.</span></span>

<span data-ttu-id="8afb2-117">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8afb2-117">*tableid*</span></span>

<span data-ttu-id="8afb2-118">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="8afb2-118">The cursor to use for this call.</span></span>

<span data-ttu-id="8afb2-119">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="8afb2-119">*pvBookmark*</span></span>

<span data-ttu-id="8afb2-120">Puntatore a un segnalibro restituito per una riga inserita.</span><span class="sxs-lookup"><span data-stu-id="8afb2-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="8afb2-121">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="8afb2-121">*cbBookmark*</span></span>

<span data-ttu-id="8afb2-122">Dimensioni del buffer a cui punta *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="8afb2-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="8afb2-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="8afb2-123">*pcbActual*</span></span>

<span data-ttu-id="8afb2-124">Dimensioni restituite del segnalibro per la riga inserita restituita in *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="8afb2-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="8afb2-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8afb2-125">*grbit*</span></span>

<span data-ttu-id="8afb2-126">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8afb2-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8afb2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8afb2-127">Value</span></span></p></th>
<th><p><span data-ttu-id="8afb2-128">Significato</span><span class="sxs-lookup"><span data-stu-id="8afb2-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="8afb2-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="8afb2-130">Questo flag fa in modo che l'aggiornamento restituisca un errore se l'aggiornamento non è stato possibile nella versione Windows 2000 di ESE, che ha applicato un numero massimo di istanze di colonna multivalore inferiore in ogni record rispetto alle versioni successive di ESE.</span><span class="sxs-lookup"><span data-stu-id="8afb2-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="8afb2-131">Questo aspetto è importante solo per le applicazioni che vogliono replicare i dati tra le applicazioni ospitate in Windows 2000 e le applicazioni ospitate in Windows Server 2003 o versioni successive di ESE.</span><span class="sxs-lookup"><span data-stu-id="8afb2-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="8afb2-132">Non dovrebbe essere necessario per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8afb2-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8afb2-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8afb2-133">Return Value</span></span>

<span data-ttu-id="8afb2-134">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="8afb2-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8afb2-135">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="8afb2-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8afb2-136">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8afb2-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="8afb2-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8afb2-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8afb2-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8afb2-139">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8afb2-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="8afb2-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="8afb2-141">Il buffer specificato per il segnalibro di record non è sufficientemente grande per l'archiviazione del segnalibro del record.</span><span class="sxs-lookup"><span data-stu-id="8afb2-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8afb2-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8afb2-143">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8afb2-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="8afb2-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="8afb2-145">L'operazione di aggiornamento richiede la crescita del file di database o l'allocazione dei file di log, ma l'unità disco in cui risiede il file di database o la serie di log è piena.</span><span class="sxs-lookup"><span data-stu-id="8afb2-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="8afb2-146">In alternativa, il file di database si trova in un volume formattato FAT32 e il file di database è già 4GBytes, il limite per file per FAT32.</span><span class="sxs-lookup"><span data-stu-id="8afb2-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8afb2-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8afb2-148">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="8afb2-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8afb2-149"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8afb2-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8afb2-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8afb2-151">Il parametro <em>Prep</em> specificato nella funzione <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> non è un flag valido.</span><span class="sxs-lookup"><span data-stu-id="8afb2-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="8afb2-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="8afb2-153">Una chiave di indice per questo record è un duplicato di un'altra chiave di indice per un altro record già presente nella tabella e l'indice non consente duplicati.</span><span class="sxs-lookup"><span data-stu-id="8afb2-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="8afb2-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="8afb2-155">Il record inserito o aggiornato presenta uno o più indici per i quali la chiave generata avrebbe superato le dimensioni massime consentite.</span><span class="sxs-lookup"><span data-stu-id="8afb2-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="8afb2-156">Di conseguenza, l'operazione non è riuscita a impedire il troncamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="8afb2-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="8afb2-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="8afb2-158">Il record inserito o aggiornato ha una colonna multivalore indicizzata con due o più valori identici all'interno delle dimensioni della chiave di lunghezza massima impostate per l'indice.</span><span class="sxs-lookup"><span data-stu-id="8afb2-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="8afb2-159">Di conseguenza, nel record sono presenti due voci identiche nell'indice che non sono valide.</span><span class="sxs-lookup"><span data-stu-id="8afb2-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8afb2-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8afb2-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="8afb2-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="8afb2-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="8afb2-163">Una o più colonne del record da inserire o nello stato aggiornato di un record da sostituire è <strong>null</strong> , che viola il vincolo definito per tali colonne.</span><span class="sxs-lookup"><span data-stu-id="8afb2-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="8afb2-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="8afb2-165">Uno o più indici sono definiti per non consentire una chiave <strong>null</strong> e lo stato inserito o aggiornato di un record sostituito viola questo vincolo definito.</span><span class="sxs-lookup"><span data-stu-id="8afb2-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="8afb2-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="8afb2-167">Un'operazione di sostituzione di record ha aggiornato la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="8afb2-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="8afb2-168">Gli aggiornamenti alle colonne chiave primaria devono essere eseguiti tramite l'eliminazione del record esistente e l'inserimento di un nuovo record con i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="8afb2-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8afb2-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8afb2-170">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="8afb2-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8afb2-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8afb2-172">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8afb2-173"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8afb2-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8afb2-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8afb2-175">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="8afb2-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="8afb2-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="8afb2-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> è stato chiamato con JET_prepCancel ma il cursore non si trovava nello stato preparato.</span><span class="sxs-lookup"><span data-stu-id="8afb2-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="8afb2-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="8afb2-179">Un'operazione di sostituzione di record per cui un blocco di scrittura non è già stato allocato può riscontrare un conflitto di scrittura al momento dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8afb2-180">Al termine dell'operazione, l'operazione di apertura aggiornamento sul cursore viene completata.</span><span class="sxs-lookup"><span data-stu-id="8afb2-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="8afb2-181">Se per la tabella è definita una colonna con incremento automatico, questo valore viene impostato per i record inseriti.</span><span class="sxs-lookup"><span data-stu-id="8afb2-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="8afb2-182">Se per la tabella è definita una colonna della versione, il relativo valore viene inizializzato per i nuovi record inseriti o incrementato ogni volta che un record viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="8afb2-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="8afb2-183">Tutti gli indici, inclusi gli indici cluster e non cluster, vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="8afb2-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="8afb2-184">In caso di errore, non viene apportata alcuna modifica al database.</span><span class="sxs-lookup"><span data-stu-id="8afb2-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="8afb2-185">È possibile che siano state richiamate le funzioni di callback before INSERT e before, ma dopo che i callback di Replace e After non sono state richiamate, poiché quest'ultimo non può causare errori di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="8afb2-186">Il buffer di copia del cursore viene lasciato nello stato preparato, in modo che esista un'opportunità per correggere in modo incrementale i problemi che hanno causato errori e ripetere l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8afb2-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8afb2-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="8afb2-187">Remarks</span></span>

<span data-ttu-id="8afb2-188">Le limitazioni relative alle dimensioni dei record vengono applicate da [JetSetColumn](./jetsetcolumn-function.md)e non in generale da [JetUpdate](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="8afb2-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="8afb2-189">L'unica eccezione si verifica quando viene utilizzato il flag di compatibilità JET_bitUpdateCheckESE97Compatibility.</span><span class="sxs-lookup"><span data-stu-id="8afb2-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="8afb2-190">In questo caso, l'intero record viene controllato perché una singola operazione [JetSetColumn](./jetsetcolumn-function.md) che supera il limite può essere compensata da una chiamata successiva a [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="8afb2-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="8afb2-191">Per ulteriori informazioni, vedere la sezione Osservazioni in [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="8afb2-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8afb2-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8afb2-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-193"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8afb2-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8afb2-194">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8afb2-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-195"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8afb2-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8afb2-196">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8afb2-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-197"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="8afb2-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8afb2-198">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="8afb2-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb2-199"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="8afb2-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8afb2-200">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8afb2-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb2-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8afb2-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8afb2-202">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8afb2-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8afb2-203">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8afb2-203">See Also</span></span>

[<span data-ttu-id="8afb2-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8afb2-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8afb2-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8afb2-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8afb2-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8afb2-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8afb2-207">JetDelete</span><span class="sxs-lookup"><span data-stu-id="8afb2-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="8afb2-208">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="8afb2-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="8afb2-209">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="8afb2-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="8afb2-210">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="8afb2-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="8afb2-211">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="8afb2-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="8afb2-212">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="8afb2-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="8afb2-213">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="8afb2-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
