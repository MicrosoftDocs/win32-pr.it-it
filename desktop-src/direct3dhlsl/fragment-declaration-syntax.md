---
title: Sintassi di dichiarazione di frammento (Direct3D 9 HLSL)
description: Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98e609820e67cc3ede6c3e280f63513850fed364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046936"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="ff5ba-103">Sintassi di dichiarazione di frammento (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff5ba-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="ff5ba-104">Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff5ba-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="ff5ba-106">dove:</span><span class="sxs-lookup"><span data-stu-id="ff5ba-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5ba-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="ff5ba-107">fragmentKeyword</span></span>   | <span data-ttu-id="ff5ba-108">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-108">Required keyword.</span></span> <span data-ttu-id="ff5ba-109">Pixelfragment o vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="ff5ba-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="ff5ba-110">FragmentName</span></span>      | <span data-ttu-id="ff5ba-111">Stringa di testo ASCII che specifica il nome del frammento compilato.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="ff5ba-112">Compila \_ frammento</span><span class="sxs-lookup"><span data-stu-id="ff5ba-112">compile\_fragment</span></span> | <span data-ttu-id="ff5ba-113">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="ff5ba-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="ff5ba-114">shaderProfile</span></span>     | <span data-ttu-id="ff5ba-115">Modello di shader in base al quale eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-115">The shader model to compile against.</span></span> <span data-ttu-id="ff5ba-116">Qualsiasi profilo vertex shader valido (vedere [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) o profilo pixel shader (vedere [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="ff5ba-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="ff5ba-117">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="ff5ba-117">FunctionName()</span></span>    | <span data-ttu-id="ff5ba-118">Nome della funzione shader, seguito da parentesi.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="ff5ba-119">I parametri dei frammenti condivisi vengono contrassegnati con l'aggiunta di un prefisso ' r \_ ' alla relativa semantica.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="ff5ba-120">In questo esempio, la \_ semantica r PosWorld e r \_ NormalWorld identificano che questi due parametri sono parametri condivisi tra gli altri frammenti.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="ff5ba-121">Fragment linker è una tecnologia Microsoft Direct3D 9 in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="ff5ba-122">Fragment linker è uno strumento (Flink.exe), un'API D3DX 9 e un miglioramento di HLSL.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="ff5ba-123">Fragment linker è stato eliminato alla versione di agosto 2009 di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="ff5ba-124">Fragment linker non è mai stato applicato a Microsoft Direct3D 10, Microsoft Direct3D 10,1 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ff5ba-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ff5ba-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff5ba-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff5ba-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff5ba-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 