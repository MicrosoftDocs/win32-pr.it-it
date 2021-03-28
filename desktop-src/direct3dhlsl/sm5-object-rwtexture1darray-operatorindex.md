---
title: 'Funzione RWTexture1DArray:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture1DArray:: operator'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981711"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="2eae2-105">Funzione RWTexture1DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="2eae2-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="2eae2-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2eae2-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eae2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2eae2-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="2eae2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2eae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eae2-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eae2-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eae2-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="2eae2-110">Type: **uint2**</span></span>

<span data-ttu-id="2eae2-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2eae2-111">The index position.</span></span> <span data-ttu-id="2eae2-112">Il primo componente contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="2eae2-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="2eae2-113">Il secondo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="2eae2-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eae2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2eae2-114">Return value</span></span>

<span data-ttu-id="2eae2-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2eae2-115">Type: **R**</span></span>

<span data-ttu-id="2eae2-116">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2eae2-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eae2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2eae2-117">Remarks</span></span>

<span data-ttu-id="2eae2-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2eae2-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2eae2-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="2eae2-119">Vertex</span></span> | <span data-ttu-id="2eae2-120">Hull</span><span class="sxs-lookup"><span data-stu-id="2eae2-120">Hull</span></span> | <span data-ttu-id="2eae2-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="2eae2-121">Domain</span></span> | <span data-ttu-id="2eae2-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="2eae2-122">Geometry</span></span> | <span data-ttu-id="2eae2-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="2eae2-123">Pixel</span></span> | <span data-ttu-id="2eae2-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2eae2-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2eae2-125">x</span><span class="sxs-lookup"><span data-stu-id="2eae2-125">x</span></span>     | <span data-ttu-id="2eae2-126">x</span><span class="sxs-lookup"><span data-stu-id="2eae2-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2eae2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2eae2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eae2-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="2eae2-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="2eae2-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2eae2-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




