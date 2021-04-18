---
description: 'Altre informazioni su: funzione JetCreateDatabase'
title: Funzione JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313105"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="20624-103">Funzione JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="20624-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20624-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="20624-105">Funzione JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="20624-106">La funzione **JetCreateDatabase** crea e associa un file di database da utilizzare con il motore di database ESE.</span><span class="sxs-lookup"><span data-stu-id="20624-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="20624-107">La chiamata di [JetCreateDatabase2](./jetcreatedatabase2-function.md) con *cpgDatabaseSizeMax* impostato su zero è identica alla chiamata a **JETCREATEDATABASE** con *szConnect* impostato su null.</span><span class="sxs-lookup"><span data-stu-id="20624-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="20624-108">Attualmente, è possibile creare fino a sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="20624-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="20624-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="20624-109">Parameters</span></span>

<span data-ttu-id="20624-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="20624-110">*sesid*</span></span>

<span data-ttu-id="20624-111">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="20624-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="20624-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="20624-112">*szFilename*</span></span>

<span data-ttu-id="20624-113">Nome del database da creare.</span><span class="sxs-lookup"><span data-stu-id="20624-113">The name of the database to be created.</span></span>

<span data-ttu-id="20624-114">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="20624-114">*szConnect*</span></span>

<span data-ttu-id="20624-115">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20624-115">Reserved for future use.</span></span> <span data-ttu-id="20624-116">Impostata su NULL.</span><span class="sxs-lookup"><span data-stu-id="20624-116">Set to NULL.</span></span>

<span data-ttu-id="20624-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="20624-117">*pdbid*</span></span>

<span data-ttu-id="20624-118">Puntatore a un buffer che, in una chiamata con esito positivo, contiene l'identificatore del database.</span><span class="sxs-lookup"><span data-stu-id="20624-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="20624-119">In caso di errore, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="20624-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="20624-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="20624-120">*grbit*</span></span>

<span data-ttu-id="20624-121">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="20624-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20624-122">Valore</span><span class="sxs-lookup"><span data-stu-id="20624-122">Value</span></span></p></th>
<th><p><span data-ttu-id="20624-123">Significato</span><span class="sxs-lookup"><span data-stu-id="20624-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20624-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="20624-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="20624-125">Per impostazione predefinita, se viene chiamato <strong>JetCreateDatabase</strong> e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="20624-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="20624-126">JET_bitDbOverwriteExisting modifica questo comportamento e il database precedente verrà sovrascritto con uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="20624-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="20624-127">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="20624-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="20624-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="20624-129">JET_bitDbRecoveryOff disattiva la registrazione.</span><span class="sxs-lookup"><span data-stu-id="20624-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="20624-130">L'impostazione di questo bit perde la possibilità di riprodurre i file di log e di ripristinare il database in uno stato utilizzabile coerente dopo un evento irreversibile.</span><span class="sxs-lookup"><span data-stu-id="20624-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="20624-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="20624-132">Impostando JET_bitDbShadowingOff si disabilita la duplicazione di alcune strutture di database interne (ombreggiatura).</span><span class="sxs-lookup"><span data-stu-id="20624-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="20624-133">La duplicazione di queste strutture viene eseguita per la resilienza, quindi l'impostazione JET_bitDbShadowingOff rimuoverà tale resilienza.</span><span class="sxs-lookup"><span data-stu-id="20624-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20624-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20624-134">Return Value</span></span>

<span data-ttu-id="20624-135">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="20624-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20624-136">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="20624-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20624-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="20624-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="20624-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20624-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20624-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20624-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20624-140">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="20624-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="20624-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="20624-142">Il database specificato in <em>szFileName</em> esiste già.</span><span class="sxs-lookup"><span data-stu-id="20624-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="20624-143">Quando viene restituito questo errore, il database non viene collegato.</span><span class="sxs-lookup"><span data-stu-id="20624-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="20624-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="20624-145">Può essere restituito se è stato richiesto l'accesso esclusivo, ma non è stato possibile concederlo o se un'altra sessione ha già aperto il database in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="20624-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="20624-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="20624-147">Restituito quando <em>cpgDatabaseSizeMax</em> è maggiore del numero massimo di pagine consentite in un database.</span><span class="sxs-lookup"><span data-stu-id="20624-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="20624-148">Il valore massimo corrente è 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="20624-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="20624-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="20624-150">È stato specificato un percorso non valido in <em>szFileName</em>.</span><span class="sxs-lookup"><span data-stu-id="20624-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="20624-151"><em>szFileName</em> deve essere non null.</span><span class="sxs-lookup"><span data-stu-id="20624-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="20624-152">Per impostazione predefinita, <em>szFileName</em> deve puntare a una directory esistente.</span><span class="sxs-lookup"><span data-stu-id="20624-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="20624-153">Il percorso verrà creato se <em>JET_paramCreatePathIfNotExist</em> è impostato (vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="20624-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="20624-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="20624-155">Indica che un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="20624-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="20624-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="20624-157">Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="20624-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="20624-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="20624-159">Il file di database è già stato allegato da un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="20624-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="20624-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="20624-161">È stato effettuato un tentativo di creazione di un database in una transazione.</span><span class="sxs-lookup"><span data-stu-id="20624-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="20624-163">È stato effettuato un tentativo di aprire un file che non è un file di database valido.</span><span class="sxs-lookup"><span data-stu-id="20624-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="20624-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="20624-165">È stato effettuato un tentativo di aprire più di un database e JET_paramOneDatabasePerSession è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="20624-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="20624-166">Vedere <a href="gg269337(v=exchg.10).md">parametri del database</a>.</span><span class="sxs-lookup"><span data-stu-id="20624-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="20624-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="20624-168">L'operazione non è riuscita perché non è stato possibile allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="20624-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="20624-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="20624-170">Per ogni istanza è possibile collegare solo un numero finito di database.</span><span class="sxs-lookup"><span data-stu-id="20624-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="20624-171">Il limite è attualmente di sette database per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="20624-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="20624-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="20624-173">Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="20624-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="20624-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="20624-175">JET_wrnFileOpenReadOnly indica che il file è stato associato in sola lettura, ma <strong>JetCreateDatabase</strong> non ha superato JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="20624-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="20624-176">Il database viene ancora aperto con accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="20624-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="20624-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="20624-177">Remarks</span></span>

<span data-ttu-id="20624-178">Se il database specificato in *szFileName* esiste e JET_bitDbOverwriteExisting non è stato passato, la chiamata API avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="20624-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="20624-179">Se JET_bitDbOverwriteExisting è stato passato, il file di database precedente verrà eliminato per primo.</span><span class="sxs-lookup"><span data-stu-id="20624-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="20624-180">Se l'API crea un file di database e quindi raggiunge un altro errore, il file verrà eliminato ed eliminato.</span><span class="sxs-lookup"><span data-stu-id="20624-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="20624-181">Il database viene aperto in modo implicito da **JetCreateDatabase** .</span><span class="sxs-lookup"><span data-stu-id="20624-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="20624-182">Non è necessario chiamare in seguito [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="20624-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="20624-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20624-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20624-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="20624-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-185">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20624-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="20624-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-187">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20624-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-188"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="20624-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-189">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="20624-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-190"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="20624-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-191">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20624-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20624-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="20624-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-193">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20624-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20624-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="20624-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="20624-195">Implementato come <strong>JetCreateDatabaseW</strong> (Unicode) e <strong>JetCreateDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="20624-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20624-196">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="20624-196">See Also</span></span>

[<span data-ttu-id="20624-197">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="20624-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="20624-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20624-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20624-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="20624-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="20624-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20624-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20624-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20624-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20624-202">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="20624-203">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="20624-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="20624-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="20624-205">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="20624-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="20624-206">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="20624-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="20624-207">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="20624-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
