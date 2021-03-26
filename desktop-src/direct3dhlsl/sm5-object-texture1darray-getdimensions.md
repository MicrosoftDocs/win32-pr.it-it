---
title: 'Funzione Texture1DArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture1DArray:: GetDimensions'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761764"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="1235c-105">Funzione Texture1DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="1235c-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="1235c-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1235c-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1235c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1235c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="1235c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1235c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1235c-109">*MipLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1235c-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1235c-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1235c-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1235c-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1235c-111">Optional.</span></span> <span data-ttu-id="1235c-112">Livello mipmap (deve essere specificato se viene usato *NumberOfLevels* ).</span><span class="sxs-lookup"><span data-stu-id="1235c-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="1235c-113">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1235c-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1235c-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1235c-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1235c-115">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="1235c-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="1235c-116">*Elementi* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1235c-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1235c-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1235c-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1235c-118">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1235c-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="1235c-119">*NumberOfLevels* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1235c-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1235c-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1235c-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1235c-121">Il numero di livelli di mipmap (richiede anche *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="1235c-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1235c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1235c-122">Return value</span></span>

<span data-ttu-id="1235c-123">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1235c-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1235c-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1235c-124">Remarks</span></span>

<span data-ttu-id="1235c-125">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="1235c-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="1235c-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1235c-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1235c-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="1235c-127">Vertex</span></span> | <span data-ttu-id="1235c-128">Hull</span><span class="sxs-lookup"><span data-stu-id="1235c-128">Hull</span></span> | <span data-ttu-id="1235c-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="1235c-129">Domain</span></span> | <span data-ttu-id="1235c-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="1235c-130">Geometry</span></span> | <span data-ttu-id="1235c-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="1235c-131">Pixel</span></span> | <span data-ttu-id="1235c-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="1235c-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1235c-133">x</span><span class="sxs-lookup"><span data-stu-id="1235c-133">x</span></span>     | <span data-ttu-id="1235c-134">x</span><span class="sxs-lookup"><span data-stu-id="1235c-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1235c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1235c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1235c-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1235c-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="1235c-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="1235c-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
