---
title: any
description: Determina se i componenti del valore specificato sono diversi da zero.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- qualsiasi HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976847"
---
# <a name="any"></a><span data-ttu-id="472cb-104">any</span><span class="sxs-lookup"><span data-stu-id="472cb-104">any</span></span>

<span data-ttu-id="472cb-105">Determina se i componenti del valore specificato sono diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="472cb-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="472cb-106">*ret* any (*x*)</span><span class="sxs-lookup"><span data-stu-id="472cb-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="472cb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="472cb-107">Parameters</span></span>



| <span data-ttu-id="472cb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="472cb-108">Item</span></span>                                                   | <span data-ttu-id="472cb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="472cb-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="472cb-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="472cb-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="472cb-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="472cb-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="472cb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="472cb-112">Return Value</span></span>

<span data-ttu-id="472cb-113">**True** se i componenti del parametro *x* sono diversi da zero. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="472cb-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="472cb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="472cb-114">Remarks</span></span>

<span data-ttu-id="472cb-115">Questa funzione è simile alla funzione intrinseca [**All**](dx-graphics-hlsl-all.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="472cb-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="472cb-116">La funzione **any** determina se i componenti del valore specificato sono diversi da zero, mentre la funzione **All** determina se tutti i componenti del valore specificato sono diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="472cb-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="472cb-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="472cb-117">Type Description</span></span>



| <span data-ttu-id="472cb-118">Nome</span><span class="sxs-lookup"><span data-stu-id="472cb-118">Name</span></span>  | [<span data-ttu-id="472cb-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="472cb-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="472cb-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="472cb-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="472cb-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="472cb-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="472cb-122">*x*</span><span class="sxs-lookup"><span data-stu-id="472cb-122">*x*</span></span>   | <span data-ttu-id="472cb-123">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="472cb-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="472cb-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="472cb-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="472cb-125">any</span><span class="sxs-lookup"><span data-stu-id="472cb-125">any</span></span>  |
| <span data-ttu-id="472cb-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="472cb-126">*ret*</span></span> | [<span data-ttu-id="472cb-127">**scalare**</span><span class="sxs-lookup"><span data-stu-id="472cb-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="472cb-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="472cb-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="472cb-129">1</span><span class="sxs-lookup"><span data-stu-id="472cb-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="472cb-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="472cb-130">Minimum Shader Model</span></span>

<span data-ttu-id="472cb-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="472cb-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="472cb-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="472cb-132">Shader Model</span></span>                                                                       | <span data-ttu-id="472cb-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="472cb-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="472cb-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="472cb-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="472cb-135">sì</span><span class="sxs-lookup"><span data-stu-id="472cb-135">yes</span></span>                   |
| [<span data-ttu-id="472cb-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="472cb-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="472cb-137">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="472cb-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="472cb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="472cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472cb-139">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="472cb-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

