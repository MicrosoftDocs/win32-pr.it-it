---
title: AllMemoryBarrier (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo fino a quando tutti gli accessi alla memoria non sono stati completati.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Funzione AllMemoryBarrier HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398011"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="2b848-104">AllMemoryBarrier (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b848-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="2b848-105">Blocca l'esecuzione di tutti i thread in un gruppo fino a quando tutti gli accessi alla memoria non sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="2b848-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b848-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b848-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="2b848-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b848-107">Parameters</span></span>

<span data-ttu-id="2b848-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="2b848-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b848-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b848-109">Return value</span></span>

<span data-ttu-id="2b848-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2b848-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b848-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b848-111">Remarks</span></span>

<span data-ttu-id="2b848-112">Una barriera di memoria garantisce il completamento delle operazioni di memoria in attesa.</span><span class="sxs-lookup"><span data-stu-id="2b848-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="2b848-113">I thread sono sincronizzati alle barriere GroupSync.</span><span class="sxs-lookup"><span data-stu-id="2b848-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="2b848-114">Questo potrebbe bloccare un thread o thread se sono in corso operazioni di memoria.</span><span class="sxs-lookup"><span data-stu-id="2b848-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2b848-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2b848-115">Minimum Shader Model</span></span>

<span data-ttu-id="2b848-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b848-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b848-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2b848-117">Shader Model</span></span>                                                                | <span data-ttu-id="2b848-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="2b848-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2b848-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="2b848-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2b848-120">sì</span><span class="sxs-lookup"><span data-stu-id="2b848-120">yes</span></span>       |



 

<span data-ttu-id="2b848-121">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b848-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2b848-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="2b848-122">Vertex</span></span> | <span data-ttu-id="2b848-123">Hull</span><span class="sxs-lookup"><span data-stu-id="2b848-123">Hull</span></span> | <span data-ttu-id="2b848-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="2b848-124">Domain</span></span> | <span data-ttu-id="2b848-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="2b848-125">Geometry</span></span> | <span data-ttu-id="2b848-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="2b848-126">Pixel</span></span> | <span data-ttu-id="2b848-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2b848-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2b848-128">x</span><span class="sxs-lookup"><span data-stu-id="2b848-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2b848-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b848-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b848-130">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="2b848-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2b848-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2b848-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




