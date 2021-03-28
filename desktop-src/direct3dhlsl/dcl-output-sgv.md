---
title: dcl_output_sgv (SM4-ASM)
description: '\_ \_ SGV di output di DCL (SM4-ASM)'
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398300"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="2501a-103">\_ \_ SGV di output di DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2501a-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="2501a-104">Dichiara un registro di output che contiene un parametro del [valore di sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="2501a-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="2501a-105">\_ \_ SGV di output di DCL su *\[ \] . mask*, *systemValue*</span><span class="sxs-lookup"><span data-stu-id="2501a-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="2501a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2501a-106">Item</span></span>                                                                                                                               | <span data-ttu-id="2501a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2501a-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2501a-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="2501a-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="2501a-109">\[in \] un registro dei dati di output; *N* è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="2501a-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="2501a-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. mask\]*</span><span class="sxs-lookup"><span data-stu-id="2501a-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="2501a-111">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2501a-111">\[in\] Optional.</span></span> <span data-ttu-id="2501a-112">Maschera di componenti (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2501a-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="2501a-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="2501a-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="2501a-114">\[nel \] nome del valore di sistema che è una stringa (vedere [semantica del valore di sistema](dx-graphics-hlsl-semantics.md)) senza il prefisso "SV \_ ".</span><span class="sxs-lookup"><span data-stu-id="2501a-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="2501a-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2501a-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2501a-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2501a-116">Vertex Shader</span></span> | <span data-ttu-id="2501a-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2501a-117">Geometry Shader</span></span> | <span data-ttu-id="2501a-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2501a-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="2501a-119">x</span><span class="sxs-lookup"><span data-stu-id="2501a-119">x</span></span>               |              |



 

<span data-ttu-id="2501a-120">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="2501a-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="2501a-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="2501a-121">Example</span></span>

<span data-ttu-id="2501a-122">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="2501a-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="2501a-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2501a-123">Minimum Shader Model</span></span>

<span data-ttu-id="2501a-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2501a-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2501a-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2501a-125">Shader Model</span></span>                                              | <span data-ttu-id="2501a-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="2501a-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2501a-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2501a-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2501a-128">sì</span><span class="sxs-lookup"><span data-stu-id="2501a-128">yes</span></span>       |
| [<span data-ttu-id="2501a-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2501a-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2501a-130">sì</span><span class="sxs-lookup"><span data-stu-id="2501a-130">yes</span></span>       |
| [<span data-ttu-id="2501a-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2501a-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2501a-132">sì</span><span class="sxs-lookup"><span data-stu-id="2501a-132">yes</span></span>       |
| [<span data-ttu-id="2501a-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2501a-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2501a-134">no</span><span class="sxs-lookup"><span data-stu-id="2501a-134">no</span></span>        |
| [<span data-ttu-id="2501a-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2501a-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2501a-136">no</span><span class="sxs-lookup"><span data-stu-id="2501a-136">no</span></span>        |
| [<span data-ttu-id="2501a-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2501a-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2501a-138">no</span><span class="sxs-lookup"><span data-stu-id="2501a-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2501a-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2501a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2501a-140">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2501a-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





