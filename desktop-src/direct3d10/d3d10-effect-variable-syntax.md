---
description: Una variabile Effect viene dichiarata con la sintassi seguente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintassi della variabile Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401449"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="ebea0-103">Sintassi della variabile Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ebea0-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="ebea0-104">Una variabile Effect viene dichiarata con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="ebea0-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebea0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebea0-105">Syntax</span></span>

<span data-ttu-id="ebea0-106">*DataType* *variablename* \[ : *semanticname* \]  <  *annotazioni* >;</span><span class="sxs-lookup"><span data-stu-id="ebea0-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="ebea0-107">Nome</span><span class="sxs-lookup"><span data-stu-id="ebea0-107">Name</span></span>         | <span data-ttu-id="ebea0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebea0-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebea0-109">DataType</span><span class="sxs-lookup"><span data-stu-id="ebea0-109">DataType</span></span>     | <span data-ttu-id="ebea0-110">Qualsiasi tipo di [trama](../direct3dhlsl/dx-graphics-hlsl-to-type.md) o di [base](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="ebea0-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="ebea0-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="ebea0-111">VariableName</span></span> | <span data-ttu-id="ebea0-112">Stringa ASCII che identifica in modo univoco il nome della variabile di effetto.</span><span class="sxs-lookup"><span data-stu-id="ebea0-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="ebea0-113">Semanticname</span><span class="sxs-lookup"><span data-stu-id="ebea0-113">SemanticName</span></span> | <span data-ttu-id="ebea0-114">Stringa ASCII che indica informazioni aggiuntive sulla modalità di utilizzo di una variabile.</span><span class="sxs-lookup"><span data-stu-id="ebea0-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="ebea0-115">Una semantica è una stringa ASCII che può essere un valore di sistema predefinito o una stringa utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ebea0-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="ebea0-116">annotazioni</span><span class="sxs-lookup"><span data-stu-id="ebea0-116">Annotations</span></span>  | <span data-ttu-id="ebea0-117">Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="ebea0-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="ebea0-118">Per la sintassi, vedere [sintassi delle annotazioni (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ebea0-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="ebea0-119">Una variabile di effetto dichiarata al di fuori di tutte le funzioni è considerata globale nell'ambito. le variabili dichiarate all'interno di una funzione sono locali a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="ebea0-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="ebea0-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="ebea0-120">Example</span></span>

<span data-ttu-id="ebea0-121">L' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variabili globali senza semantica per colori materiali, proprietà chiare e matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="ebea0-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="ebea0-122">Questo esempio illustra le variabili di effetto globale.</span><span class="sxs-lookup"><span data-stu-id="ebea0-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="ebea0-123">Questo esempio illustra le variabili di effetto locali a una funzione shader.</span><span class="sxs-lookup"><span data-stu-id="ebea0-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="ebea0-124">In questo esempio vengono illustrati i parametri della funzione con semantica.</span><span class="sxs-lookup"><span data-stu-id="ebea0-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="ebea0-125">In questo esempio viene illustrata la dichiarazione di una variabile di trama.</span><span class="sxs-lookup"><span data-stu-id="ebea0-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="ebea0-126">Campionamento di una trama viene eseguita con un campionatore di trame.</span><span class="sxs-lookup"><span data-stu-id="ebea0-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="ebea0-127">Per configurare un campionatore in un effetto, vedere il [tipo di campionatore](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ebea0-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebea0-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebea0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebea0-129">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="ebea0-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
