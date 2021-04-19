---
description: 'Altre informazioni su: funzione JetDeleteIndex'
title: JetDeleteIndex (funzione)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319179"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="dc679-103">JetDeleteIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="dc679-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="dc679-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc679-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="dc679-105">JetDeleteIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="dc679-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="dc679-106">La funzione **JetDeleteIndex** Elimina un indice da una tabella.</span><span class="sxs-lookup"><span data-stu-id="dc679-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="dc679-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc679-107">Parameters</span></span>

<span data-ttu-id="dc679-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc679-108">*sesid*</span></span>

<span data-ttu-id="dc679-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="dc679-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="dc679-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="dc679-110">*tableid*</span></span>

<span data-ttu-id="dc679-111">Tabella contenente la colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dc679-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="dc679-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="dc679-112">*szIndexName*</span></span>

<span data-ttu-id="dc679-113">Nome dell'indice da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dc679-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="dc679-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc679-114">Return Value</span></span>

<span data-ttu-id="dc679-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="dc679-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dc679-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="dc679-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc679-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dc679-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc679-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc679-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc679-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc679-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc679-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="dc679-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="dc679-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="dc679-122">È stato effettuato un tentativo di eliminare un indice da una tabella fissa (ad esempio, uno creato con JET_bitTableCreateFixedDDL).</span><span class="sxs-lookup"><span data-stu-id="dc679-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc679-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="dc679-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="dc679-124">È stato effettuato un tentativo di eliminare un indice da una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="dc679-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="dc679-125">Una tabella modello ha un linguaggio DDL fisso.</span><span class="sxs-lookup"><span data-stu-id="dc679-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="dc679-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="dc679-127">L'indice denominato in <em>szIndexName</em> non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="dc679-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc679-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="dc679-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="dc679-129">Impossibile aggiornare la tabella perché è stata aperta in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dc679-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="dc679-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="dc679-131">Più thread hanno tentato di usare la stessa sessione di database.</span><span class="sxs-lookup"><span data-stu-id="dc679-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc679-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc679-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="dc679-133">La transazione è stata aperta come transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dc679-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="dc679-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc679-134">Remarks</span></span>

<span data-ttu-id="dc679-135">In caso di esito positivo, l'indice viene eliminato e pertanto non può essere utilizzato successivamente.</span><span class="sxs-lookup"><span data-stu-id="dc679-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="dc679-136">Non deve essere presente alcuna transazione attiva utilizzando l'indice.</span><span class="sxs-lookup"><span data-stu-id="dc679-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="dc679-137">In seguito all'esito positivo, la valuta viene impostata prima del primo record.</span><span class="sxs-lookup"><span data-stu-id="dc679-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc679-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc679-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc679-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-140">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dc679-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-142">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dc679-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc679-143"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-144">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc679-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-145"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-146">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc679-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc679-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-148">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc679-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc679-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="dc679-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="dc679-150">Implementato come <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="dc679-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc679-151">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc679-151">See Also</span></span>

[<span data-ttu-id="dc679-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc679-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dc679-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dc679-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dc679-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dc679-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dc679-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dc679-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dc679-156">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="dc679-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="dc679-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="dc679-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
