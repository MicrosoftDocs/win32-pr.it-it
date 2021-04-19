---
description: 'Altre informazioni su: funzione JetBeginExternalBackup'
title: JetBeginExternalBackup (funzione)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318100"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="8827b-103">JetBeginExternalBackup (funzione)</span><span class="sxs-lookup"><span data-stu-id="8827b-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="8827b-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8827b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="8827b-105">JetBeginExternalBackup (funzione)</span><span class="sxs-lookup"><span data-stu-id="8827b-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="8827b-106">La funzione **JetBeginExternalBackup** avvia un backup esterno mentre il motore e il database sono online e attivi.</span><span class="sxs-lookup"><span data-stu-id="8827b-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="8827b-107">**JetBeginExternalBackup** è il primo di una serie di funzioni che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.</span><span class="sxs-lookup"><span data-stu-id="8827b-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="8827b-108">Un backup esterno può essere utilizzato per implementare backup completi, incrementali o differenziali.</span><span class="sxs-lookup"><span data-stu-id="8827b-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="8827b-109">Il backup sarà fuzzy, in quanto il backup sarà coerente a un singolo momento della cronologia delle transazioni, ma non è possibile controllare il punto nel tempo esatto.</span><span class="sxs-lookup"><span data-stu-id="8827b-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8827b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8827b-110">Parameters</span></span>

<span data-ttu-id="8827b-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8827b-111">*grbit*</span></span>

<span data-ttu-id="8827b-112">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8827b-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8827b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8827b-113">Value</span></span></p></th>
<th><p><span data-ttu-id="8827b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="8827b-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8827b-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="8827b-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="8827b-116">Questo flag è deprecato.</span><span class="sxs-lookup"><span data-stu-id="8827b-116">This flag is deprecated.</span></span> <span data-ttu-id="8827b-117">L'utilizzo di questo bit comporterà la restituzione JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="8827b-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="8827b-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="8827b-119">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="8827b-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="8827b-120">Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="8827b-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="8827b-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="8827b-122">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="8827b-122">Reserved for future use.</span></span> <span data-ttu-id="8827b-123">Definito per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8827b-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8827b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8827b-124">Return Value</span></span>

<span data-ttu-id="8827b-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="8827b-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8827b-126">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="8827b-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8827b-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8827b-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="8827b-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8827b-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8827b-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8827b-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8827b-130">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8827b-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="8827b-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="8827b-132">Se è già in corso un backup o un backup di snapshot esterno, verrà restituito questo errore fino a quando non viene chiamato <strong>JetBeginExternalBackup</strong> (o una delle varianti).</span><span class="sxs-lookup"><span data-stu-id="8827b-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="8827b-133">ESE consente un solo backup online alla volta.</span><span class="sxs-lookup"><span data-stu-id="8827b-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="8827b-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="8827b-135">L'istanza o il motore di database è in fase di ripristino oppure in fase di arresto o chiusura.</span><span class="sxs-lookup"><span data-stu-id="8827b-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="8827b-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="8827b-137">In un backup completo non è stato possibile leggere il file del checkpoint oppure il file non è stato verificato.</span><span class="sxs-lookup"><span data-stu-id="8827b-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="8827b-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="8827b-139">In un backup completo non è stato possibile trovare il file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="8827b-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8827b-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8827b-141">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8827b-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8827b-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8827b-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="8827b-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8827b-144"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8827b-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="8827b-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="8827b-146">La registrazione circolare è abilitata e il tipo di backup specificato viene JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="8827b-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="8827b-147">Per informazioni su come controllare la registrazione circolare o non circolare, vedere <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> negli <strong>errori del log delle transazioni</strong> .</span><span class="sxs-lookup"><span data-stu-id="8827b-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="8827b-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="8827b-149">Uno o più membri di <em>grbit</em> non sono validi.</span><span class="sxs-lookup"><span data-stu-id="8827b-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="8827b-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="8827b-151">Il ripristino o la registrazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="8827b-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="8827b-152">Se la registrazione è disabilitata, non è possibile eseguire un backup in linea.</span><span class="sxs-lookup"><span data-stu-id="8827b-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="8827b-153">Per ulteriori informazioni sulla registrazione e il ripristino, vedere <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="8827b-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="8827b-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="8827b-155">Il motore ha smesso di scrivere nell'unità di log, a causa di errori di i/o del disco e completi.</span><span class="sxs-lookup"><span data-stu-id="8827b-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="8827b-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="8827b-157">Il backup incrementale è stato specificato (con JET_bitBackupIncremental) e non è mai stato eseguito un backup completo per uno dei database collegati per il set di registrazione.</span><span class="sxs-lookup"><span data-stu-id="8827b-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8827b-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8827b-159">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="8827b-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="8827b-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="8827b-161">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="8827b-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8827b-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8827b-163">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="8827b-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="8827b-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="8827b-165">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="8827b-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8827b-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8827b-167">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="8827b-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8827b-168">Se la funzione ha esito positivo, viene avviato un backup esterno e viene inizializzato il motore dello stato di backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="8827b-169">È ora possibile chiamare le API successive per completare la sequenza di backup esterna e trasmettere o leggere il file di database, il file di patch del database (se supportato) e il file di log.</span><span class="sxs-lookup"><span data-stu-id="8827b-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="8827b-170">È possibile registrare un evento in cui è stato avviato un backup esterno.</span><span class="sxs-lookup"><span data-stu-id="8827b-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="8827b-171">Se la funzione ha esito negativo, la sessione di backup non verrà avviata.</span><span class="sxs-lookup"><span data-stu-id="8827b-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="8827b-172">Se è in corso un'altra sessione di backup, non verrà annullata.</span><span class="sxs-lookup"><span data-stu-id="8827b-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8827b-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="8827b-173">Remarks</span></span>

<span data-ttu-id="8827b-174">Il processo di backup esterno, come avviato da **JetBeginExternalBackup**, è progettato per consentire a un dispositivo di destinazione un backup di transazione fuzzy dell'intera istanza in un dispositivo di destinazione come flusso.</span><span class="sxs-lookup"><span data-stu-id="8827b-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="8827b-175">Il backup conterrà tutti i file di database collegati all'istanza di utilizzando [JetAttachDatabase](./jetattachdatabase-function.md) (per un backup completo), seguiti dai file di patch del database associati (se supportati) e infine dai file di log delle transazioni generati durante il processo di backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="8827b-176">Il risultato finale sarà un set di file che possono essere ripristinati dal flusso, possibilmente combinati con i file di database e di log esistenti e infine ripristinati in uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="8827b-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="8827b-177">L'ordine generale delle operazioni per un backup completo è costituito dalle chiamate seguenti.</span><span class="sxs-lookup"><span data-stu-id="8827b-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="8827b-178">In primo luogo, **JetBeginExternalBackup** viene chiamato per avviare il processo di backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="8827b-179">Viene quindi chiamato [JetGetAttachInfo](./jetgetattachinfo-function.md) per ottenere l'elenco di database collegati all'istanza di di cui è necessario eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="8827b-180">Per ognuno di questi database, viene chiamato [JetOpenFile](./jetopenfile-function.md) , seguito da una serie di chiamate [JetReadFile](./jetreadfile-function.md) e quindi da una chiamata a [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="8827b-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="8827b-181">Viene quindi chiamato [JetGetLogInfo](./jetgetloginfo-function.md) per ottenere un elenco dei file di patch e di log del database di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="8827b-182">Per ognuno di questi file viene effettuata un'altra sequenza di chiamate a [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)e [JetCloseFile](./jetclosefile-function.md) .</span><span class="sxs-lookup"><span data-stu-id="8827b-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="8827b-183">Quindi, eventuali file di log delle transazioni indesiderati vengono eliminati utilizzando [JetTruncateLog](./jettruncatelog-function.md).</span><span class="sxs-lookup"><span data-stu-id="8827b-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="8827b-184">Infine, il backup viene terminato con una chiamata a [JetEndExternalBackup](./jetendexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="8827b-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="8827b-185">È anche possibile modificare questa serie di passaggi per eseguire un backup incrementale dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8827b-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="8827b-186">Un backup incrementale enumera ed esegue il backup dei file di log.</span><span class="sxs-lookup"><span data-stu-id="8827b-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="8827b-187">I backup incrementali sono possibili solo se la registrazione circolare non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="8827b-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="8827b-188">È anche possibile modificare questa serie di passaggi per consentire l'esecuzione di backup differenziali successivi dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8827b-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="8827b-189">Per eseguire un backup differenziale, non chiamare [JetTruncateLog](./jettruncatelog-function.md) nel backup completo o incrementale precedente.</span><span class="sxs-lookup"><span data-stu-id="8827b-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="8827b-190">Se non si chiama [JetTruncateLog](./jettruncatelog-function.md), i backup successivi vengono abilitati come differenziali rispetto all'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="8827b-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="8827b-191">I backup differenziali sono possibili solo se la registrazione circolare non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="8827b-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="8827b-192">Il file di patch del database è un file ausiliario speciale usato per archiviare le immagini della pagina del database in determinate circostanze durante il backup.</span><span class="sxs-lookup"><span data-stu-id="8827b-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="8827b-193">Questo file deve essere presente nella stessa posizione del database associato durante un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8827b-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="8827b-194">Questo file viene usato solo in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8827b-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="8827b-195">Di conseguenza, tutte le applicazioni scritte per funzionare con Windows 2000 e altre versioni devono supportare i file delle patch del database, se sono presenti, ma anche non devono avere esito negativo se non sono presenti.</span><span class="sxs-lookup"><span data-stu-id="8827b-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8827b-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8827b-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8827b-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8827b-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8827b-198">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8827b-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8827b-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8827b-200">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8827b-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-201"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="8827b-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8827b-202">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="8827b-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8827b-203"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="8827b-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8827b-204">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8827b-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8827b-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8827b-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8827b-206">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8827b-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8827b-207">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8827b-207">See Also</span></span>

[<span data-ttu-id="8827b-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8827b-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8827b-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8827b-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8827b-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8827b-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8827b-211">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="8827b-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="8827b-212">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="8827b-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="8827b-213">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="8827b-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="8827b-214">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="8827b-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="8827b-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="8827b-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="8827b-216">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="8827b-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="8827b-217">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="8827b-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="8827b-218">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="8827b-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="8827b-219">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="8827b-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="8827b-220">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="8827b-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="8827b-221">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="8827b-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
