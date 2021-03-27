---
title: ProcessIsolineTessFactors (funzione)
description: Genera i fattori a mosaico arrotondati per un oggetto oline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Funzione ProcessIsolineTessFactors HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718820"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="fba86-104">ProcessIsolineTessFactors (funzione)</span><span class="sxs-lookup"><span data-stu-id="fba86-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="fba86-105">Genera i fattori a mosaico arrotondati per un oggetto oline.</span><span class="sxs-lookup"><span data-stu-id="fba86-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba86-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fba86-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="fba86-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fba86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba86-108">*RawDetailFactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fba86-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba86-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fba86-109">Type: **float**</span></span>

<span data-ttu-id="fba86-110">Fattore di dettaglio desiderato.</span><span class="sxs-lookup"><span data-stu-id="fba86-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="fba86-111">*RawDensityFactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fba86-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba86-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fba86-112">Type: **float**</span></span>

<span data-ttu-id="fba86-113">Fattore di densità desiderato.</span><span class="sxs-lookup"><span data-stu-id="fba86-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="fba86-114">*RoundedDetailFactor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fba86-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba86-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fba86-115">Type: **float**</span></span>

<span data-ttu-id="fba86-116">Il fattore di dettaglio arrotondato è stato fissato a un intervallo che può essere utilizzato da mosaico.</span><span class="sxs-lookup"><span data-stu-id="fba86-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="fba86-117">*RoundedDensityFactor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fba86-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba86-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fba86-118">Type: **float**</span></span>

<span data-ttu-id="fba86-119">Il fattore di densità arrotondato fissato a un rangethat può essere utilizzato da mosaico.</span><span class="sxs-lookup"><span data-stu-id="fba86-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba86-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fba86-120">Return value</span></span>

<span data-ttu-id="fba86-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fba86-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba86-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fba86-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="fba86-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="fba86-123">Minimum Shader Model</span></span>

<span data-ttu-id="fba86-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="fba86-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fba86-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fba86-125">Shader Model</span></span>                                                                | <span data-ttu-id="fba86-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="fba86-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fba86-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="fba86-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fba86-128">sì</span><span class="sxs-lookup"><span data-stu-id="fba86-128">yes</span></span>       |



 

<span data-ttu-id="fba86-129">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fba86-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fba86-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="fba86-130">Vertex</span></span> | <span data-ttu-id="fba86-131">Hull</span><span class="sxs-lookup"><span data-stu-id="fba86-131">Hull</span></span> | <span data-ttu-id="fba86-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="fba86-132">Domain</span></span> | <span data-ttu-id="fba86-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="fba86-133">Geometry</span></span> | <span data-ttu-id="fba86-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="fba86-134">Pixel</span></span> | <span data-ttu-id="fba86-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fba86-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="fba86-136">x</span><span class="sxs-lookup"><span data-stu-id="fba86-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="fba86-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fba86-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba86-138">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="fba86-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="fba86-139">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fba86-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




