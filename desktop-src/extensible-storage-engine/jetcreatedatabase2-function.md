---
description: 'Altre informazioni su: funzione JetCreateDatabase2'
title: Funzione JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316455"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="b19fc-103">Funzione JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="b19fc-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="b19fc-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b19fc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="b19fc-105">Funzione JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="b19fc-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="b19fc-106">La funzione **JetCreateDatabase2** crea e associa un file di database da utilizzare con il motore di database ESE con le dimensioni massime del database specificate.</span><span class="sxs-lookup"><span data-stu-id="b19fc-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="b19fc-107">La chiamata di **JetCreateDatabase2** con *cpgDatabaseSizeMax* impostato su zero è identica alla chiamata a [JETCREATEDATABASE](./jetcreatedatabase-function.md) con *szConnect* impostato su null.</span><span class="sxs-lookup"><span data-stu-id="b19fc-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="b19fc-108">Attualmente è possibile creare fino a sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="b19fc-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b19fc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b19fc-109">Parameters</span></span>

<span data-ttu-id="b19fc-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b19fc-110">*sesid*</span></span>

<span data-ttu-id="b19fc-111">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="b19fc-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="b19fc-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="b19fc-112">*szFilename*</span></span>

<span data-ttu-id="b19fc-113">Nome del database da creare.</span><span class="sxs-lookup"><span data-stu-id="b19fc-113">The name of the database to be created.</span></span>

<span data-ttu-id="b19fc-114">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="b19fc-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="b19fc-115">Dimensione massima delle pagine del database per il database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="b19fc-116">Le dimensioni predefinite della pagina del database sono di 4 kilobyte e possono essere modificate con [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima della creazione di un database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="b19fc-117">Il passaggio di zero indica che non viene applicato alcun valore massimo dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="b19fc-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="b19fc-118">*pdbid*</span></span>

<span data-ttu-id="b19fc-119">Puntatore a un buffer che, in una chiamata con esito positivo, contiene l'identificatore del database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="b19fc-120">In caso di errore, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="b19fc-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="b19fc-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b19fc-121">*grbit*</span></span>

<span data-ttu-id="b19fc-122">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b19fc-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b19fc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b19fc-123">Value</span></span></p></th>
<th><p><span data-ttu-id="b19fc-124">Significato</span><span class="sxs-lookup"><span data-stu-id="b19fc-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="b19fc-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="b19fc-126">Per impostazione predefinita, se viene chiamato <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> o <strong>JetCreateDatabase2</strong> e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="b19fc-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="b19fc-127">JET_bitDbOverwriteExisting modifica questo comportamento e il database precedente verrà sovrascritto con uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="b19fc-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="b19fc-128">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b19fc-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="b19fc-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="b19fc-130">JET_bitDbRecoveryOff disattiva la registrazione.</span><span class="sxs-lookup"><span data-stu-id="b19fc-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="b19fc-131">L'impostazione di questo bit perde la possibilità di riprodurre i file di log e di ripristinare il database in uno stato utilizzabile coerente dopo un evento irreversibile.</span><span class="sxs-lookup"><span data-stu-id="b19fc-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="b19fc-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="b19fc-133">Impostando JET_bitDbShadowingOff si disabilita la duplicazione di alcune strutture di database interne (ombreggiatura).</span><span class="sxs-lookup"><span data-stu-id="b19fc-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="b19fc-134">La duplicazione di queste strutture viene eseguita per la resilienza, quindi l'impostazione JET_bitDbShadowingOff rimuoverà tale resilienza.</span><span class="sxs-lookup"><span data-stu-id="b19fc-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b19fc-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b19fc-135">Return Value</span></span>

<span data-ttu-id="b19fc-136">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b19fc-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b19fc-137">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b19fc-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b19fc-138">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b19fc-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="b19fc-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b19fc-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b19fc-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b19fc-141">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b19fc-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="b19fc-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b19fc-143">Il database specificato in <em>szFileName</em> esiste già.</span><span class="sxs-lookup"><span data-stu-id="b19fc-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="b19fc-144">Quando viene restituito questo errore, il database non viene collegato.</span><span class="sxs-lookup"><span data-stu-id="b19fc-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="b19fc-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="b19fc-146">Può essere restituito se è stato richiesto l'accesso esclusivo, ma non è stato possibile concederlo o se un'altra sessione ha già aperto il database in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="b19fc-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="b19fc-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="b19fc-148">Restituito quando <em>cpgDatabaseSizeMax</em> è maggiore del numero massimo di pagine consentite in un database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="b19fc-149">Il valore massimo corrente è 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="b19fc-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b19fc-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b19fc-151">È stato specificato un percorso non valido in <em>szFileName</em>.</span><span class="sxs-lookup"><span data-stu-id="b19fc-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="b19fc-152"><em>szFileName</em> deve essere non null.</span><span class="sxs-lookup"><span data-stu-id="b19fc-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="b19fc-153">Per impostazione predefinita, <em>szFileName</em> deve puntare a una directory esistente.</span><span class="sxs-lookup"><span data-stu-id="b19fc-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="b19fc-154">Il percorso verrà creato se <em>JET_paramCreatePathIfNotExist</em> è impostato (vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="b19fc-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="b19fc-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="b19fc-156">Indica che un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="b19fc-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="b19fc-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="b19fc-158">Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="b19fc-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b19fc-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b19fc-160">Il file di database è già stato allegato da un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="b19fc-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="b19fc-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b19fc-162">È stato effettuato un tentativo di creazione di un database in una transazione.</span><span class="sxs-lookup"><span data-stu-id="b19fc-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="b19fc-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="b19fc-164">È stato effettuato un tentativo di aprire un file che non è un file di database valido.</span><span class="sxs-lookup"><span data-stu-id="b19fc-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="b19fc-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="b19fc-166">È stato effettuato un tentativo di aprire più di un database e JET_paramOneDatabasePerSession è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="b19fc-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="b19fc-167">Vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="b19fc-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b19fc-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b19fc-169">Le risorse del sistema sono esaurite.</span><span class="sxs-lookup"><span data-stu-id="b19fc-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="b19fc-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="b19fc-171">Per ogni istanza è possibile collegare solo un numero finito di database.</span><span class="sxs-lookup"><span data-stu-id="b19fc-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="b19fc-172">Il limite è attualmente di sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="b19fc-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="b19fc-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="b19fc-174">Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="b19fc-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="b19fc-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b19fc-176">JET_wrnFileOpenReadOnly indica che il file è stato associato in sola lettura, ma <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> non ha superato JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b19fc-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="b19fc-177">Il database viene ancora aperto con accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b19fc-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b19fc-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="b19fc-178">Remarks</span></span>

<span data-ttu-id="b19fc-179">Se il database specificato in *szFileName* esiste e JET_bitDbOverwriteExisting non è stato passato, la chiamata API avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b19fc-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="b19fc-180">Se JET_bitDbOverwriteExisting è stato passato, il file di database precedente verrà eliminato per primo.</span><span class="sxs-lookup"><span data-stu-id="b19fc-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="b19fc-181">Se l'API crea un file di database e quindi raggiunge un altro errore, il file verrà eliminato ed eliminato.</span><span class="sxs-lookup"><span data-stu-id="b19fc-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="b19fc-182">Il database viene aperto in modo implicito da **JetCreateDatabase2** .</span><span class="sxs-lookup"><span data-stu-id="b19fc-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="b19fc-183">Non è necessario chiamare in seguito [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b19fc-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b19fc-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b19fc-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-186">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b19fc-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-188">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b19fc-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-189"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-190">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b19fc-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-191"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-192">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b19fc-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b19fc-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-194">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b19fc-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b19fc-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b19fc-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b19fc-196">Implementato come <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b19fc-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b19fc-197">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b19fc-197">See Also</span></span>

[<span data-ttu-id="b19fc-198">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="b19fc-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b19fc-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b19fc-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b19fc-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b19fc-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="b19fc-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b19fc-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b19fc-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b19fc-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b19fc-203">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b19fc-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b19fc-204">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="b19fc-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="b19fc-205">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="b19fc-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="b19fc-206">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="b19fc-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="b19fc-207">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b19fc-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b19fc-208">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="b19fc-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
