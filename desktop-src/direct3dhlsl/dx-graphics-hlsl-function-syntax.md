---
title: Sintassi di dichiarazione di funzione
description: Le funzioni HLSL vengono dichiarate con la sintassi seguente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119046"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="88da7-103">Sintassi di dichiarazione di funzione</span><span class="sxs-lookup"><span data-stu-id="88da7-103">Function Declaration Syntax</span></span>

<span data-ttu-id="88da7-104">Le funzioni HLSL vengono dichiarate con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="88da7-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="88da7-105">\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="88da7-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="88da7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88da7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88da7-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="88da7-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-108">Modificatore che ridefinisce una dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="88da7-109">**inline** è attualmente l'unico valore modificatore.</span><span class="sxs-lookup"><span data-stu-id="88da7-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="88da7-110">Il valore del modificatore deve **essere inline** perché è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="88da7-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="88da7-111">Pertanto, una funzione è inline indipendentemente dal fatto che si specifica **inline** e tutte le funzioni in HLSL siano inline.</span><span class="sxs-lookup"><span data-stu-id="88da7-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="88da7-112">Una funzione inline genera una copia del corpo della funzione (durante la compilazione) per ogni chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="88da7-113">Questa operazione viene eseguita per ridurre l'overhead della chiamata alla funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="88da7-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplan*</span><span class="sxs-lookup"><span data-stu-id="88da7-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-115">Elenco facoltativo dei piani di ritaglio, ovvero fino a 6 piani di ritaglio specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="88da7-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="88da7-116">Si tratta di un meccanismo alternativo [per SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) che funziona [sul](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) livello di funzionalità 9 x e versioni \_ successive.</span><span class="sxs-lookup"><span data-stu-id="88da7-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="88da7-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="88da7-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-118">Stringa ASCII che identifica in modo univoco il nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="88da7-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="88da7-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="88da7-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-120">Elenco di argomenti facoltativo, ovvero un elenco delimitato da virgole di [argomenti](dx-graphics-hlsl-function-parameters.md) passati in una funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="88da7-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*</span><span class="sxs-lookup"><span data-stu-id="88da7-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-122">Stringa facoltativa che identifica l'utilizzo previsto dei dati restituiti (vedere [Semantica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="88da7-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="88da7-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="88da7-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="88da7-124">Istruzioni [facoltative](dx-graphics-hlsl-statement-blocks.md) che costituiscono il corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="88da7-125">Una funzione definita senza corpo è denominata prototipo di funzione. Il corpo di una funzione prototipo deve essere definito altrove prima di poter chiamare la funzione.</span><span class="sxs-lookup"><span data-stu-id="88da7-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88da7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88da7-126">Return Value</span></span>

<span data-ttu-id="88da7-127">Il tipo restituito può essere uno qualsiasi di [questi tipi HLSL.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="88da7-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88da7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="88da7-128">Remarks</span></span>

<span data-ttu-id="88da7-129">La sintassi in questa pagina descrive quasi tutti i tipi di funzione HLSL, inclusi vertex shader, pixel shader e funzioni helper.</span><span class="sxs-lookup"><span data-stu-id="88da7-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="88da7-130">Anche se un geometry shader viene implementato anche con una funzione, la relativa sintassi è un po' più complessa, quindi esiste una pagina separata che definisce una dichiarazione di funzione [geometry shader (vedere Oggetto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="88da7-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="88da7-131">È possibile eseguire l'overload di una funzione purché le sia data una combinazione univoca di tipi di parametro e/o ordine dei parametri.</span><span class="sxs-lookup"><span data-stu-id="88da7-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="88da7-132">HLSL implementa anche una serie di funzioni intrinseche [**o incorporate.**](dx-graphics-hlsl-intrinsic-functions.md)</span><span class="sxs-lookup"><span data-stu-id="88da7-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="88da7-133">È possibile specificare piani di ritaglio specifici dell'utente con **l'attributo clipplanes.**</span><span class="sxs-lookup"><span data-stu-id="88da7-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="88da7-134">Windows applica questi piani di ritaglio a tutte le primitive disegnate.</span><span class="sxs-lookup"><span data-stu-id="88da7-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="88da7-135">**L'attributo clipplanes** funziona come [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) ma funziona su tutti i livelli di funzionalità [hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x e \_ versioni successive.</span><span class="sxs-lookup"><span data-stu-id="88da7-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="88da7-136">Per altre informazioni, vedere [Piani di ritaglio utente nell'hardware del livello di funzionalità 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)</span><span class="sxs-lookup"><span data-stu-id="88da7-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="88da7-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="88da7-137">Examples</span></span>

<span data-ttu-id="88da7-138">Questo esempio deriva da BasicHLSL10.fx [dell'esempio BasicHLSL10.](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="88da7-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


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



<span data-ttu-id="88da7-139">Questo esempio di AdvancedParticles.fx dell'esempio [AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustra l'uso di una semantica per il tipo restituito.</span><span class="sxs-lookup"><span data-stu-id="88da7-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="88da7-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88da7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88da7-141">Funzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88da7-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
