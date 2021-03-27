---
title: 'Funzione RWTexture2D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture2D:: GetDimensions'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132263"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="7cd5c-105">Funzione RWTexture2D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="7cd5c-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="7cd5c-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7cd5c-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd5c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cd5c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="7cd5c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cd5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd5c-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7cd5c-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd5c-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7cd5c-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7cd5c-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="7cd5c-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="7cd5c-112">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7cd5c-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd5c-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7cd5c-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7cd5c-114">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="7cd5c-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd5c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cd5c-115">Return value</span></span>

<span data-ttu-id="7cd5c-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7cd5c-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd5c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cd5c-117">Remarks</span></span>

<span data-ttu-id="7cd5c-118">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7cd5c-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="7cd5c-119">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cd5c-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7cd5c-120">Vertice</span><span class="sxs-lookup"><span data-stu-id="7cd5c-120">Vertex</span></span> | <span data-ttu-id="7cd5c-121">Hull</span><span class="sxs-lookup"><span data-stu-id="7cd5c-121">Hull</span></span> | <span data-ttu-id="7cd5c-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="7cd5c-122">Domain</span></span> | <span data-ttu-id="7cd5c-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="7cd5c-123">Geometry</span></span> | <span data-ttu-id="7cd5c-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="7cd5c-124">Pixel</span></span> | <span data-ttu-id="7cd5c-125">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7cd5c-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7cd5c-126">x</span><span class="sxs-lookup"><span data-stu-id="7cd5c-126">x</span></span>     | <span data-ttu-id="7cd5c-127">x</span><span class="sxs-lookup"><span data-stu-id="7cd5c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7cd5c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cd5c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd5c-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="7cd5c-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="7cd5c-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7cd5c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
