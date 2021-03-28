---
title: D3DCOLORtoUBYTE4
description: Converte un vettore 4D a virgola mobile impostato da un D3DCOLOR in un UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- HLSL D3DCOLORtoUBYTE4
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517073"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="60a06-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="60a06-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="60a06-105">Converte un vettore 4D a virgola mobile impostato da un D3DCOLOR in un UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="60a06-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="60a06-106">*ret* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="60a06-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="60a06-107">Questa funzione swizzles e ridimensiona i componenti del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="60a06-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="60a06-108">Usare questa funzione per compensare la mancanza di supporto UBYTE4 in alcuni componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="60a06-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="60a06-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60a06-109">Parameters</span></span>



| <span data-ttu-id="60a06-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="60a06-110">Item</span></span>                                                   | <span data-ttu-id="60a06-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a06-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="60a06-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="60a06-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="60a06-113">\[nell' \] oggetto Vector4 a virgola mobile da convertire.</span><span class="sxs-lookup"><span data-stu-id="60a06-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="60a06-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60a06-114">Return Value</span></span>

<span data-ttu-id="60a06-115">Rappresentazione UBYTE4 del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="60a06-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="60a06-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="60a06-116">Type Description</span></span>



| <span data-ttu-id="60a06-117">Nome</span><span class="sxs-lookup"><span data-stu-id="60a06-117">Name</span></span>  | [<span data-ttu-id="60a06-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="60a06-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="60a06-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="60a06-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="60a06-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="60a06-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="60a06-121">*x*</span><span class="sxs-lookup"><span data-stu-id="60a06-121">*x*</span></span>   | [<span data-ttu-id="60a06-122">**vettore**</span><span class="sxs-lookup"><span data-stu-id="60a06-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="60a06-123">**float**</span><span class="sxs-lookup"><span data-stu-id="60a06-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="60a06-124">4</span><span class="sxs-lookup"><span data-stu-id="60a06-124">4</span></span>    |
| <span data-ttu-id="60a06-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="60a06-125">*ret*</span></span> | [<span data-ttu-id="60a06-126">**vettore**</span><span class="sxs-lookup"><span data-stu-id="60a06-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="60a06-127">**intero**</span><span class="sxs-lookup"><span data-stu-id="60a06-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="60a06-128">4</span><span class="sxs-lookup"><span data-stu-id="60a06-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60a06-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="60a06-129">Minimum Shader Model</span></span>

<span data-ttu-id="60a06-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="60a06-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60a06-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="60a06-131">Shader Model</span></span>                                                                       | <span data-ttu-id="60a06-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="60a06-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="60a06-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="60a06-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="60a06-134">sì</span><span class="sxs-lookup"><span data-stu-id="60a06-134">yes</span></span>       |
| [<span data-ttu-id="60a06-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60a06-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="60a06-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60a06-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="60a06-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60a06-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a06-138">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="60a06-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

