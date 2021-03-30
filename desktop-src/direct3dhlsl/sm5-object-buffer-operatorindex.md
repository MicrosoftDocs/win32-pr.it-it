---
title: 'Funzione buffer:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione buffer:: operator'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Scrittura diretta funzione operatore
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401852"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="b1d90-105">Funzione buffer:: operator</span><span class="sxs-lookup"><span data-stu-id="b1d90-105">Buffer::Operator  function</span></span>

<span data-ttu-id="b1d90-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b1d90-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d90-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1d90-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="b1d90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1d90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d90-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1d90-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1d90-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b1d90-110">Type: **uint**</span></span>

<span data-ttu-id="b1d90-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b1d90-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d90-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1d90-112">Return value</span></span>

<span data-ttu-id="b1d90-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="b1d90-113">Type: **R**</span></span>

<span data-ttu-id="b1d90-114">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1d90-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d90-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1d90-115">Remarks</span></span>

<span data-ttu-id="b1d90-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1d90-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b1d90-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="b1d90-117">Vertex</span></span> | <span data-ttu-id="b1d90-118">Hull</span><span class="sxs-lookup"><span data-stu-id="b1d90-118">Hull</span></span> | <span data-ttu-id="b1d90-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="b1d90-119">Domain</span></span> | <span data-ttu-id="b1d90-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="b1d90-120">Geometry</span></span> | <span data-ttu-id="b1d90-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="b1d90-121">Pixel</span></span> | <span data-ttu-id="b1d90-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b1d90-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b1d90-123">x</span><span class="sxs-lookup"><span data-stu-id="b1d90-123">x</span></span>     | <span data-ttu-id="b1d90-124">x</span><span class="sxs-lookup"><span data-stu-id="b1d90-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b1d90-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1d90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d90-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="b1d90-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="b1d90-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b1d90-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




