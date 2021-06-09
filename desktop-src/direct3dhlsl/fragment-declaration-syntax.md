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
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825728"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="f0d74-103">Sintassi di dichiarazione del frammento (HLSL Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f0d74-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="f0d74-104">Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.</span><span class="sxs-lookup"><span data-stu-id="f0d74-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d74-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0d74-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="f0d74-106">dove:</span><span class="sxs-lookup"><span data-stu-id="f0d74-106">where:</span></span>



| <span data-ttu-id="f0d74-107">Valore</span><span class="sxs-lookup"><span data-stu-id="f0d74-107">Value</span></span>                  | <span data-ttu-id="f0d74-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d74-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d74-109">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="f0d74-109">fragmentKeyword</span></span>   | <span data-ttu-id="f0d74-110">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="f0d74-110">Required keyword.</span></span> <span data-ttu-id="f0d74-111">Deframmentazione pixel o vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="f0d74-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="f0d74-112">FragmentName</span><span class="sxs-lookup"><span data-stu-id="f0d74-112">FragmentName</span></span>      | <span data-ttu-id="f0d74-113">Stringa di testo ASCII che specifica il nome del frammento compilato.</span><span class="sxs-lookup"><span data-stu-id="f0d74-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="f0d74-114">frammento di \_ compilazione</span><span class="sxs-lookup"><span data-stu-id="f0d74-114">compile\_fragment</span></span> | <span data-ttu-id="f0d74-115">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="f0d74-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="f0d74-116">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="f0d74-116">shaderProfile</span></span>     | <span data-ttu-id="f0d74-117">Modello di shader con cui eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="f0d74-117">The shader model to compile against.</span></span> <span data-ttu-id="f0d74-118">Qualsiasi profilo vertex shader valido (vedere [**D3DXGetVertexShaderProfile)**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)o profilo pixel shader (vedere [**D3DXGetPixelShaderProfile).**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)</span><span class="sxs-lookup"><span data-stu-id="f0d74-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="f0d74-119">FunctionName()</span><span class="sxs-lookup"><span data-stu-id="f0d74-119">FunctionName()</span></span>    | <span data-ttu-id="f0d74-120">Nome della funzione shader, seguito da parentesi.</span><span class="sxs-lookup"><span data-stu-id="f0d74-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="f0d74-121">I parametri del frammento condiviso vengono contrassegnati aggiungendo un \_ prefisso 'r' alla relativa semantica.</span><span class="sxs-lookup"><span data-stu-id="f0d74-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="f0d74-122">In questo esempio la semantica r PosWorld e r NormalWorld identificano che questi due parametri sono parametri condivisi \_ \_ tra gli altri frammenti.</span><span class="sxs-lookup"><span data-stu-id="f0d74-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="f0d74-123">Fragment Linker era una tecnologia Microsoft Direct3D 9 in D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="f0d74-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="f0d74-124">Fragment Linker era uno strumento (Flink.exe), un'API D3DX 9 e un miglioramento HLSL.</span><span class="sxs-lookup"><span data-stu-id="f0d74-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="f0d74-125">Fragment Linker è stato eliminato a partire dalla versione di agosto 2009 di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="f0d74-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="f0d74-126">Frammento linker mai applicato a Microsoft Direct3D 10, Microsoft Direct3D 10.1 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f0d74-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f0d74-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0d74-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0d74-128">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0d74-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
