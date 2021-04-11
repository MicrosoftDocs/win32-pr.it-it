---
description: Descrive una chiave Quaternion per l'uso nell'animazione con fotogramma chiave. Una chiave Quaternion è un valore quaternione in un determinato momento.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Struttura D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354809"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="c7ee4-104">\_Struttura QUATERNION D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="c7ee4-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="c7ee4-105">Descrive una chiave Quaternion per l'uso nell'animazione con fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="c7ee4-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="c7ee4-106">Una chiave Quaternion è un valore quaternione in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="c7ee4-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ee4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7ee4-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="c7ee4-108">Members</span><span class="sxs-lookup"><span data-stu-id="c7ee4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7ee4-109">**Time**</span><span class="sxs-lookup"><span data-stu-id="c7ee4-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="c7ee4-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7ee4-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7ee4-111">Valore temporale.</span><span class="sxs-lookup"><span data-stu-id="c7ee4-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="c7ee4-112">**Valore**</span><span class="sxs-lookup"><span data-stu-id="c7ee4-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c7ee4-113">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="c7ee4-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7ee4-114">Quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che fornisce valori di rotazione.</span><span class="sxs-lookup"><span data-stu-id="c7ee4-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7ee4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7ee4-115">Requirements</span></span>



| <span data-ttu-id="c7ee4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ee4-116">Requirement</span></span> | <span data-ttu-id="c7ee4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c7ee4-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ee4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7ee4-118">Header</span></span><br/> | <dl> <span data-ttu-id="c7ee4-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ee4-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ee4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7ee4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ee4-121">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c7ee4-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
