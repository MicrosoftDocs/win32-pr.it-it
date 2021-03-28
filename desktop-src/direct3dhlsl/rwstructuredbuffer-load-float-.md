---
title: 'Funzione RWStructuredBuffer:: Load (int)'
description: 'Legge i dati del buffer. | Funzione RWStructuredBuffer:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995365"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="305ea-105">Funzione RWStructuredBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="305ea-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="305ea-106">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="305ea-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="305ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="305ea-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="305ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="305ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="305ea-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="305ea-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="305ea-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="305ea-110">Type: **int**</span></span>

<span data-ttu-id="305ea-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="305ea-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="305ea-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="305ea-112">Return value</span></span>

<span data-ttu-id="305ea-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="305ea-113">Type:</span></span>

<span data-ttu-id="305ea-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="305ea-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="305ea-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="305ea-115">Remarks</span></span>

<span data-ttu-id="305ea-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="305ea-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="305ea-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="305ea-117">Vertex</span></span> | <span data-ttu-id="305ea-118">Hull</span><span class="sxs-lookup"><span data-stu-id="305ea-118">Hull</span></span> | <span data-ttu-id="305ea-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="305ea-119">Domain</span></span> | <span data-ttu-id="305ea-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="305ea-120">Geometry</span></span> | <span data-ttu-id="305ea-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="305ea-121">Pixel</span></span> | <span data-ttu-id="305ea-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="305ea-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="305ea-123">x</span><span class="sxs-lookup"><span data-stu-id="305ea-123">x</span></span>      | <span data-ttu-id="305ea-124">x</span><span class="sxs-lookup"><span data-stu-id="305ea-124">x</span></span>    | <span data-ttu-id="305ea-125">x</span><span class="sxs-lookup"><span data-stu-id="305ea-125">x</span></span>      | <span data-ttu-id="305ea-126">x</span><span class="sxs-lookup"><span data-stu-id="305ea-126">x</span></span>        | <span data-ttu-id="305ea-127">x</span><span class="sxs-lookup"><span data-stu-id="305ea-127">x</span></span>     | <span data-ttu-id="305ea-128">x</span><span class="sxs-lookup"><span data-stu-id="305ea-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="305ea-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="305ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305ea-130">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="305ea-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




