---
description: 'Altre informazioni su: struttura JET_RECORDLIST'
title: Struttura JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885017"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="d1327-103">Struttura JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="d1327-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="d1327-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d1327-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="d1327-105">Struttura JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="d1327-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="d1327-106">La struttura **JET_RECORDLIST** trova i record che si trovano nell'intersezione degli intervalli di indice specificati quando vengono utilizzati con la funzione [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d1327-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="d1327-107">Membri</span><span class="sxs-lookup"><span data-stu-id="d1327-107">Members</span></span>

<span data-ttu-id="d1327-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d1327-108">**cbStruct**</span></span>

<span data-ttu-id="d1327-109">Dimensioni in byte della struttura **JET_RECORDLIST** .</span><span class="sxs-lookup"><span data-stu-id="d1327-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="d1327-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="d1327-110">**tableid**</span></span>

<span data-ttu-id="d1327-111">Identificatore di tabella di una tabella temporanea che contiene i segnalibri per i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="d1327-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="d1327-112">La tabella verrà chiusa automaticamente se viene eseguito il rollback della transazione corrente con [JetRollback](./jetrollback-function.md); in caso contrario, deve essere chiuso con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="d1327-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="d1327-113">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="d1327-113">**cRecord**</span></span>

<span data-ttu-id="d1327-114">Numero di righe nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="d1327-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="d1327-115">**columnidBookmark**</span><span class="sxs-lookup"><span data-stu-id="d1327-115">**columnidBookmark**</span></span>

<span data-ttu-id="d1327-116">Identificatore di colonna della colonna del segnalibro nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="d1327-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="d1327-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1327-117">Remarks</span></span>

<span data-ttu-id="d1327-118">La tabella temporanea identificata da **TableID** ha una sola colonna.</span><span class="sxs-lookup"><span data-stu-id="d1327-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="d1327-119">Questa singola colonna include i segnalibri e ogni record deve rientrare in un buffer di dimensioni JET_cbBookmarkMost byte.</span><span class="sxs-lookup"><span data-stu-id="d1327-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="d1327-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1327-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1327-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d1327-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d1327-122">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d1327-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1327-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d1327-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d1327-124">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d1327-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1327-125"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d1327-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d1327-126">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d1327-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d1327-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d1327-127">See Also</span></span>

[<span data-ttu-id="d1327-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d1327-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d1327-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d1327-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d1327-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d1327-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d1327-131">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d1327-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="d1327-132">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="d1327-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="d1327-133">JetRollback</span><span class="sxs-lookup"><span data-stu-id="d1327-133">JetRollback</span></span>](./jetrollback-function.md)
