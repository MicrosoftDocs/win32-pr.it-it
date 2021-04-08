---
description: 'Altre informazioni su: funzione JetDeleteColumn'
title: JetDeleteColumn (funzione)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969529"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="25a49-103">JetDeleteColumn (funzione)</span><span class="sxs-lookup"><span data-stu-id="25a49-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="25a49-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25a49-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="25a49-105">JetDeleteColumn (funzione)</span><span class="sxs-lookup"><span data-stu-id="25a49-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="25a49-106">La funzione **JetDeleteColumn** Elimina una colonna da una tabella di database ESE.</span><span class="sxs-lookup"><span data-stu-id="25a49-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="25a49-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="25a49-107">Parameters</span></span>

<span data-ttu-id="25a49-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="25a49-108">*sesid*</span></span>

<span data-ttu-id="25a49-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="25a49-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="25a49-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="25a49-110">*tableid*</span></span>

<span data-ttu-id="25a49-111">Tabella da cui eliminare la colonna.</span><span class="sxs-lookup"><span data-stu-id="25a49-111">The table from which to delete the column.</span></span>

<span data-ttu-id="25a49-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="25a49-112">*szColumnName*</span></span>

<span data-ttu-id="25a49-113">Nome della colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="25a49-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="25a49-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25a49-114">Return Value</span></span>

<span data-ttu-id="25a49-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="25a49-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="25a49-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="25a49-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25a49-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="25a49-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="25a49-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25a49-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25a49-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="25a49-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="25a49-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="25a49-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="25a49-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="25a49-122">La colonna è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="25a49-122">The column is currently in use.</span></span> <span data-ttu-id="25a49-123">Può essere usato attualmente da un indice.</span><span class="sxs-lookup"><span data-stu-id="25a49-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25a49-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="25a49-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="25a49-125">È stato effettuato un tentativo di modificare il DDL fisso.</span><span class="sxs-lookup"><span data-stu-id="25a49-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="25a49-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="25a49-127">La colonna denominata in <em>szColumnName</em> esiste nella tabella del modello e non è possibile modificare il DDL di una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="25a49-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25a49-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="25a49-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="25a49-129">Questo può essere restituito se è stato specificato un nome non valido per <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="25a49-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="25a49-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="25a49-131">La tabella non è accessibile in scrittura.</span><span class="sxs-lookup"><span data-stu-id="25a49-131">The table is not writable.</span></span> <span data-ttu-id="25a49-132">Questa operazione può essere restituita se il database è stato aperto in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="25a49-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25a49-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="25a49-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="25a49-134">La transazione è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="25a49-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="25a49-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="25a49-135">Remarks</span></span>

<span data-ttu-id="25a49-136">La chiamata di **JetDeleteColumn** è identica alla chiamata di [JetDeleteColumn2](./jetdeletecolumn2-function.md) con *grbit* impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="25a49-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="25a49-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25a49-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25a49-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-139">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="25a49-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-141">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="25a49-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25a49-142"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-143">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="25a49-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-144"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-145">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25a49-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25a49-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-147">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25a49-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25a49-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="25a49-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="25a49-149">Implementato come <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="25a49-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25a49-150">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="25a49-150">See Also</span></span>

[<span data-ttu-id="25a49-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25a49-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25a49-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="25a49-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="25a49-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="25a49-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="25a49-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="25a49-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="25a49-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="25a49-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
