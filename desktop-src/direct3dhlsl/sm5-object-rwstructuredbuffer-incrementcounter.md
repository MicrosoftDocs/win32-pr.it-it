---
title: 'Funzione RWStructuredBuffer:: IncrementCounter (Httpserv. h)'
description: Incrementa il contatore nascosto dell'oggetto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Funzione IncrementCounter HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355494"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="9e4d0-104">IncrementCounter (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e4d0-104">IncrementCounter function</span></span>

<span data-ttu-id="9e4d0-105">Incrementa il contatore nascosto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e4d0-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e4d0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e4d0-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="9e4d0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e4d0-107">Parameters</span></span>

<span data-ttu-id="9e4d0-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="9e4d0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e4d0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e4d0-109">Return value</span></span>

<span data-ttu-id="9e4d0-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9e4d0-110">Type: **uint**</span></span>

<span data-ttu-id="9e4d0-111">Valore del contatore pre-incrementato.</span><span class="sxs-lookup"><span data-stu-id="9e4d0-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e4d0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e4d0-112">Remarks</span></span>

<span data-ttu-id="9e4d0-113">Per il corretto funzionamento di questo metodo, è necessario che nella visualizzazione di accesso non ordinato associato sia impostato il [**\_ \_ \_ \_ contatore dei flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="9e4d0-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="9e4d0-114">Una risorsa strutturata può essere ulteriormente indicizzata in base ai nomi dei componenti delle strutture.</span><span class="sxs-lookup"><span data-stu-id="9e4d0-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="9e4d0-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e4d0-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9e4d0-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="9e4d0-116">Vertex</span></span> | <span data-ttu-id="9e4d0-117">Hull</span><span class="sxs-lookup"><span data-stu-id="9e4d0-117">Hull</span></span> | <span data-ttu-id="9e4d0-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="9e4d0-118">Domain</span></span> | <span data-ttu-id="9e4d0-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="9e4d0-119">Geometry</span></span> | <span data-ttu-id="9e4d0-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="9e4d0-120">Pixel</span></span> | <span data-ttu-id="9e4d0-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9e4d0-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9e4d0-122">x</span><span class="sxs-lookup"><span data-stu-id="9e4d0-122">x</span></span>     | <span data-ttu-id="9e4d0-123">x</span><span class="sxs-lookup"><span data-stu-id="9e4d0-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="9e4d0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e4d0-124">Requirements</span></span>



| <span data-ttu-id="9e4d0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e4d0-125">Requirement</span></span> | <span data-ttu-id="9e4d0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9e4d0-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e4d0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e4d0-127">Header</span></span><br/> | <dl> <span data-ttu-id="9e4d0-128"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e4d0-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e4d0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e4d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e4d0-130">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="9e4d0-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="9e4d0-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9e4d0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

