---
title: gradi
description: Converte il valore specificato da radianti in gradi.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- gradi HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399215"
---
# <a name="degrees"></a><span data-ttu-id="87b92-104">gradi</span><span class="sxs-lookup"><span data-stu-id="87b92-104">degrees</span></span>

<span data-ttu-id="87b92-105">Converte il valore specificato da radianti in gradi.</span><span class="sxs-lookup"><span data-stu-id="87b92-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="87b92-106">gradi *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="87b92-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="87b92-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="87b92-107">Parameters</span></span>



| <span data-ttu-id="87b92-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="87b92-108">Item</span></span>                                                   | <span data-ttu-id="87b92-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87b92-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="87b92-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="87b92-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="87b92-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="87b92-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="87b92-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87b92-112">Return Value</span></span>

<span data-ttu-id="87b92-113">Risultato della conversione del parametro *x* da radianti a gradi.</span><span class="sxs-lookup"><span data-stu-id="87b92-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="87b92-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="87b92-114">Type Description</span></span>



| <span data-ttu-id="87b92-115">Nome</span><span class="sxs-lookup"><span data-stu-id="87b92-115">Name</span></span>  | [<span data-ttu-id="87b92-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="87b92-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="87b92-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="87b92-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="87b92-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="87b92-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="87b92-119">*x*</span><span class="sxs-lookup"><span data-stu-id="87b92-119">*x*</span></span>   | <span data-ttu-id="87b92-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="87b92-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="87b92-121">**float**</span><span class="sxs-lookup"><span data-stu-id="87b92-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87b92-122">any</span><span class="sxs-lookup"><span data-stu-id="87b92-122">any</span></span>                            |
| <span data-ttu-id="87b92-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="87b92-123">*ret*</span></span> | <span data-ttu-id="87b92-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="87b92-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="87b92-125">**float**</span><span class="sxs-lookup"><span data-stu-id="87b92-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87b92-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="87b92-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87b92-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="87b92-127">Minimum Shader Model</span></span>

<span data-ttu-id="87b92-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="87b92-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="87b92-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="87b92-129">Shader Model</span></span>                                                                       | <span data-ttu-id="87b92-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="87b92-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="87b92-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="87b92-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="87b92-132">sì</span><span class="sxs-lookup"><span data-stu-id="87b92-132">yes</span></span>       |
| [<span data-ttu-id="87b92-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87b92-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="87b92-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="87b92-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="87b92-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87b92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b92-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="87b92-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

