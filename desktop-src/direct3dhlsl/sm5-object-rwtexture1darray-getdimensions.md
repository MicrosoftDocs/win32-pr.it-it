---
title: 'Funzione RWTexture1DArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture1DArray:: GetDimensions'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234778"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="7280e-105">Funzione RWTexture1DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="7280e-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="7280e-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7280e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7280e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7280e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="7280e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7280e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7280e-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7280e-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7280e-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7280e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7280e-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="7280e-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7280e-112">*Elementi* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7280e-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7280e-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7280e-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7280e-114">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7280e-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7280e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7280e-115">Return value</span></span>

<span data-ttu-id="7280e-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7280e-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7280e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7280e-117">Remarks</span></span>

<span data-ttu-id="7280e-118">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7280e-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="7280e-119">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7280e-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7280e-120">Vertice</span><span class="sxs-lookup"><span data-stu-id="7280e-120">Vertex</span></span> | <span data-ttu-id="7280e-121">Hull</span><span class="sxs-lookup"><span data-stu-id="7280e-121">Hull</span></span> | <span data-ttu-id="7280e-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="7280e-122">Domain</span></span> | <span data-ttu-id="7280e-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="7280e-123">Geometry</span></span> | <span data-ttu-id="7280e-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="7280e-124">Pixel</span></span> | <span data-ttu-id="7280e-125">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7280e-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7280e-126">x</span><span class="sxs-lookup"><span data-stu-id="7280e-126">x</span></span>     | <span data-ttu-id="7280e-127">x</span><span class="sxs-lookup"><span data-stu-id="7280e-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7280e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7280e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7280e-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="7280e-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="7280e-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7280e-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
