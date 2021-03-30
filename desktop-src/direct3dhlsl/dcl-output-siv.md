---
title: dcl_output_siv (SM4-ASM)
description: '\_output \_ di DCL (SM4-ASM)'
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993216"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="11620-103">\_output \_ di DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="11620-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="11620-104">Dichiara un registro di output che contiene un parametro del [valore di sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="11620-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="11620-105">\_SIV output \_ SIV su \[ *. Masks* \] , *systemValue*</span><span class="sxs-lookup"><span data-stu-id="11620-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="11620-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="11620-106">Item</span></span>                                                                                                                               | <span data-ttu-id="11620-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11620-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11620-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="11620-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="11620-109">\[in \] un registro dei dati di output; *N* è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="11620-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="11620-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. mask\]*</span><span class="sxs-lookup"><span data-stu-id="11620-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="11620-111">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="11620-111">\[in\] Optional.</span></span> <span data-ttu-id="11620-112">Maschera di componenti (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</span><span class="sxs-lookup"><span data-stu-id="11620-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="11620-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="11620-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="11620-114">\[nel \] nome del valore di sistema che è una stringa (vedere [semantica del valore di sistema](dx-graphics-hlsl-semantics.md)) senza il prefisso "SV \_ ".</span><span class="sxs-lookup"><span data-stu-id="11620-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="11620-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="11620-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11620-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="11620-116">Vertex Shader</span></span> | <span data-ttu-id="11620-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="11620-117">Geometry Shader</span></span> | <span data-ttu-id="11620-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="11620-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="11620-119">x</span><span class="sxs-lookup"><span data-stu-id="11620-119">x</span></span>             | <span data-ttu-id="11620-120">x</span><span class="sxs-lookup"><span data-stu-id="11620-120">x</span></span>               |              |



 

<span data-ttu-id="11620-121">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="11620-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="11620-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="11620-122">Example</span></span>

<span data-ttu-id="11620-123">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="11620-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="11620-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="11620-124">Minimum Shader Model</span></span>

<span data-ttu-id="11620-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="11620-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="11620-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="11620-126">Shader Model</span></span>                                              | <span data-ttu-id="11620-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="11620-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11620-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="11620-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11620-129">sì</span><span class="sxs-lookup"><span data-stu-id="11620-129">yes</span></span>       |
| [<span data-ttu-id="11620-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="11620-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11620-131">sì</span><span class="sxs-lookup"><span data-stu-id="11620-131">yes</span></span>       |
| [<span data-ttu-id="11620-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="11620-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11620-133">sì</span><span class="sxs-lookup"><span data-stu-id="11620-133">yes</span></span>       |
| [<span data-ttu-id="11620-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11620-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11620-135">no</span><span class="sxs-lookup"><span data-stu-id="11620-135">no</span></span>        |
| [<span data-ttu-id="11620-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11620-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11620-137">no</span><span class="sxs-lookup"><span data-stu-id="11620-137">no</span></span>        |
| [<span data-ttu-id="11620-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11620-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11620-139">no</span><span class="sxs-lookup"><span data-stu-id="11620-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11620-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11620-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11620-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11620-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





