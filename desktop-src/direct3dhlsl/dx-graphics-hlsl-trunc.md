---
title: tronca (Corecrt \_ Math. h)
description: Tronca un valore a virgola mobile nel componente intero.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- tronca HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995945"
---
# <a name="trunc"></a><span data-ttu-id="42223-104">trunc</span><span class="sxs-lookup"><span data-stu-id="42223-104">trunc</span></span>

<span data-ttu-id="42223-105">Tronca un valore a virgola mobile nel componente intero.</span><span class="sxs-lookup"><span data-stu-id="42223-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="42223-106">troncamento RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="42223-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="42223-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="42223-107">Parameters</span></span>



| <span data-ttu-id="42223-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="42223-108">Item</span></span>                                                   | <span data-ttu-id="42223-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42223-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="42223-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="42223-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="42223-111">\[nell' \] input specificato.</span><span class="sxs-lookup"><span data-stu-id="42223-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="42223-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42223-112">Return Value</span></span>

<span data-ttu-id="42223-113">Valore di input troncato a un componente intero.</span><span class="sxs-lookup"><span data-stu-id="42223-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="42223-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="42223-114">Remarks</span></span>

<span data-ttu-id="42223-115">Questa funzione tronca un valore a virgola mobile nel componente intero.</span><span class="sxs-lookup"><span data-stu-id="42223-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="42223-116">Dato un valore a virgola mobile 1,6, la funzione tronca restituirà 1,0, dove la funzione [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) restituirà 2,0.</span><span class="sxs-lookup"><span data-stu-id="42223-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="42223-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="42223-117">Type Description</span></span>



| <span data-ttu-id="42223-118">Nome</span><span class="sxs-lookup"><span data-stu-id="42223-118">Name</span></span> | [<span data-ttu-id="42223-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="42223-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="42223-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="42223-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="42223-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="42223-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="42223-122">*x*</span><span class="sxs-lookup"><span data-stu-id="42223-122">*x*</span></span>  | <span data-ttu-id="42223-123">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="42223-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="42223-124">**float**</span><span class="sxs-lookup"><span data-stu-id="42223-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="42223-125">any</span><span class="sxs-lookup"><span data-stu-id="42223-125">any</span></span>                          |
| <span data-ttu-id="42223-126">RET</span><span class="sxs-lookup"><span data-stu-id="42223-126">ret</span></span>  | <span data-ttu-id="42223-127">Stesso tipo di input x</span><span class="sxs-lookup"><span data-stu-id="42223-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="42223-128">**float**</span><span class="sxs-lookup"><span data-stu-id="42223-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="42223-129">Le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="42223-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42223-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="42223-130">Minimum Shader Model</span></span>

<span data-ttu-id="42223-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="42223-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42223-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="42223-132">Shader Model</span></span>                                                                       | <span data-ttu-id="42223-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="42223-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42223-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="42223-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="42223-135">sì</span><span class="sxs-lookup"><span data-stu-id="42223-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="42223-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42223-136">Requirements</span></span>



| <span data-ttu-id="42223-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="42223-137">Requirement</span></span> | <span data-ttu-id="42223-138">Valore</span><span class="sxs-lookup"><span data-stu-id="42223-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="42223-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42223-139">Header</span></span><br/> | <dl> <span data-ttu-id="42223-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="42223-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42223-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42223-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42223-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="42223-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

