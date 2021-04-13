---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMNID'
title: Struttura JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526083"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="141bd-103">Struttura JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="141bd-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="141bd-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="141bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="141bd-105">Struttura JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="141bd-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="141bd-106">La struttura **JET_ENUMCOLUMNID** enumera un set specifico di colonne e, facoltativamente, un set specifico di più valori per tali colonne quando viene utilizzata la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="141bd-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="141bd-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMNID** .</span><span class="sxs-lookup"><span data-stu-id="141bd-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="141bd-108">Membri</span><span class="sxs-lookup"><span data-stu-id="141bd-108">Members</span></span>

<span data-ttu-id="141bd-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="141bd-109">**columnid**</span></span>

<span data-ttu-id="141bd-110">ID di colonna da enumerare.</span><span class="sxs-lookup"><span data-stu-id="141bd-110">The column ID to enumerate.</span></span>

<span data-ttu-id="141bd-111">Se l'ID di colonna è 0 (zero), l'enumerazione di questa colonna verrà ignorata e verrà generato uno slot corrispondente nella matrice di output di [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) strutture con lo stato della colonna JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="141bd-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="141bd-112">**ctagSequence**</span><span class="sxs-lookup"><span data-stu-id="141bd-112">**ctagSequence**</span></span>

<span data-ttu-id="141bd-113">Identifica facoltativamente una matrice di valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="141bd-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="141bd-114">Se **ctagSequence** è 0 (zero), **rgtagSequence** viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="141bd-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="141bd-115">Se un elemento di **rgtagSequence** è 0 (zero), l'enumerazione del valore della colonna (in base a un indice in base 1) verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="141bd-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="141bd-116">Uno slot corrispondente nella matrice di output della struttura **JET_ENUMCOLUMNID** verrà generato con un valore di stato della colonna pari a JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="141bd-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="141bd-117">**rgtagSequence**</span><span class="sxs-lookup"><span data-stu-id="141bd-117">**rgtagSequence**</span></span>

<span data-ttu-id="141bd-118">Matrice di indici in base uno nella matrice di valori di colonna per una colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="141bd-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="141bd-119">Un singolo elemento è un **itagSequence** definito in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="141bd-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="141bd-120">Un **itagSequence** di 0 (zero) indica "Skip".</span><span class="sxs-lookup"><span data-stu-id="141bd-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="141bd-121">Un **itagSequence** di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="141bd-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="141bd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="141bd-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="141bd-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="141bd-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="141bd-124">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="141bd-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="141bd-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="141bd-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="141bd-126">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="141bd-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="141bd-127"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="141bd-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="141bd-128">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="141bd-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="141bd-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="141bd-129">See Also</span></span>

[<span data-ttu-id="141bd-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="141bd-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="141bd-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="141bd-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="141bd-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="141bd-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="141bd-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="141bd-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="141bd-134">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="141bd-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
