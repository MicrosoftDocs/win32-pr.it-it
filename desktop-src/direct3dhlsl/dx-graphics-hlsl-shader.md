---
title: Tipo shader
description: La sintassi per la dichiarazione di una variabile shader in un effetto è cambiata da Direct3D 9 a Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Tipo di shader HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976791"
---
# <a name="shader-type"></a><span data-ttu-id="54ea2-104">Tipo shader</span><span class="sxs-lookup"><span data-stu-id="54ea2-104">Shader Type</span></span>

<span data-ttu-id="54ea2-105">La sintassi per la dichiarazione di una variabile shader in un effetto è cambiata da Direct3D 9 a Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="54ea2-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="54ea2-106">Tipo di shader per Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="54ea2-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="54ea2-107">Dichiarare una variabile shader in un passaggio di effetto (in Direct3D 10) usando la sintassi del tipo di shader:</span><span class="sxs-lookup"><span data-stu-id="54ea2-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ea2-108">**SetPixelShader** Compilazione ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compilazione ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compilazione ( **ShaderTarget, ShaderFunction** );</span><span class="sxs-lookup"><span data-stu-id="54ea2-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="54ea2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54ea2-109">Parameters</span></span>



| <span data-ttu-id="54ea2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="54ea2-110">Item</span></span>                                                                                                                             | <span data-ttu-id="54ea2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54ea2-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ea2-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span><span class="sxs-lookup"><span data-stu-id="54ea2-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="54ea2-113">Chiamata all'API Direct3D che crea l'oggetto shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="54ea2-114">Può essere: **SetPixelShader** o **SetGeometryShader** o **SetVertexShader**.</span><span class="sxs-lookup"><span data-stu-id="54ea2-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="54ea2-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="54ea2-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="54ea2-116">Modello di shader in base al quale eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="54ea2-116">The shader model to compile against.</span></span> <span data-ttu-id="54ea2-117">Questa operazione è valida per qualsiasi destinazione, inclusi tutti gli obiettivi di Direct3D 9 più gli obiettivi di [Shader Model 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 e PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="54ea2-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="54ea2-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="54ea2-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="54ea2-119">Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che inizia l'esecuzione quando viene richiamato lo shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="54ea2-120">(...) Rappresenta gli argomenti dello shader; si tratta degli stessi argomenti passati all'API di creazione dello shader: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) o [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) o [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="54ea2-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="54ea2-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="54ea2-121">Example</span></span>

<span data-ttu-id="54ea2-122">Di seguito è riportato un esempio in cui vengono creati un vertex shader e un oggetto pixel shader, compilati per un particolare modello shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="54ea2-123">Nell'esempio Direct3D 10 non è presente alcun geometry shader, quindi il puntatore è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="54ea2-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="54ea2-124">Tipo shader per Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="54ea2-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="54ea2-125">Dichiarare una variabile shader in un passaggio di effetto (per Direct3D 9) usando la sintassi del tipo di shader:</span><span class="sxs-lookup"><span data-stu-id="54ea2-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ea2-126">**PixelShader** = Compila **ShaderTarget ShaderFunction (...); VertexShader** = Compila **ShaderTarget ShaderFunction (...);**</span><span class="sxs-lookup"><span data-stu-id="54ea2-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="54ea2-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="54ea2-127">Parameters</span></span>



| <span data-ttu-id="54ea2-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="54ea2-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="54ea2-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54ea2-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ea2-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span><span class="sxs-lookup"><span data-stu-id="54ea2-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="54ea2-131">Variabile shader che rappresenta lo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="54ea2-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="54ea2-132">Può essere: **PixelShader** o **vertexshader**.</span><span class="sxs-lookup"><span data-stu-id="54ea2-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="54ea2-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="54ea2-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="54ea2-134">[Modello di shader](dx-graphics-hlsl-models.md) in base al quale eseguire la compilazione. dipende dal tipo di variabile shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="54ea2-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span><span class="sxs-lookup"><span data-stu-id="54ea2-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="54ea2-136">Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che inizia l'esecuzione quando viene richiamato lo shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="54ea2-137">(...) Rappresenta gli argomenti dello shader; si tratta degli stessi argomenti passati all'API di creazione dello shader: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) o [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span><span class="sxs-lookup"><span data-stu-id="54ea2-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="54ea2-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="54ea2-138">Example</span></span>

<span data-ttu-id="54ea2-139">Di seguito è riportato un esempio di vertex shader e pixel shader oggetto, compilato per un particolare modello shader.</span><span class="sxs-lookup"><span data-stu-id="54ea2-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="54ea2-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54ea2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ea2-141">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54ea2-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

