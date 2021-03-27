---
title: EvaluateAttributeAtSample (funzione)
description: Valuta in corrispondenza della posizione di esempio indicizzata.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Funzione EvaluateAttributeAtSample HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718142"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="9b54e-104">EvaluateAttributeAtSample (funzione)</span><span class="sxs-lookup"><span data-stu-id="9b54e-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="9b54e-105">Valuta in corrispondenza della posizione di esempio indicizzata.</span><span class="sxs-lookup"><span data-stu-id="9b54e-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b54e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b54e-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="9b54e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b54e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b54e-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9b54e-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b54e-109">Tipo: formato **numerico attrib**</span><span class="sxs-lookup"><span data-stu-id="9b54e-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="9b54e-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="9b54e-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="9b54e-111">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b54e-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b54e-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b54e-112">Type: **uint**</span></span>

<span data-ttu-id="9b54e-113">Percorso di esempio.</span><span class="sxs-lookup"><span data-stu-id="9b54e-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b54e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b54e-114">Remarks</span></span>

<span data-ttu-id="9b54e-115">La modalità di interpolazione può essere **lineare** o **lineare \_ senza alcuna \_ prospettiva** sulla variabile.</span><span class="sxs-lookup"><span data-stu-id="9b54e-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="9b54e-116">L'uso **di centro** o **campione** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9b54e-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="9b54e-117">Sono consentiti anche gli attributi con interpolazione costante. in questo caso, l'indice di esempio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9b54e-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9b54e-118">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9b54e-118">Minimum Shader Model</span></span>

<span data-ttu-id="9b54e-119">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9b54e-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9b54e-120">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9b54e-120">Shader Model</span></span>                                                                | <span data-ttu-id="9b54e-121">Supportato</span><span class="sxs-lookup"><span data-stu-id="9b54e-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9b54e-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="9b54e-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9b54e-123">sì</span><span class="sxs-lookup"><span data-stu-id="9b54e-123">yes</span></span>       |



 

<span data-ttu-id="9b54e-124">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b54e-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9b54e-125">Vertice</span><span class="sxs-lookup"><span data-stu-id="9b54e-125">Vertex</span></span> | <span data-ttu-id="9b54e-126">Hull</span><span class="sxs-lookup"><span data-stu-id="9b54e-126">Hull</span></span> | <span data-ttu-id="9b54e-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="9b54e-127">Domain</span></span> | <span data-ttu-id="9b54e-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="9b54e-128">Geometry</span></span> | <span data-ttu-id="9b54e-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="9b54e-129">Pixel</span></span> | <span data-ttu-id="9b54e-130">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9b54e-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9b54e-131">x</span><span class="sxs-lookup"><span data-stu-id="9b54e-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="9b54e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b54e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b54e-133">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="9b54e-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9b54e-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9b54e-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




