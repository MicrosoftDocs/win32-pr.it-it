---
title: funzione DST
description: Calcola un vettore di distanza. | funzione DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- funzione DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886090"
---
# <a name="dst-function"></a><span data-ttu-id="22ff1-105">funzione DST</span><span class="sxs-lookup"><span data-stu-id="22ff1-105">dst function</span></span>

<span data-ttu-id="22ff1-106">Calcola un vettore di distanza.</span><span class="sxs-lookup"><span data-stu-id="22ff1-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ff1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22ff1-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="22ff1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22ff1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ff1-109">*src0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22ff1-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22ff1-110">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="22ff1-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="22ff1-111">Primo vettore.</span><span class="sxs-lookup"><span data-stu-id="22ff1-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="22ff1-112">*src1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22ff1-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22ff1-113">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="22ff1-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="22ff1-114">Secondo vettore.</span><span class="sxs-lookup"><span data-stu-id="22ff1-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ff1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22ff1-115">Return value</span></span>

<span data-ttu-id="22ff1-116">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="22ff1-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="22ff1-117">Vettore di distanza calcolato.</span><span class="sxs-lookup"><span data-stu-id="22ff1-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ff1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="22ff1-118">Remarks</span></span>

<span data-ttu-id="22ff1-119">Questa funzione intrinseca fornisce la stessa funzionalità dell'istruzione vertex shader dell'istruzione [DST](dst---vs.md).</span><span class="sxs-lookup"><span data-stu-id="22ff1-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="22ff1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22ff1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ff1-121">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="22ff1-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




