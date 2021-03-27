---
title: 'Funzione Texture3D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture3D:: GetDimensions'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995753"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="dea70-105">Funzione Texture3D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="dea70-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="dea70-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dea70-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dea70-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="dea70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dea70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea70-109">*MipLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dea70-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea70-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dea70-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dea70-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dea70-111">Optional.</span></span> <span data-ttu-id="dea70-112">Livello mipmap (deve essere specificato se viene usato *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="dea70-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="dea70-113">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dea70-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea70-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dea70-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dea70-115">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="dea70-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="dea70-116">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dea70-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea70-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dea70-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dea70-118">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="dea70-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="dea70-119">*Profondità* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dea70-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea70-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dea70-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dea70-121">Profondità della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="dea70-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="dea70-122">*NumberOfLevels* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dea70-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea70-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dea70-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dea70-124">Il numero di livelli di mipmap (richiede anche *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="dea70-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea70-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dea70-125">Return value</span></span>

<span data-ttu-id="dea70-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="dea70-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="dea70-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dea70-127">Remarks</span></span>

<span data-ttu-id="dea70-128">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="dea70-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="dea70-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dea70-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dea70-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="dea70-130">Vertex</span></span> | <span data-ttu-id="dea70-131">Hull</span><span class="sxs-lookup"><span data-stu-id="dea70-131">Hull</span></span> | <span data-ttu-id="dea70-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="dea70-132">Domain</span></span> | <span data-ttu-id="dea70-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="dea70-133">Geometry</span></span> | <span data-ttu-id="dea70-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="dea70-134">Pixel</span></span> | <span data-ttu-id="dea70-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dea70-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dea70-136">x</span><span class="sxs-lookup"><span data-stu-id="dea70-136">x</span></span>     | <span data-ttu-id="dea70-137">x</span><span class="sxs-lookup"><span data-stu-id="dea70-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dea70-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dea70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea70-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="dea70-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="dea70-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dea70-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
