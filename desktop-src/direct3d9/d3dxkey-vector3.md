---
description: Descrive una chiave vettoriale da utilizzare nell'animazione con fotogramma chiave. Specifica un vettore in un determinato momento. Viene utilizzato per le chiavi di scala e di conversione.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Struttura D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322641"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="68141-105">\_Struttura D3DXKEY VECTOR3</span><span class="sxs-lookup"><span data-stu-id="68141-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="68141-106">Descrive una chiave vettoriale da utilizzare nell'animazione con fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="68141-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="68141-107">Specifica un vettore in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="68141-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="68141-108">Viene utilizzato per le chiavi di scala e di conversione.</span><span class="sxs-lookup"><span data-stu-id="68141-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="68141-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68141-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="68141-110">Members</span><span class="sxs-lookup"><span data-stu-id="68141-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="68141-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="68141-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="68141-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68141-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="68141-113">Timestamp del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="68141-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="68141-114">**Valore**</span><span class="sxs-lookup"><span data-stu-id="68141-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="68141-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="68141-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="68141-116">Vettore 3D [**D3DXVECTOR3**](d3dxvector3.md) che fornisce valori di scala e/o di conversione.</span><span class="sxs-lookup"><span data-stu-id="68141-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68141-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68141-117">Requirements</span></span>



| <span data-ttu-id="68141-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68141-118">Requirement</span></span> | <span data-ttu-id="68141-119">Valore</span><span class="sxs-lookup"><span data-stu-id="68141-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68141-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68141-120">Header</span></span><br/> | <dl> <span data-ttu-id="68141-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="68141-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68141-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68141-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68141-123">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="68141-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
