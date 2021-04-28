---
description: 'Struttura D3DXQUATERNION (D3dx9math.h): descrive un quaternione.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Struttura D3DXQUATERNION (D3dx9math.h)
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115679"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="bd92d-103">Struttura D3DXQUATERNION (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bd92d-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="bd92d-104">Descrive un quaternione.</span><span class="sxs-lookup"><span data-stu-id="bd92d-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd92d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd92d-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="bd92d-106">Members</span><span class="sxs-lookup"><span data-stu-id="bd92d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd92d-107">**x**</span><span class="sxs-lookup"><span data-stu-id="bd92d-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="bd92d-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd92d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bd92d-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="bd92d-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="bd92d-110">**y**</span><span class="sxs-lookup"><span data-stu-id="bd92d-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="bd92d-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd92d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bd92d-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="bd92d-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="bd92d-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="bd92d-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="bd92d-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd92d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bd92d-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="bd92d-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="bd92d-116">**w**</span><span class="sxs-lookup"><span data-stu-id="bd92d-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="bd92d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd92d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bd92d-118">Componente w.</span><span class="sxs-lookup"><span data-stu-id="bd92d-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd92d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd92d-119">Remarks</span></span>

<span data-ttu-id="bd92d-120">I quaternioni aggiungono un quarto elemento ai valori x, y, z che definiscono un vettore, con conseguente vettori \[ \] 4D arbitrari.</span><span class="sxs-lookup"><span data-stu-id="bd92d-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="bd92d-121">Tuttavia, l'esempio seguente illustra come ogni elemento di un quaternione di unità è correlato a una rotazione asse-angolo (dove q rappresenta un quaternione unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione CCW desiderata intorno all'asse:</span><span class="sxs-lookup"><span data-stu-id="bd92d-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="bd92d-122">I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXQUATERNION**](d3dxquaternion-extensions.md), che implementano costruttori di overload e operatori di assegnazione, unario e binario (inclusa l'uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="bd92d-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd92d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd92d-123">Requirements</span></span>



| <span data-ttu-id="bd92d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd92d-124">Requirement</span></span> | <span data-ttu-id="bd92d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bd92d-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd92d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd92d-126">Header</span></span><br/> | <dl> <span data-ttu-id="bd92d-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd92d-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd92d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd92d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd92d-129">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="bd92d-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="bd92d-130">Vettori, vertici e quaternioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd92d-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
