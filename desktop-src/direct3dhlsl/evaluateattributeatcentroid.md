---
title: EvaluateAttributeAtCentroid (funzione)
description: Restituisce il baricentro del pixel.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Funzione EvaluateAttributeAtCentroid HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397726"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="c992b-104">EvaluateAttributeAtCentroid (funzione)</span><span class="sxs-lookup"><span data-stu-id="c992b-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="c992b-105">Restituisce il baricentro del pixel.</span><span class="sxs-lookup"><span data-stu-id="c992b-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="c992b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c992b-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="c992b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c992b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c992b-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c992b-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c992b-109">Tipo: formato **numerico attrib**</span><span class="sxs-lookup"><span data-stu-id="c992b-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="c992b-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="c992b-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c992b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c992b-111">Remarks</span></span>

<span data-ttu-id="c992b-112">La modalità di interpolazione può essere **lineare** o **lineare \_ senza alcuna \_ prospettiva** sulla variabile.</span><span class="sxs-lookup"><span data-stu-id="c992b-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="c992b-113">L'uso **di centro** o **campione** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c992b-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="c992b-114">Sono consentiti anche gli attributi con interpolazione costante. in questo caso, l'indice di esempio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c992b-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c992b-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c992b-115">Minimum Shader Model</span></span>

<span data-ttu-id="c992b-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c992b-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c992b-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c992b-117">Shader Model</span></span>                                                                | <span data-ttu-id="c992b-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="c992b-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c992b-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="c992b-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c992b-120">sì</span><span class="sxs-lookup"><span data-stu-id="c992b-120">yes</span></span>       |



 

<span data-ttu-id="c992b-121">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c992b-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c992b-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="c992b-122">Vertex</span></span> | <span data-ttu-id="c992b-123">Hull</span><span class="sxs-lookup"><span data-stu-id="c992b-123">Hull</span></span> | <span data-ttu-id="c992b-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="c992b-124">Domain</span></span> | <span data-ttu-id="c992b-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="c992b-125">Geometry</span></span> | <span data-ttu-id="c992b-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="c992b-126">Pixel</span></span> | <span data-ttu-id="c992b-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c992b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c992b-128">x</span><span class="sxs-lookup"><span data-stu-id="c992b-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="c992b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c992b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c992b-130">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="c992b-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c992b-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c992b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




