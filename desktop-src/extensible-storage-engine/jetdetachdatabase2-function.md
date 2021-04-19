---
description: 'Altre informazioni su: funzione JetDetachDatabase2'
title: Funzione JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315621"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ab8d2-103">Funzione JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab8d2-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="ab8d2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ab8d2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ab8d2-105">Funzione JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab8d2-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="ab8d2-106">La funzione **JetDetachDatabase2** rilascia un file di database precedentemente collegato a una sessione di database.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="ab8d2-107">**Windows XP:**  **JetDetachDatabase2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ab8d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab8d2-108">Parameters</span></span>

<span data-ttu-id="ab8d2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-109">*sesid*</span></span>

<span data-ttu-id="ab8d2-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="ab8d2-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-111">*szFilename*</span></span>

<span data-ttu-id="ab8d2-112">Nome del database da scollegare.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-112">The name of the database to detach.</span></span> <span data-ttu-id="ab8d2-113">Se *szFileName* è **null** o una stringa vuota, tutti i database collegati a *sesid* verranno scollegati.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="ab8d2-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-114">*grbit*</span></span>

<span data-ttu-id="ab8d2-115">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab8d2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ab8d2-116">Value</span></span></p></th>
<th><p><span data-ttu-id="ab8d2-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ab8d2-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="ab8d2-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-119">Impone la chiusura e lo scollegamento del database.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="ab8d2-120">Se JET_bitForceCloseAndDetach non è supportato, verrà restituito JET_errForceDetachNotAllowed.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="ab8d2-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-122">Forza la disconnessione del database.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-122">Forces the database to be detached.</span></span> <span data-ttu-id="ab8d2-123">Se JET_bitForceDetach non è supportato, verrà restituito JET_errForceDetachNotAllowed.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ab8d2-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab8d2-124">Return Value</span></span>

<span data-ttu-id="ab8d2-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ab8d2-126">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ab8d2-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab8d2-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ab8d2-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="ab8d2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab8d2-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ab8d2-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-130">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="ab8d2-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-132">È in corso il backup del database e non è possibile scollegarlo.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="ab8d2-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-134">Il database è stato aperto da <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="ab8d2-135">Prima dello scollegamento, è necessario chiudere i database.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="ab8d2-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-137">Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ab8d2-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-139">JET_bitForceDetach non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ab8d2-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ab8d2-141">È stato effettuato un tentativo di scollegamento di un database in una transazione.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ab8d2-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab8d2-142">Remarks</span></span>

<span data-ttu-id="ab8d2-143">Se un database collegato è stato aperto (con [JetAttachDatabase](./jetattachdatabase-function.md)), è necessario chiuderlo con [JetCloseDatabase](./jetclosedatabase-function.md) prima di disconnetterlo.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="ab8d2-144">Solo Windows 2000: i database che non sono stati scollegati prima della chiamata a [JetTerm](./jetterm-function.md) verranno automaticamente ricollegati al successivo chiamata di [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ab8d2-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ab8d2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab8d2-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-147">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-149">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-150"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-151">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-152"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-153">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab8d2-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-155">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab8d2-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ab8d2-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ab8d2-157">Implementato come <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ab8d2-158">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ab8d2-158">See Also</span></span>

[<span data-ttu-id="ab8d2-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ab8d2-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ab8d2-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ab8d2-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ab8d2-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ab8d2-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ab8d2-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ab8d2-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ab8d2-163">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="ab8d2-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="ab8d2-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab8d2-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="ab8d2-165">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="ab8d2-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="ab8d2-166">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="ab8d2-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="ab8d2-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab8d2-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="ab8d2-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="ab8d2-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ab8d2-169">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="ab8d2-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="ab8d2-170">JetTerm</span><span class="sxs-lookup"><span data-stu-id="ab8d2-170">JetTerm</span></span>](./jetterm-function.md)
