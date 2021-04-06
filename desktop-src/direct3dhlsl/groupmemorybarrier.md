---
title: GroupMemoryBarrier (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- Funzione GroupMemoryBarrier HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045462"
---
# <a name="groupmemorybarrier-function"></a><span data-ttu-id="b477b-104">GroupMemoryBarrier (funzione)</span><span class="sxs-lookup"><span data-stu-id="b477b-104">GroupMemoryBarrier function</span></span>

<span data-ttu-id="b477b-105">Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="b477b-105">Blocks execution of all threads in a group until all group shared accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b477b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b477b-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="b477b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b477b-107">Parameters</span></span>

<span data-ttu-id="b477b-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b477b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b477b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b477b-109">Return value</span></span>

<span data-ttu-id="b477b-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b477b-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b477b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b477b-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b477b-112">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b477b-112">Minimum Shader Model</span></span>

<span data-ttu-id="b477b-113">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b477b-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b477b-114">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b477b-114">Shader Model</span></span>                                                                | <span data-ttu-id="b477b-115">Supportato</span><span class="sxs-lookup"><span data-stu-id="b477b-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b477b-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="b477b-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b477b-117">sì</span><span class="sxs-lookup"><span data-stu-id="b477b-117">yes</span></span>       |



 

<span data-ttu-id="b477b-118">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b477b-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b477b-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="b477b-119">Vertex</span></span> | <span data-ttu-id="b477b-120">Hull</span><span class="sxs-lookup"><span data-stu-id="b477b-120">Hull</span></span> | <span data-ttu-id="b477b-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="b477b-121">Domain</span></span> | <span data-ttu-id="b477b-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="b477b-122">Geometry</span></span> | <span data-ttu-id="b477b-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="b477b-123">Pixel</span></span> | <span data-ttu-id="b477b-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b477b-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="b477b-125">x</span><span class="sxs-lookup"><span data-stu-id="b477b-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b477b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b477b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b477b-127">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="b477b-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="b477b-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b477b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




