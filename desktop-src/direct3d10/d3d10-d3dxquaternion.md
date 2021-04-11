---
description: Descrive un quaternione.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Struttura D3DXQUATERNION (D3DX10Math. h)
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
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355329"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="5281f-103">Struttura D3DXQUATERNION (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5281f-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="5281f-104">Descrive un quaternione.</span><span class="sxs-lookup"><span data-stu-id="5281f-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="5281f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5281f-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="5281f-106">Members</span><span class="sxs-lookup"><span data-stu-id="5281f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5281f-107">**x**</span><span class="sxs-lookup"><span data-stu-id="5281f-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="5281f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5281f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5281f-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="5281f-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="5281f-110">**y**</span><span class="sxs-lookup"><span data-stu-id="5281f-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="5281f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5281f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5281f-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="5281f-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="5281f-113">**z**</span><span class="sxs-lookup"><span data-stu-id="5281f-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="5281f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5281f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5281f-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="5281f-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="5281f-116">**w**</span><span class="sxs-lookup"><span data-stu-id="5281f-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="5281f-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5281f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5281f-118">Il componente w.</span><span class="sxs-lookup"><span data-stu-id="5281f-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5281f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5281f-119">Remarks</span></span>

<span data-ttu-id="5281f-120">I quaternioni aggiungono un quarto elemento ai \[ valori x, y, z \] che definiscono un vettore, ottenendo vettori 4D arbitrari.</span><span class="sxs-lookup"><span data-stu-id="5281f-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="5281f-121">Tuttavia, di seguito viene illustrato il modo in cui ogni elemento di un quaternione dell'unità è correlato a una rotazione dell'angolo dell'asse (dove q rappresenta un quaternione di unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione di CCW desiderata sull'asse):</span><span class="sxs-lookup"><span data-stu-id="5281f-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="5281f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5281f-122">Requirements</span></span>



| <span data-ttu-id="5281f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5281f-123">Requirement</span></span> | <span data-ttu-id="5281f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5281f-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5281f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5281f-125">Header</span></span><br/> | <dl> <span data-ttu-id="5281f-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5281f-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5281f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5281f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5281f-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="5281f-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
