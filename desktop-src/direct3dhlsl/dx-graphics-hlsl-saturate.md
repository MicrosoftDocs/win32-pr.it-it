---
title: saturate (riferimento HLSL)
description: Blocca il valore specificato nell'intervallo compreso tra 0 e 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- satura HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337543"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="b7d8a-104">saturate (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7d8a-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="b7d8a-105">Blocca il valore specificato nell'intervallo compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="b7d8a-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="b7d8a-106">saturazione *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="b7d8a-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="b7d8a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7d8a-107">Parameters</span></span>



| <span data-ttu-id="b7d8a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b7d8a-108">Item</span></span>                                                   | <span data-ttu-id="b7d8a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7d8a-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b7d8a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b7d8a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b7d8a-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="b7d8a-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b7d8a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7d8a-112">Return Value</span></span>

<span data-ttu-id="b7d8a-113">Parametro *x* , premuto nell'intervallo compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="b7d8a-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7d8a-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="b7d8a-114">Type Description</span></span>



| <span data-ttu-id="b7d8a-115">Nome</span><span class="sxs-lookup"><span data-stu-id="b7d8a-115">Name</span></span>  | [<span data-ttu-id="b7d8a-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b7d8a-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7d8a-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b7d8a-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b7d8a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b7d8a-119">*x*</span></span>   | <span data-ttu-id="b7d8a-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b7d8a-121">**float**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7d8a-122">any</span><span class="sxs-lookup"><span data-stu-id="b7d8a-122">any</span></span>                            |
| <span data-ttu-id="b7d8a-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="b7d8a-123">*ret*</span></span> | <span data-ttu-id="b7d8a-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="b7d8a-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b7d8a-125">**float**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7d8a-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="b7d8a-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7d8a-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b7d8a-127">Minimum Shader Model</span></span>

<span data-ttu-id="b7d8a-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7d8a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7d8a-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b7d8a-129">Shader Model</span></span>                                                                       | <span data-ttu-id="b7d8a-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="b7d8a-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b7d8a-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="b7d8a-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="b7d8a-132">sì</span><span class="sxs-lookup"><span data-stu-id="b7d8a-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b7d8a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7d8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d8a-134">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b7d8a-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

