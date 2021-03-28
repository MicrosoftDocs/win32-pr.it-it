---
title: 'Funzione Texture2DMS:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2DMS:: GetDimensions'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
keywords:
- Funzione GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969135"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="e3c34-105">Funzione Texture2DMS:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="e3c34-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="e3c34-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3c34-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c34-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3c34-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="e3c34-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3c34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c34-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3c34-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c34-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3c34-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3c34-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="e3c34-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e3c34-112">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3c34-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c34-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3c34-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3c34-114">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="e3c34-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e3c34-115">*NumberOfSamples* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3c34-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c34-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3c34-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3c34-117">Il numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="e3c34-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c34-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3c34-118">Return value</span></span>

<span data-ttu-id="e3c34-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e3c34-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c34-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3c34-120">Remarks</span></span>

<span data-ttu-id="e3c34-121">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e3c34-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="e3c34-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3c34-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e3c34-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="e3c34-123">Vertex</span></span> | <span data-ttu-id="e3c34-124">Hull</span><span class="sxs-lookup"><span data-stu-id="e3c34-124">Hull</span></span> | <span data-ttu-id="e3c34-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="e3c34-125">Domain</span></span> | <span data-ttu-id="e3c34-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="e3c34-126">Geometry</span></span> | <span data-ttu-id="e3c34-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="e3c34-127">Pixel</span></span> | <span data-ttu-id="e3c34-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e3c34-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e3c34-129">x</span><span class="sxs-lookup"><span data-stu-id="e3c34-129">x</span></span>     | <span data-ttu-id="e3c34-130">x</span><span class="sxs-lookup"><span data-stu-id="e3c34-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e3c34-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3c34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c34-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="e3c34-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="e3c34-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e3c34-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
