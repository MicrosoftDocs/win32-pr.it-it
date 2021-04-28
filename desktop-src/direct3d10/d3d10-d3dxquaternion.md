---
description: 'Struttura D3DXQUATERNION (D3DX10Math.h): descrive un quaternione.'
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Struttura D3DXQUATERNION (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103249"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="4d221-103">Struttura D3DXQUATERNION (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4d221-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="4d221-104">Descrive un quaternione.</span><span class="sxs-lookup"><span data-stu-id="4d221-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d221-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d221-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="4d221-106">Members</span><span class="sxs-lookup"><span data-stu-id="4d221-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d221-107">**x**</span><span class="sxs-lookup"><span data-stu-id="4d221-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="4d221-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d221-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d221-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="4d221-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="4d221-110">**y**</span><span class="sxs-lookup"><span data-stu-id="4d221-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="4d221-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d221-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d221-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="4d221-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="4d221-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="4d221-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="4d221-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d221-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d221-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="4d221-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="4d221-116">**w**</span><span class="sxs-lookup"><span data-stu-id="4d221-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="4d221-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d221-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d221-118">Componente w.</span><span class="sxs-lookup"><span data-stu-id="4d221-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d221-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d221-119">Remarks</span></span>

<span data-ttu-id="4d221-120">I quaternioni aggiungono un quarto elemento ai valori x, y, z che definiscono un vettore, con conseguente vettori \[ \] 4D arbitrari.</span><span class="sxs-lookup"><span data-stu-id="4d221-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="4d221-121">Tuttavia, l'esempio seguente illustra come ogni elemento di un quaternione di unità è correlato a una rotazione asse-angolo (dove q rappresenta un quaternione unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione CCW desiderata intorno all'asse:</span><span class="sxs-lookup"><span data-stu-id="4d221-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="4d221-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d221-122">Requirements</span></span>



| <span data-ttu-id="4d221-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d221-123">Requirement</span></span> | <span data-ttu-id="4d221-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4d221-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d221-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d221-125">Header</span></span><br/> | <dl> <span data-ttu-id="4d221-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4d221-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d221-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d221-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d221-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="4d221-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
