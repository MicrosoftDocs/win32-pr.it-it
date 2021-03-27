---
title: Sintassi della funzione Effect (Direct3D 11)
description: Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727378"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="92ffe-103">Sintassi della funzione Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="92ffe-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="92ffe-104">Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="92ffe-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ffe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92ffe-105">Syntax</span></span>

<span data-ttu-id="92ffe-106">*ReturnType* *FunctionName* ( \[ *argomento* \] )</span><span class="sxs-lookup"><span data-stu-id="92ffe-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="92ffe-107">{</span><span class="sxs-lookup"><span data-stu-id="92ffe-107">{</span></span>

<dl> <span data-ttu-id="92ffe-108">\[ *Istruzioni* \]</span><span class="sxs-lookup"><span data-stu-id="92ffe-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="92ffe-109">};</span><span class="sxs-lookup"><span data-stu-id="92ffe-109">};</span></span>



| <span data-ttu-id="92ffe-110">Nome</span><span class="sxs-lookup"><span data-stu-id="92ffe-110">Name</span></span>         | <span data-ttu-id="92ffe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92ffe-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ffe-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="92ffe-112">ReturnType</span></span>   | <span data-ttu-id="92ffe-113">Qualsiasi [tipo di HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="92ffe-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="92ffe-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="92ffe-114">FunctionName</span></span> | <span data-ttu-id="92ffe-115">Stringa ASCII che identifica in modo univoco il nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="92ffe-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="92ffe-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="92ffe-116">ArgumentList</span></span> | <span data-ttu-id="92ffe-117">Uno o più argomenti separati da virgole (vedere [argomenti della funzione (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="92ffe-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="92ffe-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="92ffe-118">Statements</span></span>   | <span data-ttu-id="92ffe-119">Una o più istruzioni (vedere le [istruzioni (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) che costituiscono il corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="92ffe-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="92ffe-120">Se una funzione viene definita senza un corpo, viene considerato un prototipo; e devono essere ridefiniti con un corpo prima dell'uso.</span><span class="sxs-lookup"><span data-stu-id="92ffe-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="92ffe-121">Una funzione Effect può essere uno shader oppure può essere semplicemente una funzione chiamata da uno shader.</span><span class="sxs-lookup"><span data-stu-id="92ffe-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="92ffe-122">Una funzione viene identificata in modo univoco in base al nome, ai tipi dei relativi parametri e alla piattaforma di destinazione. è pertanto possibile eseguire l'overload delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="92ffe-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="92ffe-123">Qualsiasi funzione HLSL valida deve adattarsi a questo formato; per un elenco più dettagliato della sintassi per le funzioni HLSL, vedere [funzioni (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="92ffe-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="92ffe-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="92ffe-124">Example</span></span>

<span data-ttu-id="92ffe-125">Di seguito è riportato un esempio di una funzione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="92ffe-125">The following is an example of a pixel shader function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="92ffe-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92ffe-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ffe-127">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="92ffe-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 