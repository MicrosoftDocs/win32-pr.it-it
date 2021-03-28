---
title: 'Texture1D:: MIPS. Funzione operator'
description: Restituisce una variabile di risorsa di sola lettura o un Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
keywords:
- MIPS. Funzione operator HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340232"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="6d1c9-104">Texture1D:: MIPS. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="6d1c9-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="6d1c9-105">Restituisce una variabile di risorsa di sola lettura o un [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="6d1c9-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1c9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d1c9-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="6d1c9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d1c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d1c9-108">*mipSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d1c9-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1c9-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6d1c9-109">Type: **uint**</span></span>

<span data-ttu-id="6d1c9-110">Indice della sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="6d1c9-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="6d1c9-111">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d1c9-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1c9-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6d1c9-112">Type: **uint**</span></span>

<span data-ttu-id="6d1c9-113">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="6d1c9-113">The index position.</span></span> <span data-ttu-id="6d1c9-114">Contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="6d1c9-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d1c9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d1c9-115">Return value</span></span>

<span data-ttu-id="6d1c9-116">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6d1c9-116">Type: **R**</span></span>

<span data-ttu-id="6d1c9-117">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d1c9-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d1c9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d1c9-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="6d1c9-119">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="6d1c9-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="6d1c9-120">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d1c9-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6d1c9-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="6d1c9-121">Vertex</span></span> | <span data-ttu-id="6d1c9-122">Hull</span><span class="sxs-lookup"><span data-stu-id="6d1c9-122">Hull</span></span> | <span data-ttu-id="6d1c9-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="6d1c9-123">Domain</span></span> | <span data-ttu-id="6d1c9-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="6d1c9-124">Geometry</span></span> | <span data-ttu-id="6d1c9-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d1c9-125">Pixel</span></span> | <span data-ttu-id="6d1c9-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6d1c9-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d1c9-127">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-127">x</span></span>      | <span data-ttu-id="6d1c9-128">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-128">x</span></span>    | <span data-ttu-id="6d1c9-129">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-129">x</span></span>      | <span data-ttu-id="6d1c9-130">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-130">x</span></span>        | <span data-ttu-id="6d1c9-131">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-131">x</span></span>     | <span data-ttu-id="6d1c9-132">x</span><span class="sxs-lookup"><span data-stu-id="6d1c9-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6d1c9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d1c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1c9-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6d1c9-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="6d1c9-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6d1c9-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




