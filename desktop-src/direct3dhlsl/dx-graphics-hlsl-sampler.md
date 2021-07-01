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
# <a name="sampler-type"></a>Tipo di campionatore

Usare la sintassi seguente per dichiarare lo stato del campionatore e lo stato di confronto del campionatore.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:<br/> Ecco la sintassi per un campionatore in Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td>sampler <em>Name</em>  =  <em>SamplerType</em>{ Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La sintassi per un campionatore in Direct3D 10 e versioni successive è stata leggermente modificata per supportare oggetti trama e matrici di campionatori.</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType Name[Index]</em>{ [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>Campionatore
</dt> <dd>

Solo Direct3D 9. Parola chiave obbligatoria.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della variabile del campionatore.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Indice\]*
</dt> <dd>

Solo Direct3D 10 e versioni successive. Dimensioni della matrice facoltative. Un numero intero positivo maggiore o uguale a 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[in Tipo di campionatore, che è uno dei \] seguenti: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler \_ state*, *SamplerState*.

Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:

- Direct3D 10 e versioni successive supporta un tipo di campionatore aggiuntivo: *SamplerComparisonState.*



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Trama* = <*\_ variabile di* trama>;
</dt> <dd>

Solo Direct3D 9. Variabile di trama. La parola chiave *Texture* è obbligatoria sul lato sinistro. Il nome della variabile appartiene al lato destro dell'espressione all'interno delle parentesi angolari.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state \_ name = state \_ value*
</dt> <dd>

\[in \] Assegnazioni di stato facoltative. Il lato sinistro di un'assegnazione è un nome di stato, il lato destro è il valore dello stato. Tutte le assegnazioni di stato devono essere presenti all'interno di un blocco di istruzioni (tra parentesi graffe). Ogni istruzione è separata da un punto e virgola. Nella tabella seguente sono elencati i nomi di stato possibili.


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



Il lato destro di ogni espressione è il valore assegnato a ogni stato. Vedere la [**struttura \_ \_ DESC D3D11 SAMPLER**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) per i valori di stato possibili per Direct3D 11. Esiste una relazione da 1 a 1 tra i nomi di stato e i membri della struttura . Vedere l'esempio seguente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si implementa un effetto, lo stato del campionatore è uno dei diversi tipi di stato che potrebbe essere necessario configurare nella pipeline per il rendering. Per un elenco di tutti i possibili stati che è possibile impostare in un effetto, vedere:

-   Direct3D 10 usa i [gruppi di stati](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 usa singoli [stati](/windows/desktop/direct3d9/effect-states).

## <a name="example"></a>Esempio



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Di seguito è riportato un esempio parziale di un campionatore Direct3D 9 <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">dell'esempio BasicHLSL.</a><br/> <span data-codelanguage=""></span>
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

<p>Di seguito è riportato un esempio parziale di un campionatore Direct3D 10 di <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample.</a></p>
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



 

Di seguito è riportato un esempio parziale di dichiarazione dello stato di confronto del campionatore e della chiamata di un campionatore di confronto in Direct3D 10.


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



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

