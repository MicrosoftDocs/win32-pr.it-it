---
title: abs
description: Restituisce il valore assoluto del valore specificato.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- HLSL ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976794"
---
# <a name="abs"></a><span data-ttu-id="82921-104">abs</span><span class="sxs-lookup"><span data-stu-id="82921-104">abs</span></span>

<span data-ttu-id="82921-105">Restituisce il valore assoluto del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="82921-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="82921-106">ABS RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="82921-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="82921-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="82921-107">Parameters</span></span>



| <span data-ttu-id="82921-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="82921-108">Item</span></span>                                                   | <span data-ttu-id="82921-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82921-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="82921-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="82921-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="82921-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="82921-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="82921-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82921-112">Return Value</span></span>

<span data-ttu-id="82921-113">Valore assoluto del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="82921-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="82921-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="82921-114">Type Description</span></span>



| <span data-ttu-id="82921-115">Nome</span><span class="sxs-lookup"><span data-stu-id="82921-115">Name</span></span>  | [<span data-ttu-id="82921-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="82921-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="82921-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="82921-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="82921-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="82921-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="82921-119">*x*</span><span class="sxs-lookup"><span data-stu-id="82921-119">*x*</span></span>   | <span data-ttu-id="82921-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="82921-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="82921-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="82921-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="82921-122">any</span><span class="sxs-lookup"><span data-stu-id="82921-122">any</span></span>                            |
| <span data-ttu-id="82921-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="82921-123">*ret*</span></span> | <span data-ttu-id="82921-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="82921-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="82921-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="82921-125">same as input *x*</span></span>                                                              | <span data-ttu-id="82921-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="82921-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82921-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="82921-127">Minimum Shader Model</span></span>

<span data-ttu-id="82921-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="82921-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="82921-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="82921-129">Shader Model</span></span>                                                                       | <span data-ttu-id="82921-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="82921-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="82921-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="82921-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="82921-132">sì</span><span class="sxs-lookup"><span data-stu-id="82921-132">yes</span></span>                   |
| [<span data-ttu-id="82921-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82921-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="82921-134">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="82921-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="82921-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82921-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82921-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="82921-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

