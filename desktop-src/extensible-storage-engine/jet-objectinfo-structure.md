---
description: 'Altre informazioni su: struttura JET_OBJECTINFO'
title: Struttura JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057931"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="511dd-103">Struttura JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="511dd-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="511dd-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="511dd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="511dd-105">Struttura JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="511dd-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="511dd-106">La struttura **JET_OBJECTINFO** include informazioni su un oggetto.</span><span class="sxs-lookup"><span data-stu-id="511dd-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="511dd-107">Le tabelle sono gli unici tipi di oggetto attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="511dd-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="511dd-108">Membri</span><span class="sxs-lookup"><span data-stu-id="511dd-108">Members</span></span>

<span data-ttu-id="511dd-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="511dd-109">**cbStruct**</span></span>

<span data-ttu-id="511dd-110">Dimensione, in byte, della struttura **JET_OBJECTINFO** .</span><span class="sxs-lookup"><span data-stu-id="511dd-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="511dd-111">**objtyp**</span><span class="sxs-lookup"><span data-stu-id="511dd-111">**objtyp**</span></span>

<span data-ttu-id="511dd-112">Include il [JET_OBJTYP](./jet-objtyp.md) della struttura.</span><span class="sxs-lookup"><span data-stu-id="511dd-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="511dd-113">Attualmente verranno restituite solo le tabelle, ovvero JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="511dd-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="511dd-114">**dtCreate**</span><span class="sxs-lookup"><span data-stu-id="511dd-114">**dtCreate**</span></span>

<span data-ttu-id="511dd-115">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="511dd-115">Obsolete.</span></span> <span data-ttu-id="511dd-116">Non usare.</span><span class="sxs-lookup"><span data-stu-id="511dd-116">Do not use.</span></span>

<span data-ttu-id="511dd-117">**dtUpdate**</span><span class="sxs-lookup"><span data-stu-id="511dd-117">**dtUpdate**</span></span>

<span data-ttu-id="511dd-118">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="511dd-118">Obsolete.</span></span> <span data-ttu-id="511dd-119">Non usare.</span><span class="sxs-lookup"><span data-stu-id="511dd-119">Do not use.</span></span>

<span data-ttu-id="511dd-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="511dd-120">**grbit**</span></span>

<span data-ttu-id="511dd-121">Gruppo di bit che contiene le opzioni disponibili per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="511dd-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="511dd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="511dd-122">Value</span></span></p></th>
<th><p><span data-ttu-id="511dd-123">Significato</span><span class="sxs-lookup"><span data-stu-id="511dd-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="511dd-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="511dd-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="511dd-125">La tabella può includere segnalibri.</span><span class="sxs-lookup"><span data-stu-id="511dd-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="511dd-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="511dd-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="511dd-127">È possibile eseguire il rollback della tabella.</span><span class="sxs-lookup"><span data-stu-id="511dd-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="511dd-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="511dd-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="511dd-129">È possibile aggiornare la tabella.</span><span class="sxs-lookup"><span data-stu-id="511dd-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="511dd-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="511dd-130">**flags**</span></span>

<span data-ttu-id="511dd-131">Campo di bit che contiene zero o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="511dd-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="511dd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="511dd-132">Value</span></span></p></th>
<th><p><span data-ttu-id="511dd-133">Significato</span><span class="sxs-lookup"><span data-stu-id="511dd-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="511dd-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="511dd-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="511dd-135">La tabella è una tabella di sistema ed è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="511dd-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="511dd-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="511dd-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="511dd-137">Tabella DDL ereditata da una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="511dd-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="511dd-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="511dd-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="511dd-139">Impossibile modificare il linguaggio DDL per la tabella.</span><span class="sxs-lookup"><span data-stu-id="511dd-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="511dd-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="511dd-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="511dd-141">Utilizzato in combinazione con JET_bitObjectTableTemplate per non consentire colonne fisse o variabili nelle tabelle derivate, in modo che le colonne fisse o variabili possano essere aggiunte al modello in futuro.</span><span class="sxs-lookup"><span data-stu-id="511dd-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="511dd-142"><strong>Windows XP:  </strong> Questo valore è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="511dd-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="511dd-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="511dd-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="511dd-144">La tabella è una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="511dd-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="511dd-145">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="511dd-145">**cRecord**</span></span>

<span data-ttu-id="511dd-146">Numero di record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="511dd-146">The number of records in the table.</span></span>

<span data-ttu-id="511dd-147">Questo valore viene recuperato solo se **JET_OBJECTINFO** è stato passato a [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="511dd-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="511dd-148">**cPage**</span><span class="sxs-lookup"><span data-stu-id="511dd-148">**cPage**</span></span>

<span data-ttu-id="511dd-149">Numero di pagine utilizzate dalla tabella.</span><span class="sxs-lookup"><span data-stu-id="511dd-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="511dd-150">Questo valore viene recuperato solo se **JET_OBJECTINFO** è stato passato a [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="511dd-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="511dd-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="511dd-151">Remarks</span></span>

<span data-ttu-id="511dd-152">Una struttura **JET_OBJECTINFO** viene popolata da una chiamata a [JetGetObjectInfo](./jetgetobjectinfo-function.md) o [JetGetTableInfo](./jetgettableinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="511dd-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="511dd-153">Se la chiamata API ha esito negativo, il contenuto della struttura non è definito.</span><span class="sxs-lookup"><span data-stu-id="511dd-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="511dd-154">Se applicabile, le statistiche della tabella includono il numero di record e il numero di pagine presenti nell'indice cluster, ovvero l'indice contenente i dati del record.</span><span class="sxs-lookup"><span data-stu-id="511dd-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="511dd-155">È possibile accedere alle statistiche dell'indice separatamente in base al nome, utilizzando [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="511dd-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="511dd-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="511dd-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="511dd-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="511dd-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="511dd-158">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="511dd-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="511dd-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="511dd-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="511dd-160">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="511dd-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="511dd-161"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="511dd-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="511dd-162">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="511dd-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="511dd-163">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="511dd-163">See Also</span></span>

[<span data-ttu-id="511dd-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="511dd-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="511dd-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="511dd-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="511dd-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="511dd-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="511dd-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="511dd-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="511dd-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="511dd-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="511dd-169">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="511dd-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="511dd-170">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="511dd-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="511dd-171">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="511dd-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="511dd-172">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="511dd-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
