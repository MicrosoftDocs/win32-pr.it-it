---
title: Sintassi di dichiarazione del frammento (HLSL Direct3D 9)
description: Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998308"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="2900c-103">Sintassi di dichiarazione del frammento (HLSL Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2900c-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="2900c-104">Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.</span><span class="sxs-lookup"><span data-stu-id="2900c-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2900c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2900c-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="2900c-106">dove:</span><span class="sxs-lookup"><span data-stu-id="2900c-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2900c-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="2900c-107">fragmentKeyword</span></span>   | <span data-ttu-id="2900c-108">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="2900c-108">Required keyword.</span></span> <span data-ttu-id="2900c-109">Deframmentazione pixel o vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="2900c-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="2900c-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="2900c-110">FragmentName</span></span>      | <span data-ttu-id="2900c-111">Stringa di testo ASCII che specifica il nome del frammento compilato.</span><span class="sxs-lookup"><span data-stu-id="2900c-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="2900c-112">frammento di \_ compilazione</span><span class="sxs-lookup"><span data-stu-id="2900c-112">compile\_fragment</span></span> | <span data-ttu-id="2900c-113">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="2900c-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="2900c-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="2900c-114">shaderProfile</span></span>     | <span data-ttu-id="2900c-115">Modello di shader con cui eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="2900c-115">The shader model to compile against.</span></span> <span data-ttu-id="2900c-116">Qualsiasi profilo vertex shader valido (vedere [**D3DXGetVertexShaderProfile)**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)o profilo pixel shader (vedere [**D3DXGetPixelShaderProfile).**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)</span><span class="sxs-lookup"><span data-stu-id="2900c-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="2900c-117">FunctionName()</span><span class="sxs-lookup"><span data-stu-id="2900c-117">FunctionName()</span></span>    | <span data-ttu-id="2900c-118">Nome della funzione shader, seguito da parentesi.</span><span class="sxs-lookup"><span data-stu-id="2900c-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="2900c-119">I parametri del frammento condiviso vengono contrassegnati aggiungendo un \_ prefisso 'r' alla relativa semantica.</span><span class="sxs-lookup"><span data-stu-id="2900c-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="2900c-120">In questo esempio la semantica r PosWorld e r NormalWorld identificano che questi due parametri sono parametri condivisi \_ \_ tra gli altri frammenti.</span><span class="sxs-lookup"><span data-stu-id="2900c-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="2900c-121">Fragment Linker era una tecnologia Microsoft Direct3D 9 in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="2900c-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="2900c-122">Fragment Linker era uno strumento (Flink.exe), un'API D3DX 9 e un miglioramento HLSL.</span><span class="sxs-lookup"><span data-stu-id="2900c-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="2900c-123">Fragment Linker è stato eliminato a partire dalla versione di agosto 2009 di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="2900c-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="2900c-124">Frammento linker mai applicato a Microsoft Direct3D 10, Microsoft Direct3D 10.1 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2900c-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2900c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2900c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2900c-126">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2900c-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
