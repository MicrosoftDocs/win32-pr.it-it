---
description: 'Altre informazioni su: funzione JetSetDatabaseSize'
title: JetSetDatabaseSize (funzione)
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128151"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="fbbaf-103">JetSetDatabaseSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbbaf-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="fbbaf-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fbbaf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="fbbaf-105">JetSetDatabaseSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbbaf-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="fbbaf-106">La funzione **JetSetDatabaseSize** imposta la dimensione di un file di database non aperto.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="fbbaf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbbaf-107">Parameters</span></span>

<span data-ttu-id="fbbaf-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fbbaf-108">*sesid*</span></span>

<span data-ttu-id="fbbaf-109">Identifica il contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="fbbaf-110">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="fbbaf-110">*szDatabaseName*</span></span>

<span data-ttu-id="fbbaf-111">Identifica il nome del file di database la cui dimensione deve essere modificata.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="fbbaf-112">*cpg*</span><span class="sxs-lookup"><span data-stu-id="fbbaf-112">*cpg*</span></span>

<span data-ttu-id="fbbaf-113">Specifica le dimensioni desiderate del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="fbbaf-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="fbbaf-114">*pcpgReal*</span></span>

<span data-ttu-id="fbbaf-115">Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="fbbaf-116">Se la chiamata API ha avuto esito negativo, il contenuto di *pcpgReal* non è definito.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="fbbaf-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbbaf-117">Return Value</span></span>

<span data-ttu-id="fbbaf-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fbbaf-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="fbbaf-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbbaf-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fbbaf-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="fbbaf-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbaf-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fbbaf-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="fbbaf-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="fbbaf-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="fbbaf-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-126">JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown sono lo stesso valore numerico.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="fbbaf-127">Il database la cui dimensione deve essere regolata deve essere in uno stato di chiusura normale, noto come stato coerente.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="fbbaf-128">Un database incoerente non è danneggiato, ma richiede la riproduzione dei file di log.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="fbbaf-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-130"><em>szDatabaseName</em> non deve essere una stringa vuota e non null.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="fbbaf-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-132">Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di espansione.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="fbbaf-133"><strong>JetSetDatabaseSize</strong> può inoltre restituire molti errori correlati ai file, tra cui:</span><span class="sxs-lookup"><span data-stu-id="fbbaf-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="fbbaf-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="fbbaf-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="fbbaf-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="fbbaf-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="fbbaf-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="fbbaf-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="fbbaf-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="fbbaf-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="fbbaf-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="fbbaf-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fbbaf-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-140">Uno dei motivi per cui questo errore può essere restituito è se <em>CPG</em> soddisfa le dimensioni minime del database.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="fbbaf-141">Le dimensioni minime correnti del database sono di 256 pagine.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="fbbaf-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="fbbaf-143">Risorse di memoria insufficienti per il sistema.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="fbbaf-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbbaf-144">Remarks</span></span>

<span data-ttu-id="fbbaf-145">Se **JetSetDatabaseSize** viene chiamato prima dell'inserimento di grandi quantità di dati, il file di database verrà aumentato in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="fbbaf-146">In questo modo si ridurrà la probabilità che il file di database diventi frammentato a livello di file system e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="fbbaf-147">La crescita del file di database può essere più veloce rispetto alla crescita più volte.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="fbbaf-148">Attualmente è supportata solo la crescita del file.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="fbbaf-149">Per compattare un file, utilizzare la funzionalità di deframmentazione del programma di utilità esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="fbbaf-150">Se *CPG* è inferiore alla dimensione corrente del database, l'operazione verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="fbbaf-151">Se *CPG* è inferiore alle dimensioni minime del database (attualmente 256 pagine), verrà restituito JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="fbbaf-152">Per impostare le dimensioni di un database aperto, vedere [JetGrowDatabase](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbbaf-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="fbbaf-153">Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite in *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="fbbaf-154">Sono disponibili altre due pagine riservate che non possono essere conteggiate in *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fbbaf-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbbaf-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-157">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-159">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-160"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-161">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-162"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-163">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbbaf-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-165">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fbbaf-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbaf-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fbbaf-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fbbaf-167">Implementato come <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fbbaf-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fbbaf-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fbbaf-168">See Also</span></span>

[<span data-ttu-id="fbbaf-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fbbaf-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fbbaf-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fbbaf-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fbbaf-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fbbaf-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fbbaf-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fbbaf-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fbbaf-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fbbaf-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="fbbaf-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="fbbaf-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="fbbaf-175">JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="fbbaf-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
