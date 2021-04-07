---
description: 'Altre informazioni su: funzione JetOpenDatabase'
title: Funzione JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760538"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="3a54d-103">Funzione JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="3a54d-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="3a54d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3a54d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="3a54d-105">Funzione JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="3a54d-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="3a54d-106">La funzione **JetOpenDatabase** apre un database precedentemente collegato, usando le funzioni [JetAttachDatabase](./jetattachdatabase-function.md) o [JetAttachDatabase2](./jetattachdatabase2-function.md) , da usare con una sessione di database.</span><span class="sxs-lookup"><span data-stu-id="3a54d-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="3a54d-107">Questa funzione può essere chiamata più volte per lo stesso database.</span><span class="sxs-lookup"><span data-stu-id="3a54d-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3a54d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a54d-108">Parameters</span></span>

<span data-ttu-id="3a54d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3a54d-109">*sesid*</span></span>

<span data-ttu-id="3a54d-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="3a54d-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="3a54d-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="3a54d-111">*szFilename*</span></span>

<span data-ttu-id="3a54d-112">Nome del database da aprire.</span><span class="sxs-lookup"><span data-stu-id="3a54d-112">The name of the database to open.</span></span>

<span data-ttu-id="3a54d-113">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="3a54d-113">*szConnect*</span></span>

<span data-ttu-id="3a54d-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3a54d-114">Reserved.</span></span> <span data-ttu-id="3a54d-115">Impostata su NULL.</span><span class="sxs-lookup"><span data-stu-id="3a54d-115">Set to NULL.</span></span>

<span data-ttu-id="3a54d-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="3a54d-116">*pdbid*</span></span>

<span data-ttu-id="3a54d-117">Puntatore a un buffer che, in una chiamata con esito positivo, contiene l'identificatore del database.</span><span class="sxs-lookup"><span data-stu-id="3a54d-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="3a54d-118">Se la chiamata ha esito negativo, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="3a54d-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="3a54d-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3a54d-119">*grbit*</span></span>

<span data-ttu-id="3a54d-120">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a54d-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a54d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3a54d-121">Value</span></span></p></th>
<th><p><span data-ttu-id="3a54d-122">Significato</span><span class="sxs-lookup"><span data-stu-id="3a54d-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="3a54d-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="3a54d-124">Consente la connessione di un database a una singola sessione.</span><span class="sxs-lookup"><span data-stu-id="3a54d-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="3a54d-125">In genere, diverse sessioni possono aprire un database.</span><span class="sxs-lookup"><span data-stu-id="3a54d-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="3a54d-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3a54d-127">Impedisce le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="3a54d-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3a54d-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a54d-128">Return Value</span></span>

<span data-ttu-id="3a54d-129">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3a54d-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3a54d-130">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3a54d-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a54d-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3a54d-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="3a54d-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a54d-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3a54d-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3a54d-134">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3a54d-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="3a54d-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="3a54d-136">L'accesso esclusivo è stato richiesto, ma non è stato possibile concederlo.</span><span class="sxs-lookup"><span data-stu-id="3a54d-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="3a54d-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="3a54d-138">È stato specificato un percorso non valido in <em>szFileName</em>.</span><span class="sxs-lookup"><span data-stu-id="3a54d-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="3a54d-139"><em>szFileName</em> deve essere diverso da null e fare riferimento a un file valido.</span><span class="sxs-lookup"><span data-stu-id="3a54d-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="3a54d-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="3a54d-141">Un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="3a54d-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="3a54d-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="3a54d-143">Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="3a54d-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="3a54d-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="3a54d-145">È stato effettuato un tentativo di aprire un file che non è un file di database valido.</span><span class="sxs-lookup"><span data-stu-id="3a54d-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="3a54d-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="3a54d-147">È stato effettuato un tentativo di aprire più di un database e <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="3a54d-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="3a54d-148">Per ulteriori informazioni, vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="3a54d-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="3a54d-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3a54d-150">Il file è stato collegato come di sola lettura, ma <strong>JetOpenDatabase</strong> non ha superato JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="3a54d-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="3a54d-151">Il database viene ancora aperto con accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3a54d-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="3a54d-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a54d-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-154">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3a54d-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-156">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3a54d-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3a54d-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-159"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-160">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3a54d-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a54d-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-162">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3a54d-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a54d-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3a54d-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3a54d-164">Implementato come <strong>JetOpenDatabaseW</strong> (Unicode) e <strong>JetOpenDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3a54d-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3a54d-165">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3a54d-165">See Also</span></span>

[<span data-ttu-id="3a54d-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3a54d-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3a54d-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3a54d-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3a54d-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3a54d-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3a54d-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3a54d-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3a54d-170">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="3a54d-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="3a54d-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="3a54d-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="3a54d-172">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3a54d-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3a54d-173">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="3a54d-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
