---
description: 'Altre informazioni su: funzione JetAttachDatabase'
title: Funzione JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225879"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="1f568-103">Funzione JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="1f568-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="1f568-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1f568-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="1f568-105">Funzione JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="1f568-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="1f568-106">La funzione **JetAttachDatabase** connette un file di database per l'utilizzo con un'istanza di database.</span><span class="sxs-lookup"><span data-stu-id="1f568-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="1f568-107">Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f568-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1f568-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f568-108">Parameters</span></span>

<span data-ttu-id="1f568-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1f568-109">*sesid*</span></span>

<span data-ttu-id="1f568-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="1f568-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="1f568-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="1f568-111">*szFilename*</span></span>

<span data-ttu-id="1f568-112">Nome del database da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1f568-112">The name of the database to attach.</span></span>

<span data-ttu-id="1f568-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1f568-113">*grbit*</span></span>

<span data-ttu-id="1f568-114">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f568-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f568-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1f568-115">Value</span></span></p></th>
<th><p><span data-ttu-id="1f568-116">Significato</span><span class="sxs-lookup"><span data-stu-id="1f568-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f568-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="1f568-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="1f568-118">Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, verranno eliminati tutti gli indici sui dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f568-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="1f568-119">Per altre informazioni, vedere le sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1f568-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="1f568-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="1f568-121">Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione di <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="1f568-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="1f568-122">Per altre informazioni, vedere le sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1f568-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="1f568-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="1f568-124">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="1f568-124">Obsolete.</span></span> <span data-ttu-id="1f568-125">Non usare.</span><span class="sxs-lookup"><span data-stu-id="1f568-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f568-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1f568-127">Impedisce le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="1f568-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1f568-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f568-128">Return Value</span></span>

<span data-ttu-id="1f568-129">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="1f568-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1f568-130">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1f568-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f568-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1f568-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="1f568-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f568-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f568-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1f568-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1f568-134">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1f568-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="1f568-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="1f568-136">Il connessione di un database non è consentita durante un backup.</span><span class="sxs-lookup"><span data-stu-id="1f568-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f568-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1f568-138">Il file di database specificato da <em>szFileName</em> deve essere scrivibile.</span><span class="sxs-lookup"><span data-stu-id="1f568-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="1f568-139">Non è necessario impostare l'attributo Read-Only e il processo in esecuzione deve disporre di privilegi sufficienti per la scrittura nel file.</span><span class="sxs-lookup"><span data-stu-id="1f568-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="1f568-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="1f568-141">Il file di database è già aperto da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="1f568-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1f568-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1f568-143">È stato specificato un percorso non valido in <em>szFileName</em>.</span><span class="sxs-lookup"><span data-stu-id="1f568-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="1f568-144"><em>szFileName</em> deve essere non null e fare riferimento a un percorso valido.</span><span class="sxs-lookup"><span data-stu-id="1f568-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1f568-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1f568-146">Il file di database è già stato allegato da un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="1f568-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="1f568-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="1f568-148">Il motore di database non è in grado di aprire il file di database.</span><span class="sxs-lookup"><span data-stu-id="1f568-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="1f568-149">Il file potrebbe essere in uso da un altro processo oppure il chiamante potrebbe non disporre di privilegi sufficienti per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="1f568-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="1f568-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="1f568-151">Il file specificato in <em>szFileName</em> non esiste.</span><span class="sxs-lookup"><span data-stu-id="1f568-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="1f568-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="1f568-153">Si è verificato un errore con l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="1f568-153">There is an error with the primary index.</span></span> <span data-ttu-id="1f568-154">Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria.</span><span class="sxs-lookup"><span data-stu-id="1f568-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="1f568-155">Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f568-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="1f568-156">Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1f568-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="1f568-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="1f568-158">Si è verificato un errore con un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="1f568-158">There is an error with a secondary index.</span></span> <span data-ttu-id="1f568-159">Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria.</span><span class="sxs-lookup"><span data-stu-id="1f568-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="1f568-160">Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f568-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="1f568-161">Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1f568-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="1f568-162">Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando seguente: <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f568-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="1f568-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="1f568-164">Per ogni istanza è possibile collegare solo un numero finito di database.</span><span class="sxs-lookup"><span data-stu-id="1f568-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="1f568-165">Il limite è attualmente di sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="1f568-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="1f568-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="1f568-167">Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="1f568-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1f568-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f568-168">Remarks</span></span>

<span data-ttu-id="1f568-169">La chiamata a **JetAttachDatabase** equivale alla chiamata a [JetAttachDatabase2](./jetattachdatabase2-function.md) e al passaggio di un valore pari a zero, ovvero non esiste alcun limite per il parametro *cpgDatabaseSizeMax* .</span><span class="sxs-lookup"><span data-stu-id="1f568-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="1f568-170">Se si connette un database scrivibile, ovvero se JET_bitDbReadOnly non è stato specificato nel parametro *grbit* , il file verrà aperto esclusivamente a livello di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1f568-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="1f568-171">Nessun altro processo sarà in grado di aprire il file.</span><span class="sxs-lookup"><span data-stu-id="1f568-171">No other process will be able open the file.</span></span> <span data-ttu-id="1f568-172">È possibile che più processi alleghino un singolo database aprendoli in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1f568-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="1f568-173">Il file di database viene scollegato tramite [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f568-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="1f568-174">Parametri di controllo degli indici</span><span class="sxs-lookup"><span data-stu-id="1f568-174">Index-checking parameters</span></span>

<span data-ttu-id="1f568-175">Diverse versioni di Windows normalizzano il testo Unicode in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="1f568-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="1f568-176">Ciò significa che gli indici compilati in una versione di Windows potrebbero non funzionare in altre versioni.</span><span class="sxs-lookup"><span data-stu-id="1f568-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="1f568-177">Prima di Windows Server 2003, quando la versione del sistema operativo è cambiata (inclusa l'installazione di un Service Pack), ogni indice sui dati Unicode si trovava in uno stato potenzialmente danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1f568-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="1f568-178">Gli indici creati in Windows Server 2003 e versioni successive vengono contrassegnati con la versione di normalizzazione Unicode con cui sono stati compilati.</span><span class="sxs-lookup"><span data-stu-id="1f568-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="1f568-179">Gli indici meno recenti non contengono informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="1f568-179">Older indexes contain no version information.</span></span> <span data-ttu-id="1f568-180">La maggior parte delle modifiche di normalizzazione Unicode è costituita dall'aggiunta di nuovi caratteri, i punti di codice precedentemente non definiti sono ora definiti e normalizzati in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="1f568-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="1f568-181">Pertanto, se i dati binari vengono archiviati in una colonna Unicode, verranno normalizzati in modo diverso Man seconda che vengono definiti nuovi punti di codice.</span><span class="sxs-lookup"><span data-stu-id="1f568-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="1f568-182">A partire da Windows Server 2003, il motore di database ESE tiene traccia delle voci di indice Unicode contenenti punti di codice non definiti.</span><span class="sxs-lookup"><span data-stu-id="1f568-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="1f568-183">Questi possono essere usati per correggere un indice quando viene modificato il set di caratteri Unicode definiti.</span><span class="sxs-lookup"><span data-stu-id="1f568-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="1f568-184">Questi parametri controllano cosa accade quando il motore di database ESE si connette a un database usato per l'ultima volta in una build diversa del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1f568-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="1f568-185">La versione del sistema operativo è contrassegnata nell'intestazione del database.</span><span class="sxs-lookup"><span data-stu-id="1f568-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="1f568-186">Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **true** e il database contiene indici potenzialmente danneggiati:</span><span class="sxs-lookup"><span data-stu-id="1f568-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="1f568-187">**JetAttachDatabase** eliminerà gli indici potenzialmente danneggiati se *grbit* contiene JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="1f568-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="1f568-188">**JetAttachDatabase** restituirà un errore se *grbit* non contiene JET_bitDbDeleteCorruptIndexes e sono presenti indici che necessitano dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="1f568-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="1f568-189">Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **false**:</span><span class="sxs-lookup"><span data-stu-id="1f568-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="1f568-190">**JetAttachDatabase** ignorerà gli indici potenzialmente danneggiati e restituirà JET_errSuccess (presupponendo che non siano presenti altri errori).</span><span class="sxs-lookup"><span data-stu-id="1f568-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="1f568-191">Windows Server 2003 e versioni successive: se [JET_paramEnableIndexChecking](./database-parameters.md) non è stato reimpostato, la tabella di correzione interna verrà utilizzata per la correzione delle voci di indice.</span><span class="sxs-lookup"><span data-stu-id="1f568-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="1f568-192">Questa operazione potrebbe non correggere tutti i danneggiamenti dell'indice ma sarà trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1f568-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="1f568-193">Se il database è stato collegato come di sola lettura, non è possibile correggere o eliminare l'indice.</span><span class="sxs-lookup"><span data-stu-id="1f568-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="1f568-194">In questo caso, l'API restituirà invece un errore, ad esempio JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="1f568-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1f568-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f568-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f568-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-197">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1f568-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-199">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1f568-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-200"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-201">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1f568-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-202"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-203">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1f568-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f568-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-205">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1f568-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f568-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1f568-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1f568-207">Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1f568-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1f568-208">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1f568-208">See Also</span></span>

[<span data-ttu-id="1f568-209">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1f568-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="1f568-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1f568-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1f568-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1f568-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1f568-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1f568-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1f568-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1f568-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1f568-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="1f568-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="1f568-215">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="1f568-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="1f568-216">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="1f568-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="1f568-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="1f568-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="1f568-218">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="1f568-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="1f568-219">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="1f568-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
