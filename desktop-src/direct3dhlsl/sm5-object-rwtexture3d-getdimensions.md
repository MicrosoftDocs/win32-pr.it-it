---
title: 'Funzione RWTexture3D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture3D:: GetDimensions'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352966"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="85ad3-105">Funzione RWTexture3D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="85ad3-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="85ad3-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="85ad3-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ad3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85ad3-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="85ad3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="85ad3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ad3-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85ad3-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ad3-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85ad3-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="85ad3-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="85ad3-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="85ad3-112">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85ad3-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ad3-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85ad3-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="85ad3-114">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="85ad3-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="85ad3-115">*Profondità* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85ad3-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ad3-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85ad3-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="85ad3-117">Profondità della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="85ad3-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ad3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85ad3-118">Return value</span></span>

<span data-ttu-id="85ad3-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="85ad3-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ad3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ad3-120">Remarks</span></span>

<span data-ttu-id="85ad3-121">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="85ad3-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="85ad3-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="85ad3-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="85ad3-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="85ad3-123">Vertex</span></span> | <span data-ttu-id="85ad3-124">Hull</span><span class="sxs-lookup"><span data-stu-id="85ad3-124">Hull</span></span> | <span data-ttu-id="85ad3-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="85ad3-125">Domain</span></span> | <span data-ttu-id="85ad3-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="85ad3-126">Geometry</span></span> | <span data-ttu-id="85ad3-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="85ad3-127">Pixel</span></span> | <span data-ttu-id="85ad3-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="85ad3-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="85ad3-129">x</span><span class="sxs-lookup"><span data-stu-id="85ad3-129">x</span></span>     | <span data-ttu-id="85ad3-130">x</span><span class="sxs-lookup"><span data-stu-id="85ad3-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="85ad3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85ad3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ad3-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="85ad3-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="85ad3-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="85ad3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
