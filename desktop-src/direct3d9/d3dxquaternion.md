---
description: Descrive un quaternione.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Struttura D3DXQUATERNION (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322499"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="c6df8-103">Struttura D3DXQUATERNION (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c6df8-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="c6df8-104">Descrive un quaternione.</span><span class="sxs-lookup"><span data-stu-id="c6df8-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6df8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6df8-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="c6df8-106">Members</span><span class="sxs-lookup"><span data-stu-id="c6df8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6df8-107">**x**</span><span class="sxs-lookup"><span data-stu-id="c6df8-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c6df8-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6df8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c6df8-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="c6df8-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="c6df8-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c6df8-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c6df8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6df8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c6df8-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="c6df8-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="c6df8-113">**z**</span><span class="sxs-lookup"><span data-stu-id="c6df8-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="c6df8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6df8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c6df8-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="c6df8-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="c6df8-116">**w**</span><span class="sxs-lookup"><span data-stu-id="c6df8-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="c6df8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6df8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c6df8-118">Il componente w.</span><span class="sxs-lookup"><span data-stu-id="c6df8-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6df8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6df8-119">Remarks</span></span>

<span data-ttu-id="c6df8-120">I quaternioni aggiungono un quarto elemento ai \[ valori x, y, z \] che definiscono un vettore, ottenendo vettori 4D arbitrari.</span><span class="sxs-lookup"><span data-stu-id="c6df8-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="c6df8-121">Tuttavia, di seguito viene illustrato il modo in cui ogni elemento di un quaternione dell'unità è correlato a una rotazione dell'angolo dell'asse (dove q rappresenta un quaternione di unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione di CCW desiderata sull'asse):</span><span class="sxs-lookup"><span data-stu-id="c6df8-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="c6df8-122">I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le [**estensioni D3DXQUATERNION**](d3dxquaternion-extensions.md), che implementano costruttori di overload e operatori di assegnazione, unario e binari (inclusi uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="c6df8-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6df8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6df8-123">Requirements</span></span>



| <span data-ttu-id="c6df8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6df8-124">Requirement</span></span> | <span data-ttu-id="c6df8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c6df8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6df8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6df8-126">Header</span></span><br/> | <dl> <span data-ttu-id="c6df8-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6df8-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6df8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6df8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6df8-129">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c6df8-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="c6df8-130">Vettori, vertici e quaternioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c6df8-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
