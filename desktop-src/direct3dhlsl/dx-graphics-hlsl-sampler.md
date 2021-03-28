---
title: Tipo campionatore
description: Utilizzare la sintassi seguente per dichiarare lo stato del campionatore, nonché lo stato di confronto del campionatore.
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
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046770"
---
# <a name="sampler-type"></a>Tipo campionatore

Utilizzare la sintassi seguente per dichiarare lo stato del campionatore, nonché lo stato di confronto del campionatore.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:<br/> Di seguito è illustrata la sintassi per un campionatore in Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em>nome</em>campionatore  =  <em>SamplerType</em>{texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La sintassi per un campionatore in Direct3D 10 e versioni successive è stata modificata leggermente per supportare gli oggetti trama e le matrici del campionatore.</p>

<table>
<tbody>
<tr class="odd">
<td><em>Nome SamplerType [index]</em>{[<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>campionatore
</dt> <dd>

Solo Direct3D 9. Parola chiave required.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della variabile del campionatore.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Indice\]*
</dt> <dd>

Solo Direct3D 10 e versioni successive. Dimensioni della matrice facoltative; numero intero positivo maggiore o uguale a 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[nel \] tipo di campionatore, che è uno dei seguenti: *Sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *Sampler \_ state*, *SamplerState*.



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10 e versioni successive:<br/> Direct3D 10 e versioni successive supporta un altro tipo di campionatore: *SamplerComparisonState*.<br/> |



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Trama* = <*\_ variabile di trama*>;
</dt> <dd>

Solo Direct3D 9. Variabile di trama. La parola chiave *texture* è obbligatoria sul lato sinistro; il nome della variabile appartiene sul lato destro dell'espressione all'interno delle parentesi angolari.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*\_nome stato = \_ valore stato*
</dt> <dd>

\[nelle \] assegnazioni di stato facoltative. Il lato sinistro di un'assegnazione è un nome di stato, il lato destro è il valore dello stato. Tutte le assegnazioni di stato devono essere visualizzate all'interno di un blocco di istruzioni (tra parentesi graffe). Ogni istruzione è separata da un punto e virgola. Nella tabella seguente sono elencati i nomi di stato possibili.


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



Il lato destro di ogni espressione è il valore assegnato a ogni stato. Vedere la struttura [**d3d11 \_ Sampler \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) per i valori di stato possibili per Direct3D 11. Esiste una relazione da 1 a 1 tra i nomi di stato e i membri della struttura. Vedere l'esempio seguente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si implementa un effetto, lo stato del campionatore è uno dei diversi tipi di stato che potrebbe essere necessario configurare nella pipeline per il rendering. Per un elenco di tutti gli stati possibili che è possibile impostare in un effetto, vedere:

-   Direct3D 10 USA i [gruppi di stati](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 utilizza singoli [Stati](/windows/desktop/direct3d9/effect-states).

## <a name="example"></a>Esempio



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Di seguito è riportato un esempio parziale di un campionatore Direct3D 9 di <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">esempio BasicHLSL</a>.<br/> <span data-codelanguage=""></span>
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

<p>Di seguito è riportato un esempio parziale di un campionatore Direct3D 10 dall' <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">esempio BasicHLSL10</a>.</p>
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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

