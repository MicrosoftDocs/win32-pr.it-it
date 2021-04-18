---
description: Hint di ottimizzazione della cache vertex.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Struttura D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322398"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="5afd9-103">\_Struttura D3DDEVINFO VCACHE</span><span class="sxs-lookup"><span data-stu-id="5afd9-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="5afd9-104">Hint di ottimizzazione della cache vertex.</span><span class="sxs-lookup"><span data-stu-id="5afd9-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afd9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5afd9-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="5afd9-106">Members</span><span class="sxs-lookup"><span data-stu-id="5afd9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5afd9-107">**Modello**</span><span class="sxs-lookup"><span data-stu-id="5afd9-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="5afd9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5afd9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5afd9-109">Modello di bit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-109">Bit pattern.</span></span> <span data-ttu-id="5afd9-110">Il valore restituito deve essere FOURCC (' c',' A ',' c',' H ').</span><span class="sxs-lookup"><span data-stu-id="5afd9-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="5afd9-111">**OptMethod**</span><span class="sxs-lookup"><span data-stu-id="5afd9-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="5afd9-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5afd9-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5afd9-113">Metodo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="5afd9-113">Optimizations method.</span></span> <span data-ttu-id="5afd9-114">Utilizzare 0 per ottenere le strisce più lunghe.</span><span class="sxs-lookup"><span data-stu-id="5afd9-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="5afd9-115">Utilizzare 1 per ottimizzare l'utilizzo della cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5afd9-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="5afd9-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="5afd9-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="5afd9-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5afd9-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5afd9-118">Dimensioni della cache utilizzate come destinazione per l'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="5afd9-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="5afd9-119">Questa operazione è necessaria solo se OptMethod è 1.</span><span class="sxs-lookup"><span data-stu-id="5afd9-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="5afd9-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="5afd9-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5afd9-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5afd9-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5afd9-122">Utilizzato dai metodi di ottimizzazione interni per determinare quando riavviare le strisce.</span><span class="sxs-lookup"><span data-stu-id="5afd9-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="5afd9-123">Non può essere impostato o modificato da un utente.</span><span class="sxs-lookup"><span data-stu-id="5afd9-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="5afd9-124">Questa operazione è necessaria solo se OptMethod è 1.</span><span class="sxs-lookup"><span data-stu-id="5afd9-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5afd9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5afd9-125">Requirements</span></span>



| <span data-ttu-id="5afd9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5afd9-126">Requirement</span></span> | <span data-ttu-id="5afd9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5afd9-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5afd9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5afd9-128">Header</span></span><br/> | <dl> <span data-ttu-id="5afd9-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5afd9-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5afd9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5afd9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afd9-131">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="5afd9-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="5afd9-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="5afd9-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
