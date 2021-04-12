---
description: Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintassi della funzione Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483197"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="a70e4-103">Sintassi della funzione Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a70e4-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="a70e4-104">Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="a70e4-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a70e4-105">Syntax</span></span>

<span data-ttu-id="a70e4-106">*ReturnType* *FunctionName* ( \[ *argomento* \] )</span><span class="sxs-lookup"><span data-stu-id="a70e4-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="a70e4-107">{</span><span class="sxs-lookup"><span data-stu-id="a70e4-107">{</span></span>

<dl> <span data-ttu-id="a70e4-108">\[ *Istruzioni* \]</span><span class="sxs-lookup"><span data-stu-id="a70e4-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="a70e4-109">};</span><span class="sxs-lookup"><span data-stu-id="a70e4-109">};</span></span>



| <span data-ttu-id="a70e4-110">Nome</span><span class="sxs-lookup"><span data-stu-id="a70e4-110">Name</span></span>         | <span data-ttu-id="a70e4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a70e4-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70e4-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="a70e4-112">ReturnType</span></span>   | <span data-ttu-id="a70e4-113">Qualsiasi [tipo di HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="a70e4-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="a70e4-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="a70e4-114">FunctionName</span></span> | <span data-ttu-id="a70e4-115">Stringa ASCII che identifica in modo univoco il nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="a70e4-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="a70e4-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="a70e4-116">ArgumentList</span></span> | <span data-ttu-id="a70e4-117">Uno o più argomenti separati da virgole (vedere [argomenti della funzione (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="a70e4-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="a70e4-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a70e4-118">Statements</span></span>   | <span data-ttu-id="a70e4-119">Una o più istruzioni (vedere le [istruzioni (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) che costituiscono il corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="a70e4-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="a70e4-120">Se una funzione viene definita senza un corpo, viene considerato un prototipo; e devono essere ridefiniti con un corpo prima dell'uso.</span><span class="sxs-lookup"><span data-stu-id="a70e4-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="a70e4-121">Una funzione Effect può essere uno shader oppure può essere semplicemente una funzione chiamata da uno shader.</span><span class="sxs-lookup"><span data-stu-id="a70e4-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="a70e4-122">Una funzione viene identificata in modo univoco in base al nome, ai tipi dei relativi parametri e alla piattaforma di destinazione. è pertanto possibile eseguire l'overload delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="a70e4-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="a70e4-123">Qualsiasi funzione HLSL valida deve adattarsi a questo formato; per un elenco più dettagliato della sintassi per le funzioni HLSL, vedere [funzioni (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a70e4-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="a70e4-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="a70e4-124">Example</span></span>

<span data-ttu-id="a70e4-125">L' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) USA sia un pixel shader che un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="a70e4-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="a70e4-126">La funzione pixel shader è denominata RenderScenePS ed è illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="a70e4-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="a70e4-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a70e4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70e4-128">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="a70e4-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
