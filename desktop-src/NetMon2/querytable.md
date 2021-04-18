---
description: La struttura QUERYTABLE fornisce un elenco dei computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Struttura QUERYTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310960"
---
# <a name="querytable-structure"></a><span data-ttu-id="b7f1e-103">Struttura QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="b7f1e-103">QUERYTABLE structure</span></span>

<span data-ttu-id="b7f1e-104">La struttura **QUERYTABLE** fornisce un elenco dei computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7f1e-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="b7f1e-106">Members</span><span class="sxs-lookup"><span data-stu-id="b7f1e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7f1e-107">**nStationQueries**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="b7f1e-108">In input, il numero massimo di computer che si desidera Network Monitor restituire.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="b7f1e-109">Nell'output, numero di strutture [STATIONQUERY](stationquery.md) restituite da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="b7f1e-110">Ogni struttura **STATIONQUERY** rappresenta un computer che attualmente sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-111">**StationQuery**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="b7f1e-112">In input, matrice di strutture [STATIONQUERY](stationquery.md) vuote che contiene il numero di elementi specificato in **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="b7f1e-113">Nell'output, una struttura [STATIONQUERY](stationquery.md) piena per ogni computer che sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="b7f1e-114">Il numero di elementi riempiti viene restituito da **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7f1e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7f1e-115">Remarks</span></span>

<span data-ttu-id="b7f1e-116">La memoria per questa struttura e la matrice [STATIONQUERY](stationquery.md) deve essere allocata dall'applicazione chiamante e liberata dopo che le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f1e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7f1e-117">Requirements</span></span>



| <span data-ttu-id="b7f1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f1e-118">Requirement</span></span> | <span data-ttu-id="b7f1e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f1e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f1e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f1e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7f1e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b7f1e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f1e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7f1e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7f1e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7f1e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f1e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f1e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7f1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f1e-127">IDelaydC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b7f1e-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="b7f1e-128">IESP::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b7f1e-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="b7f1e-129">IRTC:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="b7f1e-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="b7f1e-130">IStats:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="b7f1e-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="b7f1e-131">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="b7f1e-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




