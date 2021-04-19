---
description: Statistiche delle risorse raccolte da D3DDEVINFO \_ ResourceManager quando si usa il meccanismo di query asincrono.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Struttura D3DRESOURCESTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322308"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="4a050-103">Struttura D3DRESOURCESTATS</span><span class="sxs-lookup"><span data-stu-id="4a050-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="4a050-104">Statistiche delle risorse raccolte da [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md) quando si usa il meccanismo di query asincrono.</span><span class="sxs-lookup"><span data-stu-id="4a050-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a050-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a050-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="4a050-106">Members</span><span class="sxs-lookup"><span data-stu-id="4a050-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a050-107">**bThrashing**</span><span class="sxs-lookup"><span data-stu-id="4a050-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-109">Indica se il thrashing si sta verificando.</span><span class="sxs-lookup"><span data-stu-id="4a050-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-110">**ApproxBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="4a050-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-112">Numero approssimativo di byte scaricati da Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4a050-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-113">**NumEvicts**</span><span class="sxs-lookup"><span data-stu-id="4a050-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-115">Numero di oggetti rimossi.</span><span class="sxs-lookup"><span data-stu-id="4a050-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-116">**NumVidCreates**</span><span class="sxs-lookup"><span data-stu-id="4a050-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-118">Numero di oggetti creati nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="4a050-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-119">**LastPri**</span><span class="sxs-lookup"><span data-stu-id="4a050-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-121">Priorità dell'ultimo oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="4a050-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-122">**NumUsed**</span><span class="sxs-lookup"><span data-stu-id="4a050-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-124">Numero di oggetti impostati sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a050-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-125">**NumUsedInVidMem**</span><span class="sxs-lookup"><span data-stu-id="4a050-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-127">Numero di oggetti impostati sul dispositivo, che si trovano già nella memoria del video.</span><span class="sxs-lookup"><span data-stu-id="4a050-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="4a050-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-130">Numero di oggetti nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="4a050-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-131">**WorkingSetBytes**</span><span class="sxs-lookup"><span data-stu-id="4a050-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-133">Numero di byte nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="4a050-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-134">**TotalManaged**</span><span class="sxs-lookup"><span data-stu-id="4a050-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-136">Numero totale di oggetti gestiti.</span><span class="sxs-lookup"><span data-stu-id="4a050-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="4a050-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="4a050-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4a050-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a050-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a050-139">Numero totale di byte di oggetti gestiti.</span><span class="sxs-lookup"><span data-stu-id="4a050-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a050-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a050-140">Requirements</span></span>



| <span data-ttu-id="4a050-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a050-141">Requirement</span></span> | <span data-ttu-id="4a050-142">Valore</span><span class="sxs-lookup"><span data-stu-id="4a050-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a050-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a050-143">Header</span></span><br/> | <dl> <span data-ttu-id="4a050-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a050-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a050-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a050-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a050-146">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="4a050-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4a050-147">Notifica asincrona (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a050-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
