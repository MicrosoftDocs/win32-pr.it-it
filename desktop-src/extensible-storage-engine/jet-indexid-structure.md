---
description: 'Altre informazioni su: struttura JET_INDEXID'
title: Struttura JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319679"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="f2850-103">Struttura JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f2850-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="f2850-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2850-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="f2850-105">Struttura JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f2850-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="f2850-106">La struttura **JET_INDEXID** include un ID di indice.</span><span class="sxs-lookup"><span data-stu-id="f2850-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="f2850-107">Un ID di indice è un hint usato per accelerare la selezione dell'indice corrente usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2850-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="f2850-108">Risulta particolarmente utile quando è presente un numero molto elevato di indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="f2850-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="f2850-109">L'ID di indice può essere recuperato tramite [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2850-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="f2850-110">Membri</span><span class="sxs-lookup"><span data-stu-id="f2850-110">Members</span></span>

<span data-ttu-id="f2850-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="f2850-111">**cbStruct**</span></span>

<span data-ttu-id="f2850-112">Dimensione, in byte, dell'ID di indice.</span><span class="sxs-lookup"><span data-stu-id="f2850-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="f2850-113">Si tratta delle dimensioni effettive dell'ID di indice restituito nel buffer di output da [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="f2850-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="f2850-114">**rgbIndexId**</span><span class="sxs-lookup"><span data-stu-id="f2850-114">**rgbIndexId**</span></span>

<span data-ttu-id="f2850-115">BLOB opaco di informazioni utilizzato dal motore per identificare rapidamente un indice nella relativa cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="f2850-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="f2850-116">Non tentare di interpretare il BLOB di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f2850-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="f2850-117">Non è una dimensione impostata.</span><span class="sxs-lookup"><span data-stu-id="f2850-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="f2850-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2850-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2850-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f2850-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2850-120">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f2850-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2850-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f2850-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2850-122">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f2850-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2850-123"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f2850-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2850-124">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f2850-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f2850-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f2850-125">See Also</span></span>

[<span data-ttu-id="f2850-126">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f2850-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="f2850-127">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f2850-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="f2850-128">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="f2850-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="f2850-129">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="f2850-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
