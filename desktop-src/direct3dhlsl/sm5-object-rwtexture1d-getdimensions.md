---
title: 'Funzione RWTexture1D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture1D:: GetDimensions'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981079"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="4886e-105">Funzione RWTexture1D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="4886e-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="4886e-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4886e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4886e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4886e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="4886e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4886e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4886e-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4886e-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4886e-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4886e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4886e-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="4886e-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4886e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4886e-112">Return value</span></span>

<span data-ttu-id="4886e-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="4886e-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="4886e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4886e-114">Remarks</span></span>

<span data-ttu-id="4886e-115">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4886e-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="4886e-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4886e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4886e-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="4886e-117">Vertex</span></span> | <span data-ttu-id="4886e-118">Hull</span><span class="sxs-lookup"><span data-stu-id="4886e-118">Hull</span></span> | <span data-ttu-id="4886e-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="4886e-119">Domain</span></span> | <span data-ttu-id="4886e-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="4886e-120">Geometry</span></span> | <span data-ttu-id="4886e-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="4886e-121">Pixel</span></span> | <span data-ttu-id="4886e-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4886e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4886e-123">x</span><span class="sxs-lookup"><span data-stu-id="4886e-123">x</span></span>     | <span data-ttu-id="4886e-124">x</span><span class="sxs-lookup"><span data-stu-id="4886e-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4886e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4886e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4886e-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="4886e-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="4886e-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4886e-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
