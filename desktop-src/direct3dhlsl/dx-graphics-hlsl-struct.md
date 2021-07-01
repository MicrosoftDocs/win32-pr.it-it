---
title: Tipo struct
description: Tipo struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo di struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119096"
---
# <a name="struct-type"></a><span data-ttu-id="e894c-104">Tipo struct</span><span class="sxs-lookup"><span data-stu-id="e894c-104">Struct Type</span></span>

<span data-ttu-id="e894c-105">Usare la sintassi seguente per dichiarare una struttura usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="e894c-105">Use the following syntax to declare a structure using HLSL.</span></span>

<span data-ttu-id="e894c-106">struct *Name*{ \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="e894c-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e894c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e894c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e894c-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="e894c-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="e894c-109">Stringa ASCII che identifica in modo univoco il nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="e894c-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="e894c-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolazioneModifier*\]</span><span class="sxs-lookup"><span data-stu-id="e894c-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="e894c-111">Modificatore facoltativo che specifica un tipo di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="e894c-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="e894c-112">Per [informazioni dettagliate, vedere](#remarks) Note.</span><span class="sxs-lookup"><span data-stu-id="e894c-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e894c-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="e894c-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="e894c-114">Tipo di membro con una riga facoltativa (*R*) x colonna (*C*) dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="e894c-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="e894c-115">Una struttura contiene almeno un elemento. se contiene più di un elemento, gli elementi sono tutti dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="e894c-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="e894c-116">Il numero di righe e colonne è unsigned integer compreso tra 1 e 4 inclusi.</span><span class="sxs-lookup"><span data-stu-id="e894c-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="e894c-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*</span><span class="sxs-lookup"><span data-stu-id="e894c-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="e894c-118">Stringa ASCII che identifica in modo univoco il nome del membro.</span><span class="sxs-lookup"><span data-stu-id="e894c-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e894c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e894c-119">Remarks</span></span>

<span data-ttu-id="e894c-120">Un modificatore di interpolazione può essere specificato in qualsiasi membro della struttura o in un argomento di una pixel shader funzione.</span><span class="sxs-lookup"><span data-stu-id="e894c-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="e894c-121">Se un modificatore viene visualizzato in entrambe le posizioni, il modificatore outside (modificatore di argomento pixel shader) prevale sul modificatore inside (modificatore structure).</span><span class="sxs-lookup"><span data-stu-id="e894c-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="e894c-122">Quando si compila uno shader o un effetto, il compilatore shader esegue il pacchetto dei membri della struttura in base alle [regole di pacchetto HLSL.](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="e894c-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="e894c-123">Modificatori di interpolazione introdotti nel modello shader 4</span><span class="sxs-lookup"><span data-stu-id="e894c-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="e894c-124">Gli output di vertex shader usati per pixel shader input vengono interpolati in modo lineare per ottenere valori per pixel durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="e894c-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="e894c-125">Per impostare il metodo di interpolazione, usare uno dei valori seguenti, supportati nel modello [shader 4](dx-graphics-hlsl-sm4.md) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e894c-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="e894c-126">Il modificatore viene ignorato in qualsiasi output di vertex shader che non viene usato come input pixel shader di input.</span><span class="sxs-lookup"><span data-stu-id="e894c-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="e894c-127">Modificatore di interpolazione</span><span class="sxs-lookup"><span data-stu-id="e894c-127">Interpolation Modifier</span></span> | <span data-ttu-id="e894c-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e894c-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e894c-129">**Lineare**</span><span class="sxs-lookup"><span data-stu-id="e894c-129">**linear**</span></span>             | <span data-ttu-id="e894c-130">Eseguire l'interpolazione tra gli input dello shader; **linear** è il valore predefinito se non viene specificato alcun modificatore di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="e894c-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e894c-131">**Baricentro**</span><span class="sxs-lookup"><span data-stu-id="e894c-131">**centroid**</span></span>           | <span data-ttu-id="e894c-132">Interpolazione tra campioni che si trova in un punto qualsiasi all'interno dell'area coperta del pixel (potrebbe essere necessario estrapolare i punti finali da un centro pixel).</span><span class="sxs-lookup"><span data-stu-id="e894c-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="e894c-133">Il campionamento centroide può migliorare l'antialiasing se un pixel è parzialmente coperto (anche se il centro pixel non è coperto).</span><span class="sxs-lookup"><span data-stu-id="e894c-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="e894c-134">Il **modificatore centroid** deve essere combinato con il **modificatore lineare** **o noperspective.**</span><span class="sxs-lookup"><span data-stu-id="e894c-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e894c-135">**nointerpolazione**</span><span class="sxs-lookup"><span data-stu-id="e894c-135">**nointerpolation**</span></span>    | <span data-ttu-id="e894c-136">Non eseguire l'interpolazione di .</span><span class="sxs-lookup"><span data-stu-id="e894c-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e894c-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="e894c-137">**noperspective**</span></span>      | <span data-ttu-id="e894c-138">Non eseguire la correzione della prospettiva durante l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="e894c-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="e894c-139">Il **modificatore noperspective** può essere combinato con il **modificatore centroid.**</span><span class="sxs-lookup"><span data-stu-id="e894c-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e894c-140">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e894c-140">**sample**</span></span>             | <span data-ttu-id="e894c-141">**Disponibile nel modello shader 4.1 e versioni successive** Interpolare in corrispondenza della posizione del campione anziché al centro dei pixel.</span><span class="sxs-lookup"><span data-stu-id="e894c-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="e894c-142">In questo modo il pixel shader viene eseguito per campione anziché per pixel.</span><span class="sxs-lookup"><span data-stu-id="e894c-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="e894c-143">Un altro modo per causare l'esecuzione per campione è avere un input con [ \_ SV SampleIndex semantico,](dx-graphics-hlsl-semantics.md)che indica l'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="e894c-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="e894c-144">Solo gli input  con il campione specificato (o l'input di SV SampleIndex) differiscono tra le chiamate dello shader nel pixel, mentre altri input che non specificano modificatori (ad esempio, se si combinano modificatori in input diversi) continuano a interpolare al centro \_ pixel.</span><span class="sxs-lookup"><span data-stu-id="e894c-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="e894c-145">Sia pixel shader chiamate che test di profondità/stencil vengono eseguiti per ogni campione coperto nel pixel.</span><span class="sxs-lookup"><span data-stu-id="e894c-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="e894c-146">Questa operazione è talvolta nota come *supersampling*.</span><span class="sxs-lookup"><span data-stu-id="e894c-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="e894c-147">Al contrario, in assenza di una chiamata di frequenza di campionamento, nota come multicampionamento, il pixel shader viene richiamato una volta per pixel indipendentemente dal numero di campioni coperti, mentre i test di profondità/stencil si verificano alla *frequenza* del campione.</span><span class="sxs-lookup"><span data-stu-id="e894c-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="e894c-148">Entrambe le modalità forniscono un antialiasing perimetrale equivalente.</span><span class="sxs-lookup"><span data-stu-id="e894c-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="e894c-149">Tuttavia, il supercampionamento offre una migliore qualità di ombreggiatura richiamando l'pixel shader più frequentemente.</span><span class="sxs-lookup"><span data-stu-id="e894c-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="e894c-150">1. Quando si usa un tipo int/uint, l'unica opzione valida è **nointerpolation**.</span><span class="sxs-lookup"><span data-stu-id="e894c-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="e894c-151">I modificatori di interpolazione possono essere applicati ai membri della struttura o agli [argomenti di funzione](dx-graphics-hlsl-function-parameters.md)o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="e894c-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="e894c-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="e894c-152">Examples</span></span>

<span data-ttu-id="e894c-153">Di seguito sono riportati alcuni esempi di dichiarazioni di struttura.</span><span class="sxs-lookup"><span data-stu-id="e894c-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="e894c-154">Questa dichiarazione include una matrice.</span><span class="sxs-lookup"><span data-stu-id="e894c-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="e894c-155">Questa dichiarazione include un modificatore di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="e894c-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="e894c-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e894c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e894c-157">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e894c-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





