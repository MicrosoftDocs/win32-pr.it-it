---
title: 'Funzione Texture1D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture1D:: GetDimensions'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530708"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="87fbd-105">Funzione Texture1D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="87fbd-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="87fbd-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="87fbd-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fbd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87fbd-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="87fbd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87fbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87fbd-109">*MipLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87fbd-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87fbd-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87fbd-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87fbd-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87fbd-111">Optional.</span></span> <span data-ttu-id="87fbd-112">Livello mipmap (deve essere specificato se viene usato *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="87fbd-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="87fbd-113">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87fbd-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87fbd-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87fbd-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87fbd-115">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="87fbd-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="87fbd-116">*NumberOfLevels* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87fbd-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87fbd-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87fbd-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87fbd-118">Il numero di livelli di mipmap (richiede anche *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="87fbd-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87fbd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87fbd-119">Return value</span></span>

<span data-ttu-id="87fbd-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="87fbd-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87fbd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="87fbd-121">Remarks</span></span>

<span data-ttu-id="87fbd-122">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="87fbd-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="87fbd-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="87fbd-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="87fbd-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="87fbd-124">Vertex</span></span> | <span data-ttu-id="87fbd-125">Hull</span><span class="sxs-lookup"><span data-stu-id="87fbd-125">Hull</span></span> | <span data-ttu-id="87fbd-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="87fbd-126">Domain</span></span> | <span data-ttu-id="87fbd-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="87fbd-127">Geometry</span></span> | <span data-ttu-id="87fbd-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="87fbd-128">Pixel</span></span> | <span data-ttu-id="87fbd-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="87fbd-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="87fbd-130">x</span><span class="sxs-lookup"><span data-stu-id="87fbd-130">x</span></span>     | <span data-ttu-id="87fbd-131">x</span><span class="sxs-lookup"><span data-stu-id="87fbd-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="87fbd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87fbd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fbd-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="87fbd-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="87fbd-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="87fbd-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
