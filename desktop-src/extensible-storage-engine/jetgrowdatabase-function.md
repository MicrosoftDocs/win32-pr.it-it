---
description: 'Altre informazioni su: funzione JetGrowDatabase'
title: JetGrowDatabase (funzione)
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313097"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="2fd25-103">JetGrowDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="2fd25-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="2fd25-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2fd25-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="2fd25-105">JetGrowDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="2fd25-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="2fd25-106">La funzione **JetGrowDatabase** estende le dimensioni di un database attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="2fd25-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="2fd25-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fd25-107">Parameters</span></span>

<span data-ttu-id="2fd25-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2fd25-108">*sesid*</span></span>

<span data-ttu-id="2fd25-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="2fd25-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="2fd25-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="2fd25-110">*dbid*</span></span>

<span data-ttu-id="2fd25-111">Database che verrà esteso.</span><span class="sxs-lookup"><span data-stu-id="2fd25-111">The database that will be extended.</span></span>

<span data-ttu-id="2fd25-112">*cpg*</span><span class="sxs-lookup"><span data-stu-id="2fd25-112">*cpg*</span></span>

<span data-ttu-id="2fd25-113">Dimensioni desiderate del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="2fd25-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="2fd25-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="2fd25-114">*pcpgReal*</span></span>

<span data-ttu-id="2fd25-115">Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="2fd25-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="2fd25-116">Se la chiamata API ha esito negativo, il contenuto di *pcpgReal* non è definito.</span><span class="sxs-lookup"><span data-stu-id="2fd25-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="2fd25-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fd25-117">Return Value</span></span>

<span data-ttu-id="2fd25-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="2fd25-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2fd25-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd25-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fd25-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2fd25-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="2fd25-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fd25-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fd25-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2fd25-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2fd25-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2fd25-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd25-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="2fd25-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="2fd25-125">Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di espansione.</span><span class="sxs-lookup"><span data-stu-id="2fd25-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fd25-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="2fd25-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="2fd25-127">Un errore relativo al file è stato restituito da <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="2fd25-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="2fd25-128">Per ulteriori informazioni sugli altri errori correlati ai file che potrebbero essere restituiti, vedere <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="2fd25-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="2fd25-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fd25-129">Remarks</span></span>

<span data-ttu-id="2fd25-130">Se **JetGrowDatabase** viene chiamato prima dell'inserimento di grandi quantità di dati, il file di database verrà aumentato in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="2fd25-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="2fd25-131">In questo modo si ridurrà la probabilità che il file di database diventi frammentato a livello di file system e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato.</span><span class="sxs-lookup"><span data-stu-id="2fd25-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="2fd25-132">La crescita del file di database può essere più veloce rispetto alla crescita più volte.</span><span class="sxs-lookup"><span data-stu-id="2fd25-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="2fd25-133">Attualmente è supportata solo la crescita del file.</span><span class="sxs-lookup"><span data-stu-id="2fd25-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="2fd25-134">Per compattare un file, utilizzare la funzionalità di deframmentazione del programma di utilità **esentutl.exe** .</span><span class="sxs-lookup"><span data-stu-id="2fd25-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="2fd25-135">Per impostare le dimensioni di un database non aperto, vedere [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="2fd25-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="2fd25-136">Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite in *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="2fd25-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="2fd25-137">Sono disponibili altre due pagine riservate che potrebbero non essere conteggiate in *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="2fd25-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2fd25-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fd25-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fd25-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2fd25-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2fd25-140">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2fd25-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd25-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2fd25-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2fd25-142">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2fd25-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fd25-143"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2fd25-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2fd25-144">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2fd25-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd25-145"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2fd25-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2fd25-146">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2fd25-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fd25-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2fd25-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2fd25-148">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2fd25-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2fd25-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2fd25-149">See Also</span></span>

[<span data-ttu-id="2fd25-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2fd25-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2fd25-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2fd25-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2fd25-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2fd25-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2fd25-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2fd25-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2fd25-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="2fd25-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="2fd25-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="2fd25-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="2fd25-156">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="2fd25-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
