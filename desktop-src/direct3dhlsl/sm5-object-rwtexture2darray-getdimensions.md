---
title: 'Funzione RWTexture2DArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture2DArray:: GetDimensions'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
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
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234622"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="fceab-105">Funzione RWTexture2DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="fceab-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="fceab-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fceab-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fceab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fceab-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="fceab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fceab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fceab-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fceab-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fceab-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fceab-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fceab-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="fceab-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="fceab-112">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fceab-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fceab-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fceab-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fceab-114">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="fceab-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="fceab-115">*Elementi* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fceab-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fceab-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fceab-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fceab-117">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fceab-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fceab-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fceab-118">Return value</span></span>

<span data-ttu-id="fceab-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fceab-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fceab-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fceab-120">Remarks</span></span>

<span data-ttu-id="fceab-121">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fceab-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="fceab-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fceab-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fceab-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="fceab-123">Vertex</span></span> | <span data-ttu-id="fceab-124">Hull</span><span class="sxs-lookup"><span data-stu-id="fceab-124">Hull</span></span> | <span data-ttu-id="fceab-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="fceab-125">Domain</span></span> | <span data-ttu-id="fceab-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="fceab-126">Geometry</span></span> | <span data-ttu-id="fceab-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="fceab-127">Pixel</span></span> | <span data-ttu-id="fceab-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fceab-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fceab-129">x</span><span class="sxs-lookup"><span data-stu-id="fceab-129">x</span></span>     | <span data-ttu-id="fceab-130">x</span><span class="sxs-lookup"><span data-stu-id="fceab-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fceab-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fceab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fceab-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="fceab-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="fceab-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fceab-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
