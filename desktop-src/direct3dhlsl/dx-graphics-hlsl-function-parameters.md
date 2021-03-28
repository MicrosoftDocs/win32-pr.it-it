---
title: Argomenti della funzione
description: Una funzione accetta uno o più argomenti di input. utilizzare la sintassi seguente per dichiarare ogni argomento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398501"
---
# <a name="function-arguments"></a><span data-ttu-id="c2856-103">Argomenti della funzione</span><span class="sxs-lookup"><span data-stu-id="c2856-103">Function Arguments</span></span>

<span data-ttu-id="c2856-104">Una funzione accetta uno o più argomenti di input. utilizzare la sintassi seguente per dichiarare ogni argomento.</span><span class="sxs-lookup"><span data-stu-id="c2856-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2856-105">**\[Nome del tipo di InputModifier \] \[ : Semantic \] \[ InterpolationModifier \] \[ = initializers\]**</span><span class="sxs-lookup"><span data-stu-id="c2856-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="c2856-106">\[\]Nome tipo modificatore \[ : Semantic \] \[ : modificatore interpolazione \] \[ = inizializzatore/i\]</span><span class="sxs-lookup"><span data-stu-id="c2856-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="c2856-107">Se sono presenti più argomenti della funzione, sono separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="c2856-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2856-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2856-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2856-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2856-109">Item</span></span></th>
<th><span data-ttu-id="c2856-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2856-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2856-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="c2856-112">Termine facoltativo che identifica un argomento come input, output o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c2856-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2856-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c2856-113">Value</span></span></td>
<td><span data-ttu-id="c2856-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2856-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2856-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="c2856-116">Solo input</span><span class="sxs-lookup"><span data-stu-id="c2856-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2856-117"><strong>Inout</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="c2856-118">Input e output</span><span class="sxs-lookup"><span data-stu-id="c2856-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2856-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="c2856-120">Solo output</span><span class="sxs-lookup"><span data-stu-id="c2856-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2856-121"><strong>Uniform</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="c2856-122">Input solo di dati costanti</span><span class="sxs-lookup"><span data-stu-id="c2856-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="c2856-123">I parametri vengono sempre passati per valore.</span><span class="sxs-lookup"><span data-stu-id="c2856-123">Parameters are always passed by value.</span></span> <span data-ttu-id="c2856-124">in indica che il valore del parametro deve essere copiato dall'applicazione chiamante prima che venga avviata la funzione.</span><span class="sxs-lookup"><span data-stu-id="c2856-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="c2856-125">out indica che l'ultimo valore del parametro deve essere copiato e restituito all'applicazione chiamante quando la funzione restituisce.</span><span class="sxs-lookup"><span data-stu-id="c2856-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="c2856-126">Inout è una sintassi abbreviata per specificare entrambi.</span><span class="sxs-lookup"><span data-stu-id="c2856-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="c2856-127">Un valore uniforme deriva da un registro costante. ogni vertex shader o pixel shader chiamata Visualizza lo stesso valore iniziale per una variabile uniforme.</span><span class="sxs-lookup"><span data-stu-id="c2856-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="c2856-128">Le variabili globali vengono considerate come se fossero dichiarate uniformi.</span><span class="sxs-lookup"><span data-stu-id="c2856-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="c2856-129">Per le funzioni non di primo livello, Uniform è sinonimo di <strong>in</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2856-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="c2856-130">Se non viene specificato alcun utilizzo del parametro, si presuppone che l'utilizzo del parametro sia <strong>in</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2856-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2856-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c2856-132">Tipo di argomento; può essere qualsiasi <a href="dx-graphics-hlsl-data-types.md">tipo</a>HLSL valido.</span><span class="sxs-lookup"><span data-stu-id="c2856-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2856-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c2856-134">Stringa ASCII che identifica in modo univoco il nome della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="c2856-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2856-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantica</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="c2856-136">Stringa facoltativa che identifica l'utilizzo previsto dei dati (vedere <a href="dx-graphics-hlsl-semantics.md">semantica (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="c2856-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2856-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="c2856-138"><a href="dx-graphics-hlsl-struct.md">Modificatore di interpolazione</a> facoltativo che consente a uno shader di determinare il metodo di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="c2856-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="c2856-139">Un modificatore di interpolazione su un argomento della funzione si applica solo a un argomento usato come input per una funzione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c2856-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2856-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inizializzatori</strong></span><span class="sxs-lookup"><span data-stu-id="c2856-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="c2856-141">Valori facoltativi per l'inizializzazione. per inizializzare i tipi di dati multicomponente sono necessari più valori.</span><span class="sxs-lookup"><span data-stu-id="c2856-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c2856-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2856-142">Remarks</span></span>

<span data-ttu-id="c2856-143">Gli argomenti della funzione sono elencati in un elenco di argomenti delimitati da virgole in una dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="c2856-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="c2856-144">Come nelle funzioni C, ogni argomento deve avere un nome di parametro e un tipo dichiarato; un argomento di una funzione HLSL può includere facoltativamente una semantica, un valore iniziale e un input pixel shader può includere un tipo di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="c2856-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="c2856-145">Il *tipo* di un argomento della funzione può essere una struttura, che può includere un modificatore di interpolazione per singolo membro.</span><span class="sxs-lookup"><span data-stu-id="c2856-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="c2856-146">Se l'argomento della funzione dispone anche di un modificatore di interpolazione, il modificatore di argomenti della funzione sostituisce i modificatori di interpolazione dichiarati nel tipo</span><span class="sxs-lookup"><span data-stu-id="c2856-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="c2856-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2856-147">Examples</span></span>

<span data-ttu-id="c2856-148">Questo esempio (dall' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustra gli input uniformi e non uniformi a una funzione vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c2856-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="c2856-149">Questo esempio (dall' [esempio ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) usa una struttura di input per passare argomenti a una funzione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c2856-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="c2856-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2856-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2856-151">Funzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2856-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





