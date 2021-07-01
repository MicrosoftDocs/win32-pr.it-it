---
title: Tipo di campionatore
description: Usare la sintassi seguente per dichiarare lo stato del campionatore e lo stato di confronto del campionatore.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo di campionatore HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0206f7030d3b3a05570e74273d9510bb9c2592c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119576"
---
# <a name="sampler-type"></a><span data-ttu-id="d6e87-104">Tipo di campionatore</span><span class="sxs-lookup"><span data-stu-id="d6e87-104">Sampler Type</span></span>

<span data-ttu-id="d6e87-105">Usare la sintassi seguente per dichiarare lo stato del campionatore e lo stato di confronto del campionatore.</span><span class="sxs-lookup"><span data-stu-id="d6e87-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e87-106">Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="d6e87-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="d6e87-107">Ecco la sintassi per un campionatore in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d6e87-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e87-108">sampler <em>Name</em>  =  <em>SamplerType</em>{ Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="d6e87-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="d6e87-109">La sintassi per un campionatore in Direct3D 10 e versioni successive è stata leggermente modificata per supportare oggetti trama e matrici di campionatori.</span><span class="sxs-lookup"><span data-stu-id="d6e87-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e87-110"><em>SamplerType Name[Index]</em>{ [<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="d6e87-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="d6e87-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6e87-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e87-112"><span id="sampler"></span><span id="SAMPLER"></span>Campionatore</span><span class="sxs-lookup"><span data-stu-id="d6e87-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-113">Solo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d6e87-113">Direct3D 9 only.</span></span> <span data-ttu-id="d6e87-114">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="d6e87-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="d6e87-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="d6e87-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-116">Stringa ASCII che identifica in modo univoco il nome della variabile del campionatore.</span><span class="sxs-lookup"><span data-stu-id="d6e87-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="d6e87-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Indice\]*</span><span class="sxs-lookup"><span data-stu-id="d6e87-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-118">Solo Direct3D 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d6e87-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="d6e87-119">Dimensioni della matrice facoltative. Un numero intero positivo maggiore o uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="d6e87-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d6e87-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span><span class="sxs-lookup"><span data-stu-id="d6e87-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-121">\[in Tipo di campionatore, che è uno dei \] seguenti: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler \_ state*, *SamplerState*.</span><span class="sxs-lookup"><span data-stu-id="d6e87-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>

<span data-ttu-id="d6e87-122">Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="d6e87-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span>

- <span data-ttu-id="d6e87-123">Direct3D 10 e versioni successive supporta un tipo di campionatore aggiuntivo: *SamplerComparisonState.*</span><span class="sxs-lookup"><span data-stu-id="d6e87-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span>



 

</dd> <dt>

<span data-ttu-id="d6e87-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Trama* = <*\_ variabile di* trama>;</span><span class="sxs-lookup"><span data-stu-id="d6e87-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-125">Solo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d6e87-125">Direct3D 9 only.</span></span> <span data-ttu-id="d6e87-126">Variabile di trama.</span><span class="sxs-lookup"><span data-stu-id="d6e87-126">A texture variable.</span></span> <span data-ttu-id="d6e87-127">La parola chiave *Texture* è obbligatoria sul lato sinistro. Il nome della variabile appartiene al lato destro dell'espressione all'interno delle parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="d6e87-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="d6e87-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state \_ name = state \_ value*</span><span class="sxs-lookup"><span data-stu-id="d6e87-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="d6e87-129">\[in \] Assegnazioni di stato facoltative.</span><span class="sxs-lookup"><span data-stu-id="d6e87-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="d6e87-130">Il lato sinistro di un'assegnazione è un nome di stato, il lato destro è il valore dello stato.</span><span class="sxs-lookup"><span data-stu-id="d6e87-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="d6e87-131">Tutte le assegnazioni di stato devono essere presenti all'interno di un blocco di istruzioni (tra parentesi graffe).</span><span class="sxs-lookup"><span data-stu-id="d6e87-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="d6e87-132">Ogni istruzione è separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="d6e87-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="d6e87-133">Nella tabella seguente sono elencati i nomi di stato possibili.</span><span class="sxs-lookup"><span data-stu-id="d6e87-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="d6e87-134">Il lato destro di ogni espressione è il valore assegnato a ogni stato.</span><span class="sxs-lookup"><span data-stu-id="d6e87-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="d6e87-135">Vedere la [**struttura \_ \_ DESC D3D11 SAMPLER**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) per i valori di stato possibili per Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d6e87-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="d6e87-136">Esiste una relazione da 1 a 1 tra i nomi di stato e i membri della struttura .</span><span class="sxs-lookup"><span data-stu-id="d6e87-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="d6e87-137">Vedere l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d6e87-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6e87-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6e87-138">Remarks</span></span>

<span data-ttu-id="d6e87-139">Quando si implementa un effetto, lo stato del campionatore è uno dei diversi tipi di stato che potrebbe essere necessario configurare nella pipeline per il rendering.</span><span class="sxs-lookup"><span data-stu-id="d6e87-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="d6e87-140">Per un elenco di tutti i possibili stati che è possibile impostare in un effetto, vedere:</span><span class="sxs-lookup"><span data-stu-id="d6e87-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="d6e87-141">Direct3D 10 usa i [gruppi di stati](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="d6e87-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="d6e87-142">Direct3D 9 usa singoli [stati](/windows/desktop/direct3d9/effect-states).</span><span class="sxs-lookup"><span data-stu-id="d6e87-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="d6e87-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6e87-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e87-144">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="d6e87-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="d6e87-145">Di seguito è riportato un esempio parziale di un campionatore Direct3D 9 <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">dell'esempio BasicHLSL.</a></span><span class="sxs-lookup"><span data-stu-id="d6e87-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="d6e87-146">Di seguito è riportato un esempio parziale di un campionatore Direct3D 10 di <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample.</a></span><span class="sxs-lookup"><span data-stu-id="d6e87-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d6e87-147">Di seguito è riportato un esempio parziale di dichiarazione dello stato di confronto del campionatore e della chiamata di un campionatore di confronto in Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="d6e87-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="d6e87-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d6e87-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e87-149">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6e87-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

