---
title: 'Funzione Texture2DArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2DArray:: GetDimensions'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981071"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="3ca67-105">Funzione Texture2DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="3ca67-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="3ca67-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ca67-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ca67-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="3ca67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ca67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca67-109">*MipLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ca67-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca67-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ca67-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ca67-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3ca67-111">Optional.</span></span> <span data-ttu-id="3ca67-112">Il livello mipmap (deve essere specificato se si usa *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="3ca67-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="3ca67-113">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ca67-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca67-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ca67-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ca67-115">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="3ca67-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3ca67-116">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ca67-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca67-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ca67-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ca67-118">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="3ca67-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3ca67-119">*Elementi* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3ca67-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca67-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ca67-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ca67-121">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3ca67-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3ca67-122">*NumberOfLevels* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ca67-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca67-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ca67-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ca67-124">Il numero di livelli di mipmap (richiede anche *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="3ca67-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca67-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ca67-125">Return value</span></span>

<span data-ttu-id="3ca67-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="3ca67-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca67-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ca67-127">Remarks</span></span>

<span data-ttu-id="3ca67-128">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3ca67-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="3ca67-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ca67-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3ca67-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="3ca67-130">Vertex</span></span> | <span data-ttu-id="3ca67-131">Hull</span><span class="sxs-lookup"><span data-stu-id="3ca67-131">Hull</span></span> | <span data-ttu-id="3ca67-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="3ca67-132">Domain</span></span> | <span data-ttu-id="3ca67-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="3ca67-133">Geometry</span></span> | <span data-ttu-id="3ca67-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="3ca67-134">Pixel</span></span> | <span data-ttu-id="3ca67-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3ca67-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3ca67-136">x</span><span class="sxs-lookup"><span data-stu-id="3ca67-136">x</span></span>     | <span data-ttu-id="3ca67-137">x</span><span class="sxs-lookup"><span data-stu-id="3ca67-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3ca67-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ca67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca67-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3ca67-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="3ca67-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3ca67-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
