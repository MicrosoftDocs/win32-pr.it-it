---
title: 'Funzione RWBuffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione RWBuffer:: GetDimensions'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995685"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="4cc27-105">Funzione RWBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="4cc27-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="4cc27-106">Ottiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="4cc27-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc27-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cc27-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="4cc27-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cc27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc27-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4cc27-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc27-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4cc27-110">Type: **uint**</span></span>

<span data-ttu-id="4cc27-111">Lunghezza, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="4cc27-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc27-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cc27-112">Return value</span></span>

<span data-ttu-id="4cc27-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="4cc27-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc27-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cc27-114">Remarks</span></span>

<span data-ttu-id="4cc27-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cc27-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cc27-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="4cc27-116">Vertex</span></span> | <span data-ttu-id="4cc27-117">Hull</span><span class="sxs-lookup"><span data-stu-id="4cc27-117">Hull</span></span> | <span data-ttu-id="4cc27-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="4cc27-118">Domain</span></span> | <span data-ttu-id="4cc27-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="4cc27-119">Geometry</span></span> | <span data-ttu-id="4cc27-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="4cc27-120">Pixel</span></span> | <span data-ttu-id="4cc27-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4cc27-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4cc27-122">x</span><span class="sxs-lookup"><span data-stu-id="4cc27-122">x</span></span>     | <span data-ttu-id="4cc27-123">x</span><span class="sxs-lookup"><span data-stu-id="4cc27-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cc27-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cc27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc27-125">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="4cc27-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="4cc27-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4cc27-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




