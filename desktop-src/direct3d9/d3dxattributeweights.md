---
description: 'Struttura D3DXATTRIBUTEWEIGHTS: specifica gli attributi del peso della mesh.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Struttura D3DXATTRIBUTEWEIGHTS (D3dx9mesh.h)
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
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115969"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="e4a04-103">Struttura D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="e4a04-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="e4a04-104">Specifica gli attributi del peso della mesh.</span><span class="sxs-lookup"><span data-stu-id="e4a04-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4a04-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="e4a04-106">Members</span><span class="sxs-lookup"><span data-stu-id="e4a04-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4a04-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="e4a04-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-109">Posizione.</span><span class="sxs-lookup"><span data-stu-id="e4a04-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="e4a04-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-112">Spessore della blend.</span><span class="sxs-lookup"><span data-stu-id="e4a04-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="e4a04-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-115">Normale.</span><span class="sxs-lookup"><span data-stu-id="e4a04-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-116">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="e4a04-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-118">Valore di illuminazione diffusa.</span><span class="sxs-lookup"><span data-stu-id="e4a04-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="e4a04-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-121">Valore di illuminazione speculare.</span><span class="sxs-lookup"><span data-stu-id="e4a04-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="e4a04-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-124">Otto coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="e4a04-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="e4a04-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="e4a04-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="e4a04-128">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="e4a04-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="e4a04-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a04-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e4a04-130">Binormale.</span><span class="sxs-lookup"><span data-stu-id="e4a04-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4a04-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4a04-131">Remarks</span></span>

<span data-ttu-id="e4a04-132">Questa struttura descrive in che modo un'operazione di semplificazione considererà i dati dei vertici durante il calcolo dei costi relativi tra gli bordi che comprimono.</span><span class="sxs-lookup"><span data-stu-id="e4a04-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="e4a04-133">Ad esempio, se il campo Normale è 0,0, l'operazione di semplificazione ignorerà il componente normale del vertice durante il calcolo dell'errore per la compressione.</span><span class="sxs-lookup"><span data-stu-id="e4a04-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="e4a04-134">Tuttavia, se il campo Normal è 1.0, l'operazione di semplificazione userà il componente normale del vertice.</span><span class="sxs-lookup"><span data-stu-id="e4a04-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="e4a04-135">Se il campo Normale è 2,0, raddoppiare la quantità di errori. se il campo Normal è 4.0, quadruplicare il numero di errori e così via.</span><span class="sxs-lookup"><span data-stu-id="e4a04-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="e4a04-136">Il tipo LPD3DXATTRIBUTEWEIGHTS è definito come puntatore alla **struttura D3DXATTRIBUTEWEIGHTS.**</span><span class="sxs-lookup"><span data-stu-id="e4a04-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="e4a04-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4a04-137">Requirements</span></span>



| <span data-ttu-id="e4a04-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a04-138">Requirement</span></span> | <span data-ttu-id="e4a04-139">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a04-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a04-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4a04-140">Header</span></span><br/> | <dl> <span data-ttu-id="e4a04-141"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a04-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4a04-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4a04-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a04-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="e4a04-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e4a04-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="e4a04-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
