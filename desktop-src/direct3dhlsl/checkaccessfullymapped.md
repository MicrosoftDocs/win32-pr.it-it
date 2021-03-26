---
title: CheckAccessFullyMapped (funzione)
description: Determina se tutti i valori di un'operazione di esempio, di raccolta o di caricamento hanno eseguito l'accesso ai riquadri mappati in una risorsa affiancata.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Funzione CheckAccessFullyMapped HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729370"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="964b4-104">CheckAccessFullyMapped (funzione)</span><span class="sxs-lookup"><span data-stu-id="964b4-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="964b4-105">Determina se tutti i valori di un'operazione di **esempio**, di **raccolta** o di **caricamento** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="964b4-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="964b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="964b4-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="964b4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="964b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964b4-108">*stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="964b4-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964b4-109">Tipo: **\_ solo uint**</span><span class="sxs-lookup"><span data-stu-id="964b4-109">Type: **uint\_only**</span></span>

<span data-ttu-id="964b4-110">Valore di stato restituito da un'operazione di **esempio**, **raccolta** o **caricamento** .</span><span class="sxs-lookup"><span data-stu-id="964b4-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="964b4-111">Poiché non è possibile accedere direttamente a questo valore di stato, è necessario passarlo a **CheckAccessFullyMapped**.</span><span class="sxs-lookup"><span data-stu-id="964b4-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964b4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="964b4-112">Return value</span></span>

<span data-ttu-id="964b4-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="964b4-113">Type: **bool**</span></span>

<span data-ttu-id="964b4-114">Restituisce un valore **booleano** che indica se tutti i valori di un'operazione di **esempio**, di **raccolta** o di **caricamento** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="964b4-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="964b4-115">Restituisce **true** se tutti i valori dell'operazione hanno eseguito l'accesso ai riquadri mappati; in caso contrario, restituisce **false** se sono stati rilevati valori da un riquadro non mappato.</span><span class="sxs-lookup"><span data-stu-id="964b4-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="964b4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="964b4-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="964b4-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="964b4-117">Minimum Shader Model</span></span>

<span data-ttu-id="964b4-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="964b4-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="964b4-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="964b4-119">Shader Model</span></span>                                                                | <span data-ttu-id="964b4-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="964b4-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="964b4-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="964b4-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="964b4-122">sì</span><span class="sxs-lookup"><span data-stu-id="964b4-122">yes</span></span>       |



 

<span data-ttu-id="964b4-123">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="964b4-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="964b4-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="964b4-124">Vertex</span></span> | <span data-ttu-id="964b4-125">Hull</span><span class="sxs-lookup"><span data-stu-id="964b4-125">Hull</span></span> | <span data-ttu-id="964b4-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="964b4-126">Domain</span></span> | <span data-ttu-id="964b4-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="964b4-127">Geometry</span></span> | <span data-ttu-id="964b4-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="964b4-128">Pixel</span></span> | <span data-ttu-id="964b4-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="964b4-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="964b4-130">x</span><span class="sxs-lookup"><span data-stu-id="964b4-130">x</span></span>     | <span data-ttu-id="964b4-131">x</span><span class="sxs-lookup"><span data-stu-id="964b4-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="964b4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="964b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964b4-133">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="964b4-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 