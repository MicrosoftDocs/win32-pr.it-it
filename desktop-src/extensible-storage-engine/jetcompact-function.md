---
description: 'Altre informazioni su: funzione JetCompact'
title: JetCompact (funzione)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313106"
---
# <a name="jetcompact-function"></a><span data-ttu-id="f4cb2-103">JetCompact (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4cb2-103">JetCompact Function</span></span>


<span data-ttu-id="f4cb2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f4cb2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="f4cb2-105">JetCompact (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4cb2-105">JetCompact Function</span></span>

<span data-ttu-id="f4cb2-106">La funzione **JetCompact** crea una copia di un database esistente.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="f4cb2-107">La copia viene compattata in uno stato ottimale per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="f4cb2-108">I dati nei dati copiati verranno compressi in base alle misure scelte per gli indici in fase di creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="f4cb2-109">In questo modo, i dati compressi possono essere archiviati nel modo più denso possibile.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="f4cb2-110">In alternativa, i dati compressi possono riservare spazio per gli inserimenti di indici o di crescita successivi.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f4cb2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4cb2-111">Parameters</span></span>

<span data-ttu-id="f4cb2-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-112">*sesid*</span></span>

<span data-ttu-id="f4cb2-113">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-113">The session to use for this call.</span></span>

<span data-ttu-id="f4cb2-114">*szDatabaseSrc*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="f4cb2-115">Database di origine che verrà compattato.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-115">The source database that will be compacted.</span></span>

<span data-ttu-id="f4cb2-116">*szDatabaseDest*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-116">*szDatabaseDest*</span></span>

<span data-ttu-id="f4cb2-117">Nome da utilizzare per il database compresso.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="f4cb2-118">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-118">*pfnStatus*</span></span>

<span data-ttu-id="f4cb2-119">Funzione di callback che può essere chiamata periodicamente tramite l'operazione di compattazione del database per segnalare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="f4cb2-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-120">*pconvert*</span></span>

<span data-ttu-id="f4cb2-121">Puntatore utilizzato per designare una DLL ESE alternativa che può essere utilizzata per leggere il database di origine e per fornire parametri facoltativi per un'operazione **JetCompact** che converte un database da un formato precedente a una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="f4cb2-122">Questa funzionalità è stata sospesa in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="f4cb2-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f4cb2-123">*grbit*</span></span>

<span data-ttu-id="f4cb2-124">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4cb2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f4cb2-125">Value</span></span></p></th>
<th><p><span data-ttu-id="f4cb2-126">Significato</span><span class="sxs-lookup"><span data-stu-id="f4cb2-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="f4cb2-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-128">Utilizzato quando è noto che il database di origine è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="f4cb2-129">Consente un intero set di nuovi comportamenti destinati a recuperare il maggior quantità possibile di dati dal database di origine.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="f4cb2-130"><strong>JetCompact</strong> con questo set di opzioni può restituire JET_errSuccess ma non copiare tutti i dati creati nel database di origine.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="f4cb2-131">I dati che si trovavano in parti danneggiate del database di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="f4cb2-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-133">Consente a <strong>JetCompact</strong> di eseguire il dump delle statistiche nel database di origine in un file denominato DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="f4cb2-134">Le statistiche includono il nome di ogni tabella nel database di origine, il numero di righe in ogni tabella, le dimensioni totali in byte di tutte le righe di ogni tabella, le dimensioni totali in byte di tutte le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> che erano sufficientemente grandi da essere archiviate separate dal record, il numero di pagine foglia dell'indice cluster e il numero di pagine foglia di valore lungo.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="f4cb2-135">Inoltre, le statistiche di riepilogo, incluse le dimensioni del database di origine, il database di destinazione, il tempo necessario per la compattazione del database, hanno anche tutti il dump dello spazio.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f4cb2-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4cb2-136">Return Value</span></span>

<span data-ttu-id="f4cb2-137">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f4cb2-138">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f4cb2-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4cb2-139">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f4cb2-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="f4cb2-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4cb2-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f4cb2-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-142">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f4cb2-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-144">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="f4cb2-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-146">È stato fornito un puntatore <em>PConvert</em> non null, ma la versione di ESE utilizzata non supporta la funzionalità di conversione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="f4cb2-147">Questa funzionalità è stata rimossa nella versione di ESE di Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f4cb2-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f4cb2-150">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="f4cb2-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-152">La sessione chiamante si trova all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-152">The calling session is within a transaction.</span></span> <span data-ttu-id="f4cb2-153"><strong>JetCompact</strong> deve essere chiamato da una sessione all'esterno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f4cb2-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-155">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f4cb2-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-157">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f4cb2-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-159">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f4cb2-160">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f4cb2-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4cb2-162">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4cb2-163">In seguito all'esito positivo, il database di origine viene copiato nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="f4cb2-164">Lo stato del database di destinazione è ottimale. ad esempio, tutti gli indici di tabella si trovano nello spazio su disco logico adiacente.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="f4cb2-165">Ogni pagina di indice viene riempita fino alla quantità configurata quando gli indici sono stati creati originariamente nel database di origine.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="f4cb2-166">Tutte le impostazioni di dati e metadati vengono copiate con la massima fedeltà, a meno che non sia stata specificata l'opzione di correzione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="f4cb2-167">Se è stata specificata l'opzione di correzione, è possibile che alcuni dati del database di origine non siano stati copiati.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="f4cb2-168">In caso di errore, il database di destinazione può esistere, ma non è una copia completa del database di origine.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f4cb2-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4cb2-169">Remarks</span></span>

<span data-ttu-id="f4cb2-170">La compattazione di un database viene inoltre utilizzata per aggiornare un database da un formato di versione precedente a una versione più recente.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="f4cb2-171">Un parametro facoltativo è *PConvert*, che contiene una struttura in grado di contenere una descrizione di una DLL di versione precedente da utilizzare per la lettura del formato del database di origine.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="f4cb2-172">Questa funzionalità è stata sospesa in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="f4cb2-173">Successivamente a Windows Server 2003, le nuove versioni di ESE sono sempre in grado di leggere le versioni precedenti del formato del database e pertanto questa funzionalità non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="f4cb2-174">La densità desiderata dei dati dopo un'operazione di compattazione viene specificata quando vengono creati tabelle e indici.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="f4cb2-175">La densità deve essere compresa tra il 20% e il 100%.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="f4cb2-176">Se un database viene letto e non aggiornato principalmente, le applicazioni imposteranno la densità su 100% per ridurre il numero di operazioni di I/O durante l'elaborazione della query.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="f4cb2-177">Tuttavia, se i dati vengono aggiornati di frequente con operazioni che aumentano le dimensioni dei dati archiviati insieme al record, o vengono inseriti di frequente nuovi dati, l'applicazione sceglierà una densità inferiore in modo che gli aggiornamenti rileveranno più spesso le risorse necessarie disponibili.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="f4cb2-178">Con l'operazione di compattazione del database, il database viene disposto idealmente in base al riempimento scelto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="f4cb2-179">La compattazione del database è un'operazione non in linea.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="f4cb2-180">Non può essere eseguita mentre il database è in uso.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="f4cb2-181">Di conseguenza, viene in genere eseguito come parte di un processo di compilazione per lo sviluppo di un'applicazione che fornisce un set di dati come parte di se stesso.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="f4cb2-182">La compattazione del database offline tocca ogni bit di dati in un database e può essere utilizzata come mezzo per verificare la coerenza di un database.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="f4cb2-183">Se un database è sospetto, può essere compattato.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="f4cb2-184">Se non viene rilevato alcun errore dalla compattazione, sarà noto che il database è in uno stato valido per ESE.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f4cb2-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4cb2-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-187">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-189">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-190"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-191">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-192"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-193">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4cb2-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-195">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f4cb2-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4cb2-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f4cb2-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f4cb2-197">Implementato come <strong>JetCompactW</strong> (Unicode) e <strong>JetCompactA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f4cb2-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f4cb2-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f4cb2-198">See Also</span></span>

[<span data-ttu-id="f4cb2-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="f4cb2-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="f4cb2-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f4cb2-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f4cb2-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f4cb2-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f4cb2-202">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="f4cb2-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="f4cb2-203">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f4cb2-203">JetStopService</span></span>](./jetstopservice-function.md)
