---
description: 'Altre informazioni su: funzione JetDeleteColumn2'
title: JetDeleteColumn2 (funzione)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319645"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="e9626-103">JetDeleteColumn2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9626-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="e9626-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9626-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="e9626-105">JetDeleteColumn2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9626-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="e9626-106">La funzione **JetDeleteColumn2** Elimina una colonna da una tabella di database ESE e consente l'impostazione di un'opzione *grbit* .</span><span class="sxs-lookup"><span data-stu-id="e9626-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="e9626-107">**Windows XP: JetDeleteColumn2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9626-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e9626-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9626-108">Parameters</span></span>

<span data-ttu-id="e9626-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e9626-109">*sesid*</span></span>

<span data-ttu-id="e9626-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="e9626-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="e9626-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e9626-111">*tableid*</span></span>

<span data-ttu-id="e9626-112">Tabella contenente la colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e9626-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="e9626-113">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="e9626-113">*szColumnName*</span></span>

<span data-ttu-id="e9626-114">Nome della colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e9626-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="e9626-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e9626-115">*grbit*</span></span>

<span data-ttu-id="e9626-116">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e9626-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9626-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e9626-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e9626-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e9626-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9626-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="e9626-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="e9626-120">Impostando JET_bitDeleteColumIgnoreTemplateColumns si farà in modo che l'API tenti di eliminare solo le colonne nella tabella derivata.</span><span class="sxs-lookup"><span data-stu-id="e9626-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="e9626-121">Se una colonna con tale nome esiste nella tabella di base, verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="e9626-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e9626-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9626-122">Return Value</span></span>

<span data-ttu-id="e9626-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e9626-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e9626-124">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e9626-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9626-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e9626-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="e9626-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9626-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9626-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e9626-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e9626-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e9626-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="e9626-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="e9626-130">La colonna è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="e9626-130">The column is currently in use.</span></span> <span data-ttu-id="e9626-131">Può essere usato attualmente da un indice.</span><span class="sxs-lookup"><span data-stu-id="e9626-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9626-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="e9626-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="e9626-133">È stato effettuato un tentativo di modificare il DDL fisso.</span><span class="sxs-lookup"><span data-stu-id="e9626-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="e9626-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="e9626-135">La colonna denominata in <em>szColumnName</em> esiste nella tabella del modello e non è possibile modificare il DDL di una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="e9626-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9626-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="e9626-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="e9626-137">Questo può essere restituito se è stato specificato un nome non valido per <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="e9626-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="e9626-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="e9626-139">La tabella non è accessibile in scrittura.</span><span class="sxs-lookup"><span data-stu-id="e9626-139">The table is not writable.</span></span> <span data-ttu-id="e9626-140">Questa operazione può essere restituita se il database è stato aperto in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9626-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9626-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e9626-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e9626-142">La transazione è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9626-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e9626-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9626-143">Remarks</span></span>

<span data-ttu-id="e9626-144">La chiamata di [JetDeleteColumn](./jetdeletecolumn-function.md) è identica alla chiamata di **JetDeleteColumn2** con *grbit* impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="e9626-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e9626-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9626-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9626-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-147">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9626-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-149">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9626-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9626-150"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-151">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e9626-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-152"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-153">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e9626-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9626-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-155">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e9626-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9626-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e9626-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e9626-157">Implementato come <strong>JetDeleteColumn2W</strong> (Unicode) e <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e9626-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e9626-158">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e9626-158">See Also</span></span>

[<span data-ttu-id="e9626-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e9626-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e9626-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e9626-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e9626-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e9626-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e9626-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e9626-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e9626-163">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="e9626-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
