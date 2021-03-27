---
title: length
description: Restituisce la lunghezza del vettore a virgola mobile specificato.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- lunghezza HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727855"
---
# <a name="length"></a><span data-ttu-id="91193-104">length</span><span class="sxs-lookup"><span data-stu-id="91193-104">length</span></span>

<span data-ttu-id="91193-105">Restituisce la lunghezza del vettore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="91193-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="91193-106">lunghezza *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="91193-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="91193-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="91193-107">Parameters</span></span>



| <span data-ttu-id="91193-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="91193-108">Item</span></span>                                                   | <span data-ttu-id="91193-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91193-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="91193-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="91193-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="91193-111">Vettore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="91193-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="91193-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91193-112">Return Value</span></span>

<span data-ttu-id="91193-113">Scalare a virgola mobile che rappresenta la lunghezza del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="91193-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="91193-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="91193-114">Type Description</span></span>



| <span data-ttu-id="91193-115">Nome</span><span class="sxs-lookup"><span data-stu-id="91193-115">Name</span></span>  | [<span data-ttu-id="91193-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="91193-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="91193-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="91193-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="91193-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="91193-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="91193-119">*x*</span><span class="sxs-lookup"><span data-stu-id="91193-119">*x*</span></span>   | [<span data-ttu-id="91193-120">**vettore**</span><span class="sxs-lookup"><span data-stu-id="91193-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="91193-121">**float**</span><span class="sxs-lookup"><span data-stu-id="91193-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="91193-122">any</span><span class="sxs-lookup"><span data-stu-id="91193-122">any</span></span>  |
| <span data-ttu-id="91193-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="91193-123">*ret*</span></span> | [<span data-ttu-id="91193-124">**scalare**</span><span class="sxs-lookup"><span data-stu-id="91193-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="91193-125">**float**</span><span class="sxs-lookup"><span data-stu-id="91193-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="91193-126">1</span><span class="sxs-lookup"><span data-stu-id="91193-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="91193-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="91193-127">Minimum Shader Model</span></span>

<span data-ttu-id="91193-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="91193-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="91193-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="91193-129">Shader Model</span></span>                                                                       | <span data-ttu-id="91193-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="91193-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="91193-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="91193-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="91193-132">sì</span><span class="sxs-lookup"><span data-stu-id="91193-132">yes</span></span>                 |
| [<span data-ttu-id="91193-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="91193-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="91193-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="91193-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="91193-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91193-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91193-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="91193-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

