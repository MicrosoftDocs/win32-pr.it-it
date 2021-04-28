---
description: 'D3DX10_ATTRIBUTE_WEIGHTS struttura : specifica gli attributi di spessore della mesh.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS (D3DX10.h)
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
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094354"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="c7fd7-103">Struttura WEIGHTS DEGLI ATTRIBUTI D3DX10 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7fd7-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="c7fd7-104">Specifica gli attributi di spessore della mesh.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fd7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7fd7-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="c7fd7-106">Members</span><span class="sxs-lookup"><span data-stu-id="c7fd7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7fd7-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-109">Posizione.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-110">**Limite**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-112">Spessore blend.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-115">Normale.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-116">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-118">Valore di illuminazione diffusa.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-119">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-121">Valore di illuminazione speculare.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-124">Otto coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="c7fd7-128">**Binormale**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="c7fd7-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7fd7-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7fd7-130">Binormale.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7fd7-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7fd7-131">Remarks</span></span>

<span data-ttu-id="c7fd7-132">Questa struttura descrive in che modo un'operazione di semplificazione considererà i dati dei vertici durante il calcolo dei costi relativi tra i bordi di compressione.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="c7fd7-133">Ad esempio, se il campo Normale è 0,0, l'operazione di semplificazione ignorerà il componente normale del vertice durante il calcolo dell'errore per la compressione.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="c7fd7-134">Tuttavia, se il campo Normal è 1.0, l'operazione di semplificazione userà il componente normale dei vertici.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="c7fd7-135">Se il campo Normale è 2.0, raddoppiare la quantità di errori. se il campo Normale è 4.0, quindi quadruplicare il numero di errori e così via.</span><span class="sxs-lookup"><span data-stu-id="c7fd7-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="c7fd7-136">Il tipo WEIGHTS ATTRIBUTE LPD3DX è definito come puntatore alla struttura \_ \_ ATTRIBUTE WEIGHTS D3DX. \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7fd7-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="c7fd7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7fd7-137">Requirements</span></span>



| <span data-ttu-id="c7fd7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fd7-138">Requirement</span></span> | <span data-ttu-id="c7fd7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c7fd7-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fd7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7fd7-140">Header</span></span><br/> | <dl> <span data-ttu-id="c7fd7-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fd7-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fd7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7fd7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fd7-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c7fd7-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
