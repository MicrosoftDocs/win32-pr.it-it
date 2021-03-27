---
title: DeviceMemoryBarrier (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- Funzione DeviceMemoryBarrier HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397083"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="b0879-104">DeviceMemoryBarrier (funzione)</span><span class="sxs-lookup"><span data-stu-id="b0879-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="b0879-105">Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="b0879-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0879-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0879-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="b0879-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0879-107">Parameters</span></span>

<span data-ttu-id="b0879-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b0879-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0879-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0879-109">Return value</span></span>

<span data-ttu-id="b0879-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b0879-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0879-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0879-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b0879-112">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b0879-112">Minimum Shader Model</span></span>

<span data-ttu-id="b0879-113">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0879-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b0879-114">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b0879-114">Shader Model</span></span>                                                                | <span data-ttu-id="b0879-115">Supportato</span><span class="sxs-lookup"><span data-stu-id="b0879-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b0879-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="b0879-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b0879-117">sì</span><span class="sxs-lookup"><span data-stu-id="b0879-117">yes</span></span>       |



 

<span data-ttu-id="b0879-118">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0879-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b0879-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="b0879-119">Vertex</span></span> | <span data-ttu-id="b0879-120">Hull</span><span class="sxs-lookup"><span data-stu-id="b0879-120">Hull</span></span> | <span data-ttu-id="b0879-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="b0879-121">Domain</span></span> | <span data-ttu-id="b0879-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="b0879-122">Geometry</span></span> | <span data-ttu-id="b0879-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="b0879-123">Pixel</span></span> | <span data-ttu-id="b0879-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b0879-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b0879-125">x</span><span class="sxs-lookup"><span data-stu-id="b0879-125">x</span></span>     | <span data-ttu-id="b0879-126">x</span><span class="sxs-lookup"><span data-stu-id="b0879-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b0879-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0879-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0879-128">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="b0879-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="b0879-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b0879-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




