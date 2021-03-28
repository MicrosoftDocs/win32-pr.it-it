---
title: tex2Dlod
description: Campiona una trama 2D con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL tex2Dlod
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976647"
---
# <a name="tex2dlod"></a><span data-ttu-id="f2c21-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="f2c21-105">tex2Dlod</span></span>

<span data-ttu-id="f2c21-106">Campiona una trama 2D con mipmap.</span><span class="sxs-lookup"><span data-stu-id="f2c21-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="f2c21-107">Il mipmap LOD è specificato in t.w.</span><span class="sxs-lookup"><span data-stu-id="f2c21-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="f2c21-108">tex2Dlod RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="f2c21-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="f2c21-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2c21-109">Parameters</span></span>



| <span data-ttu-id="f2c21-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2c21-110">Item</span></span>                                                   | <span data-ttu-id="f2c21-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2c21-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f2c21-112"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="f2c21-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="f2c21-113">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="f2c21-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="f2c21-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="f2c21-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="f2c21-115">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="f2c21-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f2c21-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2c21-116">Return Value</span></span>

<span data-ttu-id="f2c21-117">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="f2c21-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="f2c21-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="f2c21-118">Type Description</span></span>



| <span data-ttu-id="f2c21-119">Nome</span><span class="sxs-lookup"><span data-stu-id="f2c21-119">Name</span></span> | <span data-ttu-id="f2c21-120">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="f2c21-120">In/Out</span></span> | [<span data-ttu-id="f2c21-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="f2c21-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="f2c21-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="f2c21-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f2c21-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f2c21-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="f2c21-124">s</span><span class="sxs-lookup"><span data-stu-id="f2c21-124">s</span></span>    | <span data-ttu-id="f2c21-125">in ingresso</span><span class="sxs-lookup"><span data-stu-id="f2c21-125">in</span></span>     | [<span data-ttu-id="f2c21-126">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="f2c21-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2c21-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="f2c21-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="f2c21-128">1</span><span class="sxs-lookup"><span data-stu-id="f2c21-128">1</span></span>    |
| <span data-ttu-id="f2c21-129">u</span><span class="sxs-lookup"><span data-stu-id="f2c21-129">t</span></span>    | <span data-ttu-id="f2c21-130">in ingresso</span><span class="sxs-lookup"><span data-stu-id="f2c21-130">in</span></span>     | [<span data-ttu-id="f2c21-131">**vettore**</span><span class="sxs-lookup"><span data-stu-id="f2c21-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2c21-132">**float**</span><span class="sxs-lookup"><span data-stu-id="f2c21-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f2c21-133">4</span><span class="sxs-lookup"><span data-stu-id="f2c21-133">4</span></span>    |
| <span data-ttu-id="f2c21-134">RET</span><span class="sxs-lookup"><span data-stu-id="f2c21-134">ret</span></span>  | <span data-ttu-id="f2c21-135">in uscita</span><span class="sxs-lookup"><span data-stu-id="f2c21-135">out</span></span>    | [<span data-ttu-id="f2c21-136">**vettore**</span><span class="sxs-lookup"><span data-stu-id="f2c21-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2c21-137">**float**</span><span class="sxs-lookup"><span data-stu-id="f2c21-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f2c21-138">4</span><span class="sxs-lookup"><span data-stu-id="f2c21-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f2c21-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f2c21-139">Minimum Shader Model</span></span>

<span data-ttu-id="f2c21-140">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2c21-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2c21-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f2c21-141">Shader Model</span></span>                                                                       | <span data-ttu-id="f2c21-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="f2c21-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f2c21-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="f2c21-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="f2c21-144">sì</span><span class="sxs-lookup"><span data-stu-id="f2c21-144">yes</span></span>       |
| [<span data-ttu-id="f2c21-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2c21-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="f2c21-146">no</span><span class="sxs-lookup"><span data-stu-id="f2c21-146">no</span></span>        |
| [<span data-ttu-id="f2c21-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2c21-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f2c21-148">no</span><span class="sxs-lookup"><span data-stu-id="f2c21-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="f2c21-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2c21-149">Remarks</span></span>

<span data-ttu-id="f2c21-150">A partire da Direct3D 10, è possibile usare la nuova sintassi HLSL per accedere alle trame e ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="f2c21-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="f2c21-151">È possibile sostituire le funzioni di ricerca di trama di tipo intrinseco, ad esempio **tex2Dlod**, con uno stile più orientato agli oggetti.</span><span class="sxs-lookup"><span data-stu-id="f2c21-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="f2c21-152">In questo stile orientato a oggetti, le trame vengono disaccoppiate dai sampler e dispongono di metodi per il caricamento e il campionamento.</span><span class="sxs-lookup"><span data-stu-id="f2c21-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="f2c21-153">Per campionare una trama 2D, invece di usare **tex2Dlod** come nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="f2c21-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="f2c21-154">Usare il metodo [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) di un [**oggetto texture**](dx-graphics-hlsl-to-type.md) come nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="f2c21-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="f2c21-155">Per utilizzare le funzioni di ricerca di trama di tipo intrinseco, ad esempio **tex2Dlod**, con [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive, utilizzare D3DCOMPILE per consentire la compilazione con la [**\_ \_ \_ compatibilità**](d3dcompile-constants.md) con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="f2c21-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="f2c21-156">Tuttavia, se si desidera destinare il modello Shader 4 e versioni successive (anche [ \* \_ 4 \_ 0 \_ livello \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) con il codice di stile orientato a oggetti più recente, eseguire la migrazione alla sintassi HLSL più recente.</span><span class="sxs-lookup"><span data-stu-id="f2c21-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2c21-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2c21-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c21-158">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f2c21-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

