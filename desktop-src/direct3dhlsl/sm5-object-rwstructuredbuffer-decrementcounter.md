---
title: RWStructuredBuffer::D funzione ecrementCounter (Httpserv. h)
description: Decrementa il contatore nascosto dell'oggetto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Funzione DecrementCounter HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982388"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="67bc3-104">DecrementCounter (funzione)</span><span class="sxs-lookup"><span data-stu-id="67bc3-104">DecrementCounter function</span></span>

<span data-ttu-id="67bc3-105">Decrementa il contatore nascosto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="67bc3-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bc3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67bc3-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="67bc3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67bc3-107">Parameters</span></span>

<span data-ttu-id="67bc3-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="67bc3-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67bc3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67bc3-109">Return value</span></span>

<span data-ttu-id="67bc3-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="67bc3-110">Type: **uint**</span></span>

<span data-ttu-id="67bc3-111">Valore del contatore dopo il decremento.</span><span class="sxs-lookup"><span data-stu-id="67bc3-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bc3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="67bc3-112">Remarks</span></span>

<span data-ttu-id="67bc3-113">Per il funzionamento della visualizzazione di accesso non ordinato associato è necessario impostare il [**\_ \_ \_ \_ contatore del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante creationfor.</span><span class="sxs-lookup"><span data-stu-id="67bc3-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="67bc3-114">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="67bc3-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="67bc3-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="67bc3-115">Vertex</span></span> | <span data-ttu-id="67bc3-116">Hull</span><span class="sxs-lookup"><span data-stu-id="67bc3-116">Hull</span></span> | <span data-ttu-id="67bc3-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="67bc3-117">Domain</span></span> | <span data-ttu-id="67bc3-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="67bc3-118">Geometry</span></span> | <span data-ttu-id="67bc3-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="67bc3-119">Pixel</span></span> | <span data-ttu-id="67bc3-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="67bc3-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="67bc3-121">x</span><span class="sxs-lookup"><span data-stu-id="67bc3-121">x</span></span>     | <span data-ttu-id="67bc3-122">x</span><span class="sxs-lookup"><span data-stu-id="67bc3-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="67bc3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67bc3-123">Requirements</span></span>



| <span data-ttu-id="67bc3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="67bc3-124">Requirement</span></span> | <span data-ttu-id="67bc3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="67bc3-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67bc3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67bc3-126">Header</span></span><br/> | <dl> <span data-ttu-id="67bc3-127"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="67bc3-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67bc3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67bc3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bc3-129">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="67bc3-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="67bc3-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="67bc3-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

