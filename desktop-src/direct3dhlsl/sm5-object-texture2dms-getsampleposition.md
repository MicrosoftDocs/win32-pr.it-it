---
title: 'Funzione Texture2DMS:: GetSamplePosition'
description: Restituisce la posizione di esempio per l'indice di esempio fornito.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- Funzione GetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517325"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="f438a-104">Funzione Texture2DMS:: GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="f438a-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="f438a-105">Restituisce la posizione di esempio per l'indice di esempio fornito.</span><span class="sxs-lookup"><span data-stu-id="f438a-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="f438a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f438a-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="f438a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f438a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f438a-108">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f438a-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f438a-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f438a-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f438a-110">Indice in base zero di una posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="f438a-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f438a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f438a-111">Return value</span></span>

<span data-ttu-id="f438a-112">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="f438a-112">Type: **float2**</span></span>

<span data-ttu-id="f438a-113">Percorso di esempio.</span><span class="sxs-lookup"><span data-stu-id="f438a-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="f438a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f438a-114">Remarks</span></span>

<span data-ttu-id="f438a-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f438a-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f438a-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="f438a-116">Vertex</span></span> | <span data-ttu-id="f438a-117">Hull</span><span class="sxs-lookup"><span data-stu-id="f438a-117">Hull</span></span> | <span data-ttu-id="f438a-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="f438a-118">Domain</span></span> | <span data-ttu-id="f438a-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="f438a-119">Geometry</span></span> | <span data-ttu-id="f438a-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="f438a-120">Pixel</span></span> | <span data-ttu-id="f438a-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f438a-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f438a-122">x</span><span class="sxs-lookup"><span data-stu-id="f438a-122">x</span></span>      | <span data-ttu-id="f438a-123">x</span><span class="sxs-lookup"><span data-stu-id="f438a-123">x</span></span>    | <span data-ttu-id="f438a-124">x</span><span class="sxs-lookup"><span data-stu-id="f438a-124">x</span></span>      | <span data-ttu-id="f438a-125">x</span><span class="sxs-lookup"><span data-stu-id="f438a-125">x</span></span>        | <span data-ttu-id="f438a-126">x</span><span class="sxs-lookup"><span data-stu-id="f438a-126">x</span></span>     | <span data-ttu-id="f438a-127">x</span><span class="sxs-lookup"><span data-stu-id="f438a-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f438a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f438a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f438a-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="f438a-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="f438a-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f438a-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
