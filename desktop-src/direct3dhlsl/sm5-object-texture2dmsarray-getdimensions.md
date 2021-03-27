---
title: 'Funzione Texture2DMSArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2DMSArray:: GetDimensions'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353721"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="3031f-105">Funzione Texture2DMSArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="3031f-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="3031f-106">Restituisce le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3031f-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3031f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3031f-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="3031f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3031f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3031f-109">*Larghezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3031f-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3031f-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3031f-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3031f-111">Larghezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="3031f-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3031f-112">*Altezza* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3031f-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3031f-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3031f-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3031f-114">Altezza della risorsa, in Texel.</span><span class="sxs-lookup"><span data-stu-id="3031f-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3031f-115">*Elementi* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3031f-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3031f-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3031f-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3031f-117">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3031f-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3031f-118">*NumberOfSamples* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3031f-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3031f-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3031f-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3031f-120">Il numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="3031f-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3031f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3031f-121">Return value</span></span>

<span data-ttu-id="3031f-122">Nothing</span><span class="sxs-lookup"><span data-stu-id="3031f-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="3031f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3031f-123">Remarks</span></span>

<span data-ttu-id="3031f-124">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3031f-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="3031f-125">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3031f-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3031f-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="3031f-126">Vertex</span></span> | <span data-ttu-id="3031f-127">Hull</span><span class="sxs-lookup"><span data-stu-id="3031f-127">Hull</span></span> | <span data-ttu-id="3031f-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="3031f-128">Domain</span></span> | <span data-ttu-id="3031f-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="3031f-129">Geometry</span></span> | <span data-ttu-id="3031f-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="3031f-130">Pixel</span></span> | <span data-ttu-id="3031f-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3031f-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3031f-132">x</span><span class="sxs-lookup"><span data-stu-id="3031f-132">x</span></span>     | <span data-ttu-id="3031f-133">x</span><span class="sxs-lookup"><span data-stu-id="3031f-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3031f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3031f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3031f-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3031f-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="3031f-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3031f-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
