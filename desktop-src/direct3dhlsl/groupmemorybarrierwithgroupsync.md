---
title: GroupMemoryBarrierWithGroupSync (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Funzione GroupMemoryBarrierWithGroupSync HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976186"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a><span data-ttu-id="1c136-104">GroupMemoryBarrierWithGroupSync (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c136-104">GroupMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="1c136-105">Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1c136-105">Blocks execution of all threads in a group until all group shared accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c136-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c136-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="1c136-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c136-107">Parameters</span></span>

<span data-ttu-id="1c136-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="1c136-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c136-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c136-109">Return value</span></span>

<span data-ttu-id="1c136-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1c136-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c136-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c136-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1c136-112">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="1c136-112">Minimum Shader Model</span></span>

<span data-ttu-id="1c136-113">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c136-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c136-114">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="1c136-114">Shader Model</span></span>                                                                | <span data-ttu-id="1c136-115">Supportato</span><span class="sxs-lookup"><span data-stu-id="1c136-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1c136-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="1c136-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1c136-117">sì</span><span class="sxs-lookup"><span data-stu-id="1c136-117">yes</span></span>       |



 

<span data-ttu-id="1c136-118">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1c136-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1c136-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="1c136-119">Vertex</span></span> | <span data-ttu-id="1c136-120">Hull</span><span class="sxs-lookup"><span data-stu-id="1c136-120">Hull</span></span> | <span data-ttu-id="1c136-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="1c136-121">Domain</span></span> | <span data-ttu-id="1c136-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="1c136-122">Geometry</span></span> | <span data-ttu-id="1c136-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="1c136-123">Pixel</span></span> | <span data-ttu-id="1c136-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="1c136-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1c136-125">x</span><span class="sxs-lookup"><span data-stu-id="1c136-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1c136-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c136-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c136-127">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="1c136-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1c136-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="1c136-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




