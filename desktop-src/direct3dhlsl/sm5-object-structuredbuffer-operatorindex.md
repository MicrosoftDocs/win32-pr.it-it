---
title: 'Funzione StructuredBuffer:: operator'
description: Restituisce una variabile di risorse di sola lettura di un StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118823"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="aad16-104">Funzione StructuredBuffer:: operator</span><span class="sxs-lookup"><span data-stu-id="aad16-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="aad16-105">Restituisce una variabile di risorse di sola lettura di un [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="aad16-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aad16-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aad16-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="aad16-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aad16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad16-108">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad16-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad16-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aad16-109">Type: **uint**</span></span>

<span data-ttu-id="aad16-110">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="aad16-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad16-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aad16-111">Return value</span></span>

<span data-ttu-id="aad16-112">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="aad16-112">Type: **R**</span></span>

<span data-ttu-id="aad16-113">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="aad16-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="aad16-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="aad16-114">Remarks</span></span>

<span data-ttu-id="aad16-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="aad16-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aad16-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="aad16-116">Vertex</span></span> | <span data-ttu-id="aad16-117">Hull</span><span class="sxs-lookup"><span data-stu-id="aad16-117">Hull</span></span> | <span data-ttu-id="aad16-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="aad16-118">Domain</span></span> | <span data-ttu-id="aad16-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="aad16-119">Geometry</span></span> | <span data-ttu-id="aad16-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="aad16-120">Pixel</span></span> | <span data-ttu-id="aad16-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="aad16-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aad16-122">x</span><span class="sxs-lookup"><span data-stu-id="aad16-122">x</span></span>      | <span data-ttu-id="aad16-123">x</span><span class="sxs-lookup"><span data-stu-id="aad16-123">x</span></span>    | <span data-ttu-id="aad16-124">x</span><span class="sxs-lookup"><span data-stu-id="aad16-124">x</span></span>      | <span data-ttu-id="aad16-125">x</span><span class="sxs-lookup"><span data-stu-id="aad16-125">x</span></span>        | <span data-ttu-id="aad16-126">x</span><span class="sxs-lookup"><span data-stu-id="aad16-126">x</span></span>     | <span data-ttu-id="aad16-127">x</span><span class="sxs-lookup"><span data-stu-id="aad16-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aad16-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aad16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad16-129">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="aad16-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="aad16-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="aad16-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




