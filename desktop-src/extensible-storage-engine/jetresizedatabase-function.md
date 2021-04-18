---
description: 'Altre informazioni su: funzione JetResizeDatabase'
title: JetResizeDatabase (funzione)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319175"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="67d09-103">JetResizeDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="67d09-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="67d09-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="67d09-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="67d09-105">La funzione **JetResizeDatabase** estende o compatta le dimensioni di un database attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="67d09-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="67d09-106">La funzione **JetResizeDatabase** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67d09-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="67d09-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67d09-107">Parameters</span></span>

<span data-ttu-id="67d09-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="67d09-108">*sesid*</span></span>

<span data-ttu-id="67d09-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="67d09-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="67d09-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="67d09-110">*dbid*</span></span>

<span data-ttu-id="67d09-111">Database che verrà esteso.</span><span class="sxs-lookup"><span data-stu-id="67d09-111">The database that will be extended.</span></span>

<span data-ttu-id="67d09-112">*cpg*</span><span class="sxs-lookup"><span data-stu-id="67d09-112">*cpg*</span></span>

<span data-ttu-id="67d09-113">Dimensioni richieste del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="67d09-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="67d09-114">*pcpgActual*</span><span class="sxs-lookup"><span data-stu-id="67d09-114">*pcpgActual*</span></span>

<span data-ttu-id="67d09-115">Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="67d09-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="67d09-116">Se la chiamata API ha esito negativo, il contenuto del parametro *pcpgActual* non è definito.</span><span class="sxs-lookup"><span data-stu-id="67d09-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="67d09-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="67d09-117">*grbit*</span></span>

<span data-ttu-id="67d09-118">Gruppo di bit che specifica zero o più valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="67d09-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67d09-119">Valore</span><span class="sxs-lookup"><span data-stu-id="67d09-119">Value</span></span></p></th>
<th><p><span data-ttu-id="67d09-120">Significato</span><span class="sxs-lookup"><span data-stu-id="67d09-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67d09-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="67d09-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="67d09-122">Espandere solo il database.</span><span class="sxs-lookup"><span data-stu-id="67d09-122">Only grow the database.</span></span> <span data-ttu-id="67d09-123">Se la chiamata di ridimensionamento riduce il database, non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="67d09-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="67d09-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67d09-124">Return value</span></span>

<span data-ttu-id="67d09-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="67d09-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="67d09-126">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="67d09-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67d09-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="67d09-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="67d09-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67d09-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67d09-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="67d09-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="67d09-130">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="67d09-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d09-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="67d09-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="67d09-132">Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di espansione.</span><span class="sxs-lookup"><span data-stu-id="67d09-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67d09-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="67d09-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="67d09-134">È stato restituito un errore relativo al file dalla funzione <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> .</span><span class="sxs-lookup"><span data-stu-id="67d09-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="67d09-135">Per ulteriori informazioni sugli altri errori correlati ai file che potrebbero essere restituiti, vedere <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="67d09-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="67d09-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="67d09-136">Remarks</span></span>

<span data-ttu-id="67d09-137">Se la funzione **JetResizeDatabase** viene chiamata prima dell'inserimento di grandi quantità di dati, il file di database verrà aumentato in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="67d09-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="67d09-138">In questo modo si ridurrà la probabilità che il file di database diventi frammentato a livello di file system e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato.</span><span class="sxs-lookup"><span data-stu-id="67d09-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="67d09-139">La crescita del file di database può essere più veloce rispetto alla crescita più volte.</span><span class="sxs-lookup"><span data-stu-id="67d09-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="67d09-140">Per impostare le dimensioni di un database non aperto, vedere [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="67d09-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="67d09-141">Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite nel parametro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="67d09-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="67d09-142">Due pagine riservate aggiuntive potrebbero non essere conteggiate nel parametro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="67d09-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="67d09-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67d09-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67d09-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="67d09-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="67d09-145">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67d09-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d09-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="67d09-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="67d09-147">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="67d09-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67d09-148"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="67d09-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="67d09-149">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="67d09-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d09-150"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="67d09-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="67d09-151">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="67d09-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67d09-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="67d09-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="67d09-153">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="67d09-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="67d09-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67d09-154">See also</span></span>

[<span data-ttu-id="67d09-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="67d09-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="67d09-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="67d09-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="67d09-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="67d09-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="67d09-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="67d09-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="67d09-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="67d09-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="67d09-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="67d09-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="67d09-161">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="67d09-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
