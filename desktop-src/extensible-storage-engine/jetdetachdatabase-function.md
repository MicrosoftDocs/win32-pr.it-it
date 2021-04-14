---
description: 'Altre informazioni su: funzione JetDetachDatabase'
title: Funzione JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349926"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="d604f-103">Funzione JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="d604f-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="d604f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d604f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="d604f-105">Funzione JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="d604f-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="d604f-106">La funzione **JetDetachDatabase** rilascia un file di database precedentemente collegato a una sessione di database.</span><span class="sxs-lookup"><span data-stu-id="d604f-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="d604f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d604f-107">Parameters</span></span>

<span data-ttu-id="d604f-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d604f-108">*sesid*</span></span>

<span data-ttu-id="d604f-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="d604f-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d604f-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="d604f-110">*szFilename*</span></span>

<span data-ttu-id="d604f-111">Nome del database da scollegare.</span><span class="sxs-lookup"><span data-stu-id="d604f-111">The name of the database to detach.</span></span> <span data-ttu-id="d604f-112">Se *szFileName* è **null** o una stringa vuota, tutti i database collegati a *sesid* verranno scollegati.</span><span class="sxs-lookup"><span data-stu-id="d604f-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="d604f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d604f-113">Return Value</span></span>

<span data-ttu-id="d604f-114">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="d604f-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d604f-115">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="d604f-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d604f-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d604f-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="d604f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d604f-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d604f-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d604f-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d604f-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d604f-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d604f-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="d604f-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="d604f-121">È in corso il backup del database e non è possibile scollegarlo.</span><span class="sxs-lookup"><span data-stu-id="d604f-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d604f-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="d604f-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="d604f-123">Il database è stato aperto da <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="d604f-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="d604f-124">Prima dello scollegamento, è necessario chiudere i database.</span><span class="sxs-lookup"><span data-stu-id="d604f-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d604f-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="d604f-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="d604f-126">Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="d604f-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d604f-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="d604f-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="d604f-128">È stato effettuato un tentativo di scollegamento di un database in una transazione.</span><span class="sxs-lookup"><span data-stu-id="d604f-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d604f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d604f-129">Remarks</span></span>

<span data-ttu-id="d604f-130">Se un database collegato è stato aperto (con [JetAttachDatabase](./jetattachdatabase-function.md)), è necessario chiuderlo con [JetCloseDatabase](./jetclosedatabase-function.md) prima di disconnetterlo.</span><span class="sxs-lookup"><span data-stu-id="d604f-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="d604f-131">Solo Windows 2000: i database che non sono stati scollegati prima della chiamata a [JetTerm](./jetterm-function.md) verranno automaticamente ricollegati al successivo chiamata di [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d604f-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d604f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d604f-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d604f-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-134">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d604f-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d604f-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-136">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d604f-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d604f-137"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-138">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d604f-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d604f-139"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-140">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d604f-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d604f-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-142">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d604f-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d604f-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d604f-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d604f-144">Implementato come <strong>JetDetachDatabaseW</strong> (Unicode) e <strong>JetDetachDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d604f-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d604f-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d604f-145">See Also</span></span>

[<span data-ttu-id="d604f-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d604f-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d604f-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d604f-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d604f-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d604f-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d604f-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d604f-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d604f-150">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="d604f-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="d604f-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="d604f-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="d604f-152">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="d604f-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="d604f-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="d604f-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="d604f-154">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="d604f-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="d604f-155">JetTerm</span><span class="sxs-lookup"><span data-stu-id="d604f-155">JetTerm</span></span>](./jetterm-function.md)
