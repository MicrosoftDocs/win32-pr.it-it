---
title: determinante
description: Restituisce il determinante della matrice quadrata a virgola mobile specificata.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- HLSL determinante
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976714"
---
# <a name="determinant"></a><span data-ttu-id="62a17-104">determinante</span><span class="sxs-lookup"><span data-stu-id="62a17-104">determinant</span></span>

<span data-ttu-id="62a17-105">Restituisce il determinante della matrice quadrata a virgola mobile specificata.</span><span class="sxs-lookup"><span data-stu-id="62a17-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="62a17-106">determinante *ret* (*m*)</span><span class="sxs-lookup"><span data-stu-id="62a17-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="62a17-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="62a17-107">Parameters</span></span>



| <span data-ttu-id="62a17-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="62a17-108">Item</span></span>                                                   | <span data-ttu-id="62a17-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a17-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="62a17-110"><span id="m"></span><span id="M"></span>*m*</span><span class="sxs-lookup"><span data-stu-id="62a17-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="62a17-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="62a17-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="62a17-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62a17-112">Return Value</span></span>

<span data-ttu-id="62a17-113">Valore scalare a virgola mobile che rappresenta il determinante del parametro *m* .</span><span class="sxs-lookup"><span data-stu-id="62a17-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="62a17-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="62a17-114">Type Description</span></span>



| <span data-ttu-id="62a17-115">Nome</span><span class="sxs-lookup"><span data-stu-id="62a17-115">Name</span></span>  | [<span data-ttu-id="62a17-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="62a17-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="62a17-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="62a17-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="62a17-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="62a17-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="62a17-119">*m*</span><span class="sxs-lookup"><span data-stu-id="62a17-119">*m*</span></span>   | [<span data-ttu-id="62a17-120">**matrice**</span><span class="sxs-lookup"><span data-stu-id="62a17-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="62a17-121">**float**</span><span class="sxs-lookup"><span data-stu-id="62a17-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="62a17-122">Any (numero di righe = numero di colonne)</span><span class="sxs-lookup"><span data-stu-id="62a17-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="62a17-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="62a17-123">*ret*</span></span> | [<span data-ttu-id="62a17-124">**scalare**</span><span class="sxs-lookup"><span data-stu-id="62a17-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="62a17-125">**float**</span><span class="sxs-lookup"><span data-stu-id="62a17-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="62a17-126">1</span><span class="sxs-lookup"><span data-stu-id="62a17-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="62a17-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="62a17-127">Minimum Shader Model</span></span>

<span data-ttu-id="62a17-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="62a17-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="62a17-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="62a17-129">Shader Model</span></span>                                                                       | <span data-ttu-id="62a17-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="62a17-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="62a17-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="62a17-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="62a17-132">sì</span><span class="sxs-lookup"><span data-stu-id="62a17-132">yes</span></span>                   |
| [<span data-ttu-id="62a17-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62a17-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="62a17-134">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="62a17-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="62a17-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62a17-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a17-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="62a17-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

