---
title: 'Funzione Texture2D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2D:: GetDimensions'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995629"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="2ff4e-105">Funzione Texture2D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="2ff4e-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="2ff4e-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ff4e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff4e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ff4e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="2ff4e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ff4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff4e-109">*MipLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ff4e-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff4e-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ff4e-110">Type: **uint**</span></span>

<span data-ttu-id="2ff4e-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ff4e-111">Optional.</span></span> <span data-ttu-id="2ff4e-112">Il livello mipmap (deve essere specificato se si usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="2ff4e-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="2ff4e-113">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ff4e-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff4e-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ff4e-114">Type: **uint**</span></span>

<span data-ttu-id="2ff4e-115">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="2ff4e-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2ff4e-116">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ff4e-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff4e-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ff4e-117">Type: **uint**</span></span>

<span data-ttu-id="2ff4e-118">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="2ff4e-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2ff4e-119">*NumberOfLevels* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ff4e-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff4e-120">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ff4e-120">Type: **uint**</span></span>

<span data-ttu-id="2ff4e-121">Il numero di livelli di mipmap (richiede anche *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="2ff4e-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff4e-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ff4e-122">Return value</span></span>

<span data-ttu-id="2ff4e-123">Nothing</span><span class="sxs-lookup"><span data-stu-id="2ff4e-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff4e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ff4e-124">Remarks</span></span>

<span data-ttu-id="2ff4e-125">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2ff4e-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="2ff4e-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ff4e-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2ff4e-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="2ff4e-127">Vertex</span></span> | <span data-ttu-id="2ff4e-128">Hull</span><span class="sxs-lookup"><span data-stu-id="2ff4e-128">Hull</span></span> | <span data-ttu-id="2ff4e-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="2ff4e-129">Domain</span></span> | <span data-ttu-id="2ff4e-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="2ff4e-130">Geometry</span></span> | <span data-ttu-id="2ff4e-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="2ff4e-131">Pixel</span></span> | <span data-ttu-id="2ff4e-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2ff4e-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2ff4e-133">x</span><span class="sxs-lookup"><span data-stu-id="2ff4e-133">x</span></span>     | <span data-ttu-id="2ff4e-134">x</span><span class="sxs-lookup"><span data-stu-id="2ff4e-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2ff4e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ff4e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff4e-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2ff4e-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="2ff4e-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2ff4e-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




