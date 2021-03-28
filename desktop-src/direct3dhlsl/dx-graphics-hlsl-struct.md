---
title: Tipo struct
description: Tipo struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992904"
---
# <a name="struct-type"></a><span data-ttu-id="23fdf-104">Tipo struct</span><span class="sxs-lookup"><span data-stu-id="23fdf-104">Struct Type</span></span>

<span data-ttu-id="23fdf-105">Utilizzare la sintassi seguente per dichiarare una struttura utilizzando HLSL.</span><span class="sxs-lookup"><span data-stu-id="23fdf-105">Use the following syntax to declare a structure using HLSL.</span></span>



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fdf-106">*nome* struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *memberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="23fdf-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="23fdf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="23fdf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fdf-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="23fdf-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="23fdf-109">Stringa ASCII che identifica in modo univoco il nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="23fdf-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="23fdf-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="23fdf-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="23fdf-111">Modificatore facoltativo che specifica un tipo di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="23fdf-112">Per informazioni dettagliate, vedere la [sezione Osservazioni](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="23fdf-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="23fdf-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ di *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="23fdf-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="23fdf-114">Tipo di membro con una matrice di colonne (*C*) di riga facoltativa (*R*).</span><span class="sxs-lookup"><span data-stu-id="23fdf-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="23fdf-115">Una struttura contiene almeno un elemento. Se contiene più di un elemento, gli elementi sono tutti dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="23fdf-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="23fdf-116">Il numero di righe e colonne è costituito da interi senza segno compreso tra 1 e 4 inclusi.</span><span class="sxs-lookup"><span data-stu-id="23fdf-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="23fdf-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span><span class="sxs-lookup"><span data-stu-id="23fdf-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="23fdf-118">Stringa ASCII che identifica in modo univoco il nome del membro.</span><span class="sxs-lookup"><span data-stu-id="23fdf-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23fdf-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="23fdf-119">Remarks</span></span>

<span data-ttu-id="23fdf-120">È possibile specificare un modificatore di interpolazione per qualsiasi membro della struttura o per un argomento di una funzione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="23fdf-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="23fdf-121">Se un modificatore viene visualizzato in entrambe le posizioni, il modificatore esterno (il modificatore di argomento pixel shader) sovraregola il modificatore interno (il modificatore di struttura).</span><span class="sxs-lookup"><span data-stu-id="23fdf-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="23fdf-122">Quando si compila uno shader o un effetto, il compilatore shader comprime i membri della struttura in base alle [regole di compressione HLSL](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="23fdf-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="23fdf-123">Modificatori di interpolazione introdotti in Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="23fdf-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="23fdf-124">Gli output di vertex shader usati per gli input pixel shader vengono interpolati linearmente per ottenere i valori per pixel durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="23fdf-125">Per impostare il metodo di interpolazione, usare uno dei valori seguenti, supportati in [Shader Model 4](dx-graphics-hlsl-sm4.md) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="23fdf-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="23fdf-126">Il modificatore viene ignorato in qualsiasi output del vertex shader che non viene usato come input pixel shader.</span><span class="sxs-lookup"><span data-stu-id="23fdf-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="23fdf-127">Modificatore di interpolazione</span><span class="sxs-lookup"><span data-stu-id="23fdf-127">Interpolation Modifier</span></span> | <span data-ttu-id="23fdf-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23fdf-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fdf-129">**lineare**</span><span class="sxs-lookup"><span data-stu-id="23fdf-129">**linear**</span></span>             | <span data-ttu-id="23fdf-130">Interpolazione tra input shader; **Linear** è il valore predefinito se non è specificato alcun modificatore di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="23fdf-131">**centro**</span><span class="sxs-lookup"><span data-stu-id="23fdf-131">**centroid**</span></span>           | <span data-ttu-id="23fdf-132">Interpolare tra i campioni che si trovano in un punto qualsiasi all'interno dell'area coperta del pixel (potrebbe essere necessario estrapolare i punti finali da un pixel Center).</span><span class="sxs-lookup"><span data-stu-id="23fdf-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="23fdf-133">Il campionamento centrale può migliorare l'anti-aliasing se un pixel è parzialmente analizzato (anche se il pixel Center non è coperto).</span><span class="sxs-lookup"><span data-stu-id="23fdf-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="23fdf-134">Il modificatore di **baricentro** deve essere combinato con il modificatore **Linear** o **noperspective** .</span><span class="sxs-lookup"><span data-stu-id="23fdf-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="23fdf-135">**interpolazione**</span><span class="sxs-lookup"><span data-stu-id="23fdf-135">**nointerpolation**</span></span>    | <span data-ttu-id="23fdf-136">Non eseguire l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="23fdf-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="23fdf-137">**noperspective**</span></span>      | <span data-ttu-id="23fdf-138">Non eseguire la correzione della prospettiva durante l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="23fdf-139">Il modificatore **noperspective** può essere combinato con il modificatore di **baricentro** .</span><span class="sxs-lookup"><span data-stu-id="23fdf-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="23fdf-140">**esempio**</span><span class="sxs-lookup"><span data-stu-id="23fdf-140">**sample**</span></span>             | <span data-ttu-id="23fdf-141">**Disponibile nel modello di shader 4,1 e versioni successive** Interpolare in un percorso di esempio anziché in un pixel Center.</span><span class="sxs-lookup"><span data-stu-id="23fdf-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="23fdf-142">In questo modo il pixel shader viene eseguito per campione anziché per pixel.</span><span class="sxs-lookup"><span data-stu-id="23fdf-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="23fdf-143">Un altro modo per eseguire l'esecuzione per campione è avere un input con la [semantica SV \_ SampleIndex](dx-graphics-hlsl-semantics.md), che indica l'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="23fdf-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="23fdf-144">Solo gli input con l' **esempio** specificato (o inserendo SV \_ SampleIndex) variano tra le chiamate dello shader nel pixel, mentre altri input che non specificano i modificatori (ad esempio, se si combinano i modificatori su input diversi) ancora interpolano in corrispondenza del pixel Center.</span><span class="sxs-lookup"><span data-stu-id="23fdf-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="23fdf-145">Per ogni esempio incluso nel pixel si verificano sia la chiamata del pixel shader che il test di profondità/stencil.</span><span class="sxs-lookup"><span data-stu-id="23fdf-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="23fdf-146">Questa operazione è talvolta nota come *supercampionamento*.</span><span class="sxs-lookup"><span data-stu-id="23fdf-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="23fdf-147">Al contrario, in assenza della chiamata di frequenza di esempio, nota come *multicampionamento*, il pixel shader viene richiamato una volta per ogni pixel indipendentemente dal numero di campioni analizzati, mentre il test di profondità/stencil si verifica alla frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="23fdf-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="23fdf-148">Entrambe le modalità forniscono l'anti-aliasing Edge equivalente.</span><span class="sxs-lookup"><span data-stu-id="23fdf-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="23fdf-149">Tuttavia, il supercampionamento offre una migliore qualità di ombreggiatura richiamando il pixel shader più spesso.</span><span class="sxs-lookup"><span data-stu-id="23fdf-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="23fdf-150">1. Quando si usa un tipo int/uint, l'unica opzione valida è **Interpolation**.</span><span class="sxs-lookup"><span data-stu-id="23fdf-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="23fdf-151">È possibile applicare i modificatori di interpolazione a membri della struttura o [argomenti di funzione](dx-graphics-hlsl-function-parameters.md)o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="23fdf-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="23fdf-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="23fdf-152">Examples</span></span>

<span data-ttu-id="23fdf-153">Di seguito sono riportate alcune dichiarazioni di struttura di esempio.</span><span class="sxs-lookup"><span data-stu-id="23fdf-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="23fdf-154">Questa dichiarazione include una matrice.</span><span class="sxs-lookup"><span data-stu-id="23fdf-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="23fdf-155">Questa dichiarazione include un modificatore di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="23fdf-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="23fdf-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23fdf-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fdf-157">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23fdf-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





