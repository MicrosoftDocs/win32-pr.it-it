---
title: 'Funzione ConsumeStructuredBuffer:: consume'
description: Rimuove un valore dalla fine del buffer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Usa funzione HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045987"
---
# <a name="consume-function"></a><span data-ttu-id="83254-104">Funzione consume</span><span class="sxs-lookup"><span data-stu-id="83254-104">Consume function</span></span>

<span data-ttu-id="83254-105">Rimuove un valore dalla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="83254-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="83254-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83254-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="83254-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="83254-107">Parameters</span></span>

<span data-ttu-id="83254-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="83254-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83254-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83254-109">Return value</span></span>

<span data-ttu-id="83254-110">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="83254-110">Type: **T**</span></span>

<span data-ttu-id="83254-111">Il valore è stato rimosso (può essere una struttura).</span><span class="sxs-lookup"><span data-stu-id="83254-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="83254-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="83254-112">Remarks</span></span>

<span data-ttu-id="83254-113">T può essere qualsiasi tipo di dati, inclusa una struttura.</span><span class="sxs-lookup"><span data-stu-id="83254-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="83254-114">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="83254-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83254-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="83254-115">Vertex</span></span> | <span data-ttu-id="83254-116">Hull</span><span class="sxs-lookup"><span data-stu-id="83254-116">Hull</span></span> | <span data-ttu-id="83254-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="83254-117">Domain</span></span> | <span data-ttu-id="83254-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="83254-118">Geometry</span></span> | <span data-ttu-id="83254-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="83254-119">Pixel</span></span> | <span data-ttu-id="83254-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="83254-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="83254-121">x</span><span class="sxs-lookup"><span data-stu-id="83254-121">x</span></span>      | <span data-ttu-id="83254-122">x</span><span class="sxs-lookup"><span data-stu-id="83254-122">x</span></span>    | <span data-ttu-id="83254-123">x</span><span class="sxs-lookup"><span data-stu-id="83254-123">x</span></span>      | <span data-ttu-id="83254-124">x</span><span class="sxs-lookup"><span data-stu-id="83254-124">x</span></span>        | <span data-ttu-id="83254-125">x</span><span class="sxs-lookup"><span data-stu-id="83254-125">x</span></span>     | <span data-ttu-id="83254-126">x</span><span class="sxs-lookup"><span data-stu-id="83254-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83254-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83254-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83254-128">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="83254-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="83254-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="83254-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




