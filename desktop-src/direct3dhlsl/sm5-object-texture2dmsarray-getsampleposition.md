---
title: 'Funzione Texture2DMSArray:: GetSamplePosition'
description: "Ottiene la posizione dell'esempio specificato. | Funzione Texture2DMSArray:: GetSamplePosition"
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234884"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="d0c97-105">Funzione Texture2DMSArray:: GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="d0c97-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="d0c97-106">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="d0c97-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0c97-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="d0c97-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0c97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c97-109">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0c97-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c97-110">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0c97-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0c97-111">Indice in base zero di una posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="d0c97-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c97-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0c97-112">Return value</span></span>

<span data-ttu-id="d0c97-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="d0c97-113">Type: **float2**</span></span>

<span data-ttu-id="d0c97-114">Percorso di esempio.</span><span class="sxs-lookup"><span data-stu-id="d0c97-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c97-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0c97-115">Remarks</span></span>

<span data-ttu-id="d0c97-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0c97-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d0c97-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="d0c97-117">Vertex</span></span> | <span data-ttu-id="d0c97-118">Hull</span><span class="sxs-lookup"><span data-stu-id="d0c97-118">Hull</span></span> | <span data-ttu-id="d0c97-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="d0c97-119">Domain</span></span> | <span data-ttu-id="d0c97-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="d0c97-120">Geometry</span></span> | <span data-ttu-id="d0c97-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="d0c97-121">Pixel</span></span> | <span data-ttu-id="d0c97-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d0c97-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d0c97-123">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-123">x</span></span>      | <span data-ttu-id="d0c97-124">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-124">x</span></span>    | <span data-ttu-id="d0c97-125">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-125">x</span></span>      | <span data-ttu-id="d0c97-126">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-126">x</span></span>        | <span data-ttu-id="d0c97-127">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-127">x</span></span>     | <span data-ttu-id="d0c97-128">x</span><span class="sxs-lookup"><span data-stu-id="d0c97-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d0c97-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0c97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c97-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d0c97-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="d0c97-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d0c97-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
