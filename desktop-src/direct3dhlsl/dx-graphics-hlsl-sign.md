---
title: segno
description: Restituisce il segno di x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- firma HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993565"
---
# <a name="sign"></a><span data-ttu-id="c16d8-104">segno</span><span class="sxs-lookup"><span data-stu-id="c16d8-104">sign</span></span>

<span data-ttu-id="c16d8-105">Restituisce il segno di *x*.</span><span class="sxs-lookup"><span data-stu-id="c16d8-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="c16d8-106">segno *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="c16d8-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="c16d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c16d8-107">Parameters</span></span>



| <span data-ttu-id="c16d8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c16d8-108">Item</span></span>                                                   | <span data-ttu-id="c16d8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c16d8-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="c16d8-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c16d8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c16d8-111">\[nel \] valore di input.</span><span class="sxs-lookup"><span data-stu-id="c16d8-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c16d8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c16d8-112">Return Value</span></span>

<span data-ttu-id="c16d8-113">Restituisce-1 se *x* è minore di zero; 0 se *x* è uguale a zero; e 1 se *x* è maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="c16d8-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="c16d8-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c16d8-114">Type Description</span></span>



| <span data-ttu-id="c16d8-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c16d8-115">Name</span></span>  | [<span data-ttu-id="c16d8-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c16d8-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c16d8-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c16d8-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="c16d8-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c16d8-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c16d8-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c16d8-119">*x*</span></span>   | <span data-ttu-id="c16d8-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="c16d8-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="c16d8-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c16d8-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c16d8-122">any</span><span class="sxs-lookup"><span data-stu-id="c16d8-122">any</span></span>                            |
| <span data-ttu-id="c16d8-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c16d8-123">*ret*</span></span> | <span data-ttu-id="c16d8-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="c16d8-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c16d8-125">**INT**</span><span class="sxs-lookup"><span data-stu-id="c16d8-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="c16d8-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="c16d8-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c16d8-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c16d8-127">Minimum Shader Model</span></span>

<span data-ttu-id="c16d8-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c16d8-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c16d8-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c16d8-129">Shader Model</span></span>                                                                       | <span data-ttu-id="c16d8-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="c16d8-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="c16d8-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="c16d8-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c16d8-132">sì</span><span class="sxs-lookup"><span data-stu-id="c16d8-132">yes</span></span>                         |
| [<span data-ttu-id="c16d8-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c16d8-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c16d8-134">Sì (vs \_ 1 \_ e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="c16d8-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c16d8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c16d8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16d8-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c16d8-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

