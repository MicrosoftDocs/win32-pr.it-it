---
title: 'Funzione RWTexture1D:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture1D:: operator'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530613"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="3efc6-105">Funzione RWTexture1D:: operator</span><span class="sxs-lookup"><span data-stu-id="3efc6-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="3efc6-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3efc6-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3efc6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3efc6-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="3efc6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3efc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3efc6-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3efc6-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3efc6-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3efc6-110">Type: **uint**</span></span>

<span data-ttu-id="3efc6-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3efc6-111">The index position.</span></span> <span data-ttu-id="3efc6-112">Contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="3efc6-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3efc6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3efc6-113">Return value</span></span>

<span data-ttu-id="3efc6-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="3efc6-114">Type: **R**</span></span>

<span data-ttu-id="3efc6-115">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3efc6-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3efc6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3efc6-116">Remarks</span></span>

<span data-ttu-id="3efc6-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3efc6-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3efc6-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="3efc6-118">Vertex</span></span> | <span data-ttu-id="3efc6-119">Hull</span><span class="sxs-lookup"><span data-stu-id="3efc6-119">Hull</span></span> | <span data-ttu-id="3efc6-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="3efc6-120">Domain</span></span> | <span data-ttu-id="3efc6-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="3efc6-121">Geometry</span></span> | <span data-ttu-id="3efc6-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="3efc6-122">Pixel</span></span> | <span data-ttu-id="3efc6-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3efc6-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3efc6-124">x</span><span class="sxs-lookup"><span data-stu-id="3efc6-124">x</span></span>     | <span data-ttu-id="3efc6-125">x</span><span class="sxs-lookup"><span data-stu-id="3efc6-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3efc6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3efc6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3efc6-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="3efc6-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="3efc6-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3efc6-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




