---
description: 'Altre informazioni su: struttura JET_INDEXRANGE'
title: Struttura JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315138"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="76ce6-103">Struttura JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="76ce6-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="76ce6-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="76ce6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="76ce6-105">Struttura JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="76ce6-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="76ce6-106">La struttura **JET_INDEXRANGE** identifica un intervallo di indice quando viene utilizzato con la funzione [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="76ce6-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="76ce6-107">Membri</span><span class="sxs-lookup"><span data-stu-id="76ce6-107">Members</span></span>

<span data-ttu-id="76ce6-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="76ce6-108">**cbStruct**</span></span>

<span data-ttu-id="76ce6-109">Dimensione, in byte, del **JET_INDEXRANGE**.</span><span class="sxs-lookup"><span data-stu-id="76ce6-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="76ce6-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="76ce6-110">**tableid**</span></span>

<span data-ttu-id="76ce6-111">Un cursore che in precedenza aveva un intervallo di indici impostato con [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="76ce6-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="76ce6-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="76ce6-112">**grbit**</span></span>

<span data-ttu-id="76ce6-113">Maschera di maschera costituita esattamente da uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="76ce6-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76ce6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="76ce6-114">Value</span></span></p></th>
<th><p><span data-ttu-id="76ce6-115">Significato</span><span class="sxs-lookup"><span data-stu-id="76ce6-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76ce6-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="76ce6-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="76ce6-117">Specifica che l'intervallo di indici deve essere trattato normalmente.</span><span class="sxs-lookup"><span data-stu-id="76ce6-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76ce6-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="76ce6-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="76ce6-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="76ce6-119">Reserved for future use.</span></span> <span data-ttu-id="76ce6-120">Non usare.</span><span class="sxs-lookup"><span data-stu-id="76ce6-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="76ce6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="76ce6-121">Remarks</span></span>

<span data-ttu-id="76ce6-122">Ogni **JET_INDEXRANGE** struttura passata a [JetIntersectIndexes](./jetintersectindexes-function.md) rappresenta un intervallo di indici, che verrà intersecato dalla chiamata API.</span><span class="sxs-lookup"><span data-stu-id="76ce6-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="76ce6-123">Il cursore specificato in **JET_INDEXRANGE** deve avere già un intervallo di indici valido impostato su di esso, con una chiamata riuscita a [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="76ce6-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="76ce6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76ce6-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76ce6-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="76ce6-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="76ce6-126">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="76ce6-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76ce6-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="76ce6-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="76ce6-128">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="76ce6-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76ce6-129"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="76ce6-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="76ce6-130">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="76ce6-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="76ce6-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="76ce6-131">See Also</span></span>

[<span data-ttu-id="76ce6-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="76ce6-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="76ce6-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="76ce6-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="76ce6-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="76ce6-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="76ce6-135">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="76ce6-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="76ce6-136">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="76ce6-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="76ce6-137">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="76ce6-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
