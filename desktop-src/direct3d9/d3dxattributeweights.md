---
description: Specifica gli attributi di peso mesh.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Struttura D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322889"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="fca0f-103">Struttura D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="fca0f-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="fca0f-104">Specifica gli attributi di peso mesh.</span><span class="sxs-lookup"><span data-stu-id="fca0f-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fca0f-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="fca0f-106">Members</span><span class="sxs-lookup"><span data-stu-id="fca0f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fca0f-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="fca0f-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-109">Posizione.</span><span class="sxs-lookup"><span data-stu-id="fca0f-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="fca0f-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-112">Spessore di Blend.</span><span class="sxs-lookup"><span data-stu-id="fca0f-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="fca0f-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-115">Normale.</span><span class="sxs-lookup"><span data-stu-id="fca0f-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-116">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="fca0f-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-118">Valore di illuminazione diffuso.</span><span class="sxs-lookup"><span data-stu-id="fca0f-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="fca0f-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-121">Valore di illuminazione speculare.</span><span class="sxs-lookup"><span data-stu-id="fca0f-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="fca0f-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-124">Otto coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fca0f-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="fca0f-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="fca0f-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="fca0f-128">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="fca0f-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="fca0f-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca0f-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fca0f-130">Binormale.</span><span class="sxs-lookup"><span data-stu-id="fca0f-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fca0f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="fca0f-131">Remarks</span></span>

<span data-ttu-id="fca0f-132">Questa struttura descrive il modo in cui un'operazione di semplificazione considererà i dati dei vertici quando si calcolano i costi relativi tra i bordi.</span><span class="sxs-lookup"><span data-stu-id="fca0f-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="fca0f-133">Se, ad esempio, il campo normale è 0,0, l'operazione di semplificazione ignorerà il componente normale vertice durante il calcolo dell'errore per la compressione.</span><span class="sxs-lookup"><span data-stu-id="fca0f-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="fca0f-134">Tuttavia, se il campo normale è 1,0, l'operazione di semplificazione utilizzerà il componente normale vertice.</span><span class="sxs-lookup"><span data-stu-id="fca0f-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="fca0f-135">Se il campo normale è 2,0, raddoppiare la quantità di errori; Se il campo normale è 4,0, moltiplicare il numero di errori e così via.</span><span class="sxs-lookup"><span data-stu-id="fca0f-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="fca0f-136">Il tipo LPD3DXATTRIBUTEWEIGHTS è definito come un puntatore alla struttura **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="fca0f-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="fca0f-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fca0f-137">Requirements</span></span>



| <span data-ttu-id="fca0f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca0f-138">Requirement</span></span> | <span data-ttu-id="fca0f-139">Valore</span><span class="sxs-lookup"><span data-stu-id="fca0f-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fca0f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fca0f-140">Header</span></span><br/> | <dl> <span data-ttu-id="fca0f-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca0f-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fca0f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fca0f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca0f-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="fca0f-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="fca0f-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="fca0f-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
