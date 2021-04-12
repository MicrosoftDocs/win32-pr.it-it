---
description: Specifica gli attributi di peso mesh.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Struttura D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355109"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="7a44e-103">\_ \_ Struttura weights dell'attributo d3dx10</span><span class="sxs-lookup"><span data-stu-id="7a44e-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="7a44e-104">Specifica gli attributi di peso mesh.</span><span class="sxs-lookup"><span data-stu-id="7a44e-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a44e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a44e-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="7a44e-106">Members</span><span class="sxs-lookup"><span data-stu-id="7a44e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a44e-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="7a44e-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-109">Posizione.</span><span class="sxs-lookup"><span data-stu-id="7a44e-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="7a44e-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-112">Spessore di Blend.</span><span class="sxs-lookup"><span data-stu-id="7a44e-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="7a44e-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-115">Normale.</span><span class="sxs-lookup"><span data-stu-id="7a44e-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-116">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="7a44e-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-118">Valore di illuminazione diffuso.</span><span class="sxs-lookup"><span data-stu-id="7a44e-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="7a44e-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-121">Valore di illuminazione speculare.</span><span class="sxs-lookup"><span data-stu-id="7a44e-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="7a44e-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-124">Otto coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7a44e-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="7a44e-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="7a44e-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="7a44e-128">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="7a44e-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="7a44e-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a44e-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a44e-130">Binormale.</span><span class="sxs-lookup"><span data-stu-id="7a44e-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a44e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a44e-131">Remarks</span></span>

<span data-ttu-id="7a44e-132">Questa struttura descrive il modo in cui un'operazione di semplificazione considererà i dati dei vertici quando si calcolano i costi relativi tra i bordi.</span><span class="sxs-lookup"><span data-stu-id="7a44e-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="7a44e-133">Se, ad esempio, il campo normale è 0,0, l'operazione di semplificazione ignorerà il componente normale vertice durante il calcolo dell'errore per la compressione.</span><span class="sxs-lookup"><span data-stu-id="7a44e-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="7a44e-134">Tuttavia, se il campo normale è 1,0, l'operazione di semplificazione utilizzerà il componente normale vertice.</span><span class="sxs-lookup"><span data-stu-id="7a44e-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="7a44e-135">Se il campo normale è 2,0, raddoppiare la quantità di errori; Se il campo normale è 4,0, moltiplicare il numero di errori e così via.</span><span class="sxs-lookup"><span data-stu-id="7a44e-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="7a44e-136">Il \_ \_ tipo di ponderazione dell'attributo LPD3DX è definito come un puntatore alla \_ struttura dell'attributo D3DX \_ weights.</span><span class="sxs-lookup"><span data-stu-id="7a44e-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="7a44e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a44e-137">Requirements</span></span>



| <span data-ttu-id="7a44e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a44e-138">Requirement</span></span> | <span data-ttu-id="7a44e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="7a44e-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7a44e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a44e-140">Header</span></span><br/> | <dl> <span data-ttu-id="7a44e-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a44e-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a44e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a44e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a44e-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="7a44e-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
