---
description: Identificatore dell'indice a cui accedere in un database.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127254"
---
# <a name="indexid"></a><span data-ttu-id="eddb4-103">INDEXID</span><span class="sxs-lookup"><span data-stu-id="eddb4-103">INDEXID</span></span>

<span data-ttu-id="eddb4-104">Identificatore dell'indice a cui accedere in un database.</span><span class="sxs-lookup"><span data-stu-id="eddb4-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="eddb4-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="eddb4-105">Remarks</span></span>

<span data-ttu-id="eddb4-106">Un **INDEXID** può essere un valore intero che rappresenta l'indice oppure il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="eddb4-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="eddb4-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID \_ null ((INDEXID)-1)</span><span class="sxs-lookup"><span data-stu-id="eddb4-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="eddb4-108">**INDEXID** non valido.</span><span class="sxs-lookup"><span data-stu-id="eddb4-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eddb4-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eddb4-109">Requirements</span></span>



| <span data-ttu-id="eddb4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="eddb4-110">Requirement</span></span> | <span data-ttu-id="eddb4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="eddb4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eddb4-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eddb4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="eddb4-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eddb4-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eddb4-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eddb4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="eddb4-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eddb4-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eddb4-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eddb4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddb4-117">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="eddb4-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="eddb4-118">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="eddb4-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="eddb4-119">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="eddb4-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




