---
title: dcl_resource (SM4-ASM)
description: '\_risorsa DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719471"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="c1379-103">\_risorsa DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c1379-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="c1379-104">Dichiara una risorsa di input shader non multicampionata.</span><span class="sxs-lookup"><span data-stu-id="c1379-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="c1379-105">\_risorsa DCL *TN*, *ResourceType*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="c1379-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="c1379-106">Dichiara una risorsa di input shader multicampionata.</span><span class="sxs-lookup"><span data-stu-id="c1379-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="c1379-107">\_risorsa DCL *TN*, *\[ dimensioni ResourceType \] nn*, *returnType*</span><span class="sxs-lookup"><span data-stu-id="c1379-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="c1379-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c1379-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="c1379-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1379-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1379-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="c1379-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="c1379-111">\[nel \] Registro di trama, dove *N* è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="c1379-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="c1379-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="c1379-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="c1379-113">\[in \] qualsiasi tipo di oggetto elencato nella pagina [texture-Object](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="c1379-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="c1379-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*dimensioni del resourceType \[ \] nn*</span><span class="sxs-lookup"><span data-stu-id="c1379-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="c1379-115">\[in \] un tipo di oggetto Texture2D o Texture2DArray (vedere la pagina [texture-Object](dx-graphics-hlsl-to-type.md) ); *size* è un numero intero facoltativo che indica il numero di elementi nella matrice. *Nn* è un numero intero che indica il numero di campionamenti.</span><span class="sxs-lookup"><span data-stu-id="c1379-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="c1379-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="c1379-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="c1379-117">\[nel \] tipo restituito per componente che è uno dei seguenti: UNORM, russar, Sint, uint o float.</span><span class="sxs-lookup"><span data-stu-id="c1379-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="c1379-118">Il numero di tipi restituiti può essere pari a 1 (se tutti i componenti sono dello stesso tipo), ma può essere costituito da un massimo di quattro.</span><span class="sxs-lookup"><span data-stu-id="c1379-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="c1379-119">È possibile accedere a una risorsa in HLSL usando [Load](dx-graphics-hlsl-to-load.md); è possibile accedere a una trama non multicampionato anche usando uno dei metodi di esempio dell' [oggetto HLSL texture](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="c1379-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="c1379-120">Se una risorsa è associata a una fase shader, il formato della risorsa verrà convalidato in base al tipo restituito.</span><span class="sxs-lookup"><span data-stu-id="c1379-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="c1379-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1379-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c1379-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="c1379-122">Vertex Shader</span></span> | <span data-ttu-id="c1379-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="c1379-123">Geometry Shader</span></span> | <span data-ttu-id="c1379-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="c1379-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c1379-125">x</span><span class="sxs-lookup"><span data-stu-id="c1379-125">x</span></span>             | <span data-ttu-id="c1379-126">x</span><span class="sxs-lookup"><span data-stu-id="c1379-126">x</span></span>               | <span data-ttu-id="c1379-127">x</span><span class="sxs-lookup"><span data-stu-id="c1379-127">x</span></span>            |



 

<span data-ttu-id="c1379-128">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="c1379-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c1379-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1379-129">Example</span></span>

<span data-ttu-id="c1379-130">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="c1379-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c1379-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c1379-131">Minimum Shader Model</span></span>

<span data-ttu-id="c1379-132">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1379-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c1379-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c1379-133">Shader Model</span></span>                                              | <span data-ttu-id="c1379-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="c1379-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c1379-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c1379-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c1379-136">sì</span><span class="sxs-lookup"><span data-stu-id="c1379-136">yes</span></span>       |
| [<span data-ttu-id="c1379-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="c1379-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c1379-138">sì</span><span class="sxs-lookup"><span data-stu-id="c1379-138">yes</span></span>       |
| [<span data-ttu-id="c1379-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c1379-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c1379-140">sì</span><span class="sxs-lookup"><span data-stu-id="c1379-140">yes</span></span>       |
| [<span data-ttu-id="c1379-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1379-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c1379-142">no</span><span class="sxs-lookup"><span data-stu-id="c1379-142">no</span></span>        |
| [<span data-ttu-id="c1379-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1379-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c1379-144">no</span><span class="sxs-lookup"><span data-stu-id="c1379-144">no</span></span>        |
| [<span data-ttu-id="c1379-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1379-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c1379-146">no</span><span class="sxs-lookup"><span data-stu-id="c1379-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c1379-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1379-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1379-148">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1379-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





