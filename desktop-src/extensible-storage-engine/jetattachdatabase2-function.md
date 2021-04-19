---
description: 'Altre informazioni su: funzione JetAttachDatabase2'
title: Funzione JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318103"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="66087-103">Funzione JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="66087-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="66087-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="66087-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="66087-105">Funzione JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="66087-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="66087-106">La funzione **JetAttachDatabase2** connette un file di database per l'utilizzo con un'istanza di database e specifica le dimensioni massime del database.</span><span class="sxs-lookup"><span data-stu-id="66087-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="66087-107">Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="66087-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="66087-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66087-108">Parameters</span></span>

<span data-ttu-id="66087-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="66087-109">*sesid*</span></span>

<span data-ttu-id="66087-110">Contesto della sessione del database che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="66087-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="66087-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="66087-111">*szFilename*</span></span>

<span data-ttu-id="66087-112">Nome del database da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="66087-112">The name of the database to attach.</span></span>

<span data-ttu-id="66087-113">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="66087-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="66087-114">Dimensione massima delle pagine del database per il database.</span><span class="sxs-lookup"><span data-stu-id="66087-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="66087-115">Le dimensioni predefinite della pagina del database sono di 4 kilobyte, che possono essere modificate utilizzando la funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima di creare un database.</span><span class="sxs-lookup"><span data-stu-id="66087-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="66087-116">Il passaggio di zero indica che non viene applicato alcun valore massimo dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="66087-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="66087-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="66087-117">*grbit*</span></span>

<span data-ttu-id="66087-118">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66087-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66087-119">Valore</span><span class="sxs-lookup"><span data-stu-id="66087-119">Value</span></span></p></th>
<th><p><span data-ttu-id="66087-120">Significato</span><span class="sxs-lookup"><span data-stu-id="66087-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66087-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="66087-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="66087-122">Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, verranno eliminati tutti gli indici sui dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="66087-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="66087-123">Per altre informazioni, vedere le sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66087-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="66087-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="66087-125">Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione di <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="66087-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="66087-126">Per altre informazioni, vedere le sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66087-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="66087-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="66087-128">Impedisce le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="66087-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="66087-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="66087-130">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="66087-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="66087-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66087-131">Return Value</span></span>

<span data-ttu-id="66087-132">La funzione restituisce uno dei codici di errore [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="66087-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="66087-133">Di seguito sono riportati i più comunemente restituiti.</span><span class="sxs-lookup"><span data-stu-id="66087-133">The following are the most commonly returned.</span></span> <span data-ttu-id="66087-134">Per un elenco completo degli errori per questa API, vedere [codici di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="66087-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66087-135">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66087-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="66087-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66087-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66087-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="66087-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="66087-138">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="66087-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="66087-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="66087-140">Il connessione di un database non è consentita durante un backup.</span><span class="sxs-lookup"><span data-stu-id="66087-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="66087-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="66087-142">Il file di database specificato da <em>szFileName</em> deve essere scrivibile.</span><span class="sxs-lookup"><span data-stu-id="66087-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="66087-143">Non è necessario impostare l'attributo Read-Only e il processo in esecuzione deve disporre di privilegi sufficienti per la scrittura nel file.</span><span class="sxs-lookup"><span data-stu-id="66087-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="66087-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="66087-145">Il file di database è già aperto da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="66087-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="66087-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="66087-147">È stato specificato un percorso non valido in <em>szFileName</em>.</span><span class="sxs-lookup"><span data-stu-id="66087-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="66087-148"><em>szFileName</em> deve essere non null e fare riferimento a un percorso valido.</span><span class="sxs-lookup"><span data-stu-id="66087-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="66087-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="66087-150">Il file di database è già stato allegato da un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="66087-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="66087-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="66087-152">Il file specificato in <em>szFileName</em> non esiste.</span><span class="sxs-lookup"><span data-stu-id="66087-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="66087-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="66087-154">Si è verificato un errore con l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="66087-154">There is an error with the primary index.</span></span> <span data-ttu-id="66087-155">Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria.</span><span class="sxs-lookup"><span data-stu-id="66087-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="66087-156">Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="66087-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="66087-157">Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66087-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="66087-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="66087-159">Si è verificato un errore con un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="66087-159">There is an error with a secondary index.</span></span> <span data-ttu-id="66087-160">Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria.</span><span class="sxs-lookup"><span data-stu-id="66087-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="66087-161">Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="66087-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="66087-162">Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66087-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="66087-163">Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando seguente: <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="66087-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="66087-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="66087-165">Per ogni istanza è possibile collegare solo un numero finito di database.</span><span class="sxs-lookup"><span data-stu-id="66087-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="66087-166">Il limite è attualmente di sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="66087-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="66087-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="66087-168">Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="66087-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="66087-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="66087-169">Remarks</span></span>

<span data-ttu-id="66087-170">Il file di database viene scollegato tramite [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="66087-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="66087-171">Vedere [JetAttachDatabase](./jetattachdatabase-function.md) per le note.</span><span class="sxs-lookup"><span data-stu-id="66087-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="66087-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66087-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66087-173"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="66087-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-174">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="66087-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-175"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="66087-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-176">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="66087-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-177"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="66087-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-178">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="66087-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-179"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="66087-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-180">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="66087-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66087-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="66087-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-182">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="66087-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66087-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="66087-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="66087-184">Implementato come <strong>JetAttachDatabase2W</strong> (Unicode) e <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="66087-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="66087-185">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="66087-185">See Also</span></span>

[<span data-ttu-id="66087-186">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="66087-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="66087-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="66087-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="66087-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="66087-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="66087-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="66087-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="66087-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="66087-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="66087-191">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="66087-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="66087-192">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="66087-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="66087-193">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="66087-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="66087-194">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="66087-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
