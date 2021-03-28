---
title: Sintassi di dichiarazione di funzione
description: Le funzioni HLSL sono dichiarate con la sintassi seguente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399570"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="67277-103">Sintassi di dichiarazione di funzione</span><span class="sxs-lookup"><span data-stu-id="67277-103">Function Declaration Syntax</span></span>

<span data-ttu-id="67277-104">Le funzioni HLSL sono dichiarate con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="67277-104">HLSL functions are declared with the following syntax.</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67277-105">\[*StorageClass* \] \[clipplanes () \] \[ nome preciso del \] \_ valore restituito  ( \[ *argomento argument* \] ) \[ : *semantica* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="67277-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="67277-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67277-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67277-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="67277-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="67277-108">Modificatore che ridefinisce una dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="67277-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="67277-109">**inline** è attualmente l'unico valore del modificatore.</span><span class="sxs-lookup"><span data-stu-id="67277-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="67277-110">Il valore del modificatore deve essere **inline** perché è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="67277-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="67277-111">Una funzione è quindi inline indipendentemente dal fatto che sia stato specificato **inline** e che tutte le funzioni in HLSL siano inline.</span><span class="sxs-lookup"><span data-stu-id="67277-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="67277-112">Una funzione inline genera una copia del corpo della funzione (durante la compilazione) per ogni chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="67277-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="67277-113">Questa operazione viene eseguita per ridurre l'overhead associato alla chiamata alla funzione.</span><span class="sxs-lookup"><span data-stu-id="67277-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="67277-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="67277-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="67277-115">Elenco facoltativo di piani di ritaglio, ovvero fino a 6 piani di ritaglio specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="67277-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="67277-116">Si tratta di un meccanismo alternativo per [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) che funziona a [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="67277-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="67277-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="67277-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="67277-118">Stringa ASCII che identifica in modo univoco il nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="67277-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="67277-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="67277-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="67277-120">Elenco di argomenti facoltativo, ovvero un elenco delimitato da virgole di [argomenti](dx-graphics-hlsl-function-parameters.md) passati in una funzione.</span><span class="sxs-lookup"><span data-stu-id="67277-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="67277-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*</span><span class="sxs-lookup"><span data-stu-id="67277-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="67277-122">Stringa facoltativa che identifica l'utilizzo previsto dei dati restituiti (vedere [semantica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="67277-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="67277-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="67277-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="67277-124">[Istruzioni](dx-graphics-hlsl-statement-blocks.md) facoltative che compongono il corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="67277-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="67277-125">Una funzione definita senza un corpo viene chiamata prototipo di funzione. il corpo di una funzione Prototype deve essere definito altrove prima che la funzione possa essere chiamata.</span><span class="sxs-lookup"><span data-stu-id="67277-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67277-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67277-126">Return Value</span></span>

<span data-ttu-id="67277-127">Il tipo restituito può essere uno di questi [tipi di HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="67277-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="67277-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="67277-128">Remarks</span></span>

<span data-ttu-id="67277-129">La sintassi in questa pagina descrive quasi tutti i tipi di funzione HLSL, inclusi vertex shader, pixel shader e funzioni helper.</span><span class="sxs-lookup"><span data-stu-id="67277-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="67277-130">Anche se un geometry shader viene implementato con una funzione, la sua sintassi è leggermente più complicata, quindi esiste una pagina separata che definisce una dichiarazione di funzione geometry shader (vedere [oggetto Geometry-shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="67277-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="67277-131">Una funzione può essere sottoposto a overload purché venga fornita una combinazione univoca di tipi di parametro e/o ordine dei parametri.</span><span class="sxs-lookup"><span data-stu-id="67277-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="67277-132">HLSL implementa anche una serie di [**funzioni intrinseche**](dx-graphics-hlsl-intrinsic-functions.md)o predefinite.</span><span class="sxs-lookup"><span data-stu-id="67277-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="67277-133">È possibile specificare i piani di ritaglio specifici dell'utente con l'attributo **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="67277-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="67277-134">Windows applica questi piani di ritaglio a tutte le primitive disegnate.</span><span class="sxs-lookup"><span data-stu-id="67277-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="67277-135">L'attributo **clipplanes** funziona come [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) ma funziona su tutti i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) hardware 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="67277-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="67277-136">Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span><span class="sxs-lookup"><span data-stu-id="67277-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="67277-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="67277-137">Examples</span></span>

<span data-ttu-id="67277-138">Questo esempio è riportato da BasicHLSL10. FX dell' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="67277-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="67277-139">Questo esempio di AdvancedParticles. FX dell' [esempio AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustra l'uso di una semantica per il tipo restituito.</span><span class="sxs-lookup"><span data-stu-id="67277-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="67277-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67277-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67277-141">Funzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67277-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 