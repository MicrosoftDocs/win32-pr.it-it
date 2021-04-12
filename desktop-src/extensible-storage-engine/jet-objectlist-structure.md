---
description: 'Altre informazioni su: struttura JET_OBJECTLIST'
title: Struttura JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347516"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="7a1f7-103">Struttura JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="7a1f7-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="7a1f7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7a1f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="7a1f7-105">Struttura JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="7a1f7-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="7a1f7-106">La struttura **JET_OBJECTLIST** attraversa una tabella temporanea creata con [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="7a1f7-107">Ogni riga della tabella temporanea descrive un oggetto nel database.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="7a1f7-108">Membri</span><span class="sxs-lookup"><span data-stu-id="7a1f7-108">Members</span></span>

<span data-ttu-id="7a1f7-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-109">**cbStruct**</span></span>

<span data-ttu-id="7a1f7-110">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="7a1f7-111">La chiamata API aggiornerà questo campo, in modo che il chiamante assicuri che questo valore corrisponda a sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="7a1f7-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-112">**tableid**</span></span>

<span data-ttu-id="7a1f7-113">Identificatore di tabella della tabella temporanea creata.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="7a1f7-114">Il chiamante deve contenere codice che chiude la tabella.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="7a1f7-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-115">**cRecord**</span></span>

<span data-ttu-id="7a1f7-116">Numero di record nella tabella temporanea creata.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="7a1f7-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-117">**columnidcontainername**</span></span>

<span data-ttu-id="7a1f7-118">Identificatore di colonna del nome del tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="7a1f7-119">Gli unici contenitori attualmente supportati sono le tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="7a1f7-120">Questa colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-121">**columnidobjectname**</span></span>

<span data-ttu-id="7a1f7-122">Identificatore di colonna del nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="7a1f7-123">Questa colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-124">**columnidobjtyp**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-124">**columnidobjtyp**</span></span>

<span data-ttu-id="7a1f7-125">Identificatore di colonna del tipo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="7a1f7-126">Gli unici contenitori attualmente supportati sono tabelle, pertanto questo campo verrà JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="7a1f7-127">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-128">**columniddtCreate**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-128">**columniddtCreate**</span></span>

<span data-ttu-id="7a1f7-129">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-129">Obsolete.</span></span> <span data-ttu-id="7a1f7-130">Non usare.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-130">Do not use.</span></span>

<span data-ttu-id="7a1f7-131">**columniddtUpdate**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-131">**columniddtUpdate**</span></span>

<span data-ttu-id="7a1f7-132">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-132">Obsolete.</span></span> <span data-ttu-id="7a1f7-133">Non usare.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-133">Do not use.</span></span>

<span data-ttu-id="7a1f7-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-134">**columnidgrbit**</span></span>

<span data-ttu-id="7a1f7-135">Identificatore di colonna di **grbits** applicabili all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="7a1f7-136">Per un elenco dei **grbits** applicabili, vedere [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="7a1f7-137">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-138">**columnidflags**</span></span>

<span data-ttu-id="7a1f7-139">Identificatore di colonna dei flag applicabili all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="7a1f7-140">Per un elenco dei flag applicabili, vedere [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="7a1f7-141">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-142">**columnidcRecord**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-142">**columnidcRecord**</span></span>

<span data-ttu-id="7a1f7-143">Identificatore di colonna del numero di record presenti nella tabella denominata in **columnidobjectname**.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="7a1f7-144">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7a1f7-145">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="7a1f7-145">**columnidcPage**</span></span>

<span data-ttu-id="7a1f7-146">Identificatore di colonna del numero di pagine utilizzate dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="7a1f7-147">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f7-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="7a1f7-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a1f7-148">Remarks</span></span>

<span data-ttu-id="7a1f7-149">Ogni riga della tabella temporanea corrisponde a un oggetto nel database.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="7a1f7-150">Quando la tabella temporanea viene creata con il parametro *InfoLevel* nella funzione [JetGetObjectInfo](./jetgetobjectinfo-function.md) impostata su JET_ObjInfoListNoStats, le colonne identificate da **columnidcRecord** e **columnidcPage** non conterranno informazioni significative.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="7a1f7-151">Attualmente, solo le informazioni sulle tabelle saranno incluse nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="7a1f7-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a1f7-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a1f7-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7a1f7-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1f7-154">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1f7-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7a1f7-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1f7-156">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a1f7-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="7a1f7-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1f7-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="7a1f7-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7a1f7-159">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7a1f7-159">See Also</span></span>

[<span data-ttu-id="7a1f7-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="7a1f7-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="7a1f7-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7a1f7-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="7a1f7-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7a1f7-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7a1f7-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7a1f7-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7a1f7-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7a1f7-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7a1f7-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7a1f7-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7a1f7-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="7a1f7-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="7a1f7-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="7a1f7-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="7a1f7-168">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="7a1f7-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
