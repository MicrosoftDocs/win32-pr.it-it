---
title: DeviceMemoryBarrierWithGroupSync (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Funzione DeviceMemoryBarrierWithGroupSync HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334404"
---
# <a name="devicememorybarrierwithgroupsync-function"></a><span data-ttu-id="b652c-104">DeviceMemoryBarrierWithGroupSync (funzione)</span><span class="sxs-lookup"><span data-stu-id="b652c-104">DeviceMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="b652c-105">Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b652c-105">Blocks execution of all threads in a group until all device memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="b652c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b652c-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="b652c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b652c-107">Parameters</span></span>

<span data-ttu-id="b652c-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b652c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b652c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b652c-109">Return value</span></span>

<span data-ttu-id="b652c-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b652c-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b652c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b652c-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b652c-112">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b652c-112">Minimum Shader Model</span></span>

<span data-ttu-id="b652c-113">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b652c-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b652c-114">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b652c-114">Shader Model</span></span>                                                                | <span data-ttu-id="b652c-115">Supportato</span><span class="sxs-lookup"><span data-stu-id="b652c-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b652c-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="b652c-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b652c-117">sì</span><span class="sxs-lookup"><span data-stu-id="b652c-117">yes</span></span>       |



 

<span data-ttu-id="b652c-118">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b652c-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b652c-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="b652c-119">Vertex</span></span> | <span data-ttu-id="b652c-120">Hull</span><span class="sxs-lookup"><span data-stu-id="b652c-120">Hull</span></span> | <span data-ttu-id="b652c-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="b652c-121">Domain</span></span> | <span data-ttu-id="b652c-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="b652c-122">Geometry</span></span> | <span data-ttu-id="b652c-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="b652c-123">Pixel</span></span> | <span data-ttu-id="b652c-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b652c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="b652c-125">x</span><span class="sxs-lookup"><span data-stu-id="b652c-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b652c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b652c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b652c-127">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="b652c-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="b652c-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b652c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




