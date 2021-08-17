---
title: Argomenti della funzione
description: Una funzione accetta uno o più argomenti di input. Usare la sintassi seguente per dichiarare ogni argomento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a2f2fdb656917ccf9dc57f06713fe01d77398d35776ac0c479b7d088281bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514764"
---
# <a name="function-arguments"></a>Argomenti della funzione

Una funzione accetta uno o più argomenti di input. Usare la sintassi seguente per dichiarare ogni argomento.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[InputModifier \] Type Name \[ : Semantic \] \[ InterpolationModifier \] \[ = Initializers\]** |



 

\[Nome \] del tipo di \[ modificatore : Semantic : \] \[ Modificatore di interpolazione = \] \[ Inizializzatori\]

Se sono presenti più argomenti di funzione, sono separati da virgole.

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>Termine facoltativo che identifica un argomento come input, output o entrambi.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>Solo input</td>
</tr>
<tr class="odd">
<td><strong>Inout</strong></td>
<td>Input e output</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Solo output</td>
</tr>
<tr class="odd">
<td><strong>uniform</strong></td>
<td>Immettere solo dati costanti</td>
</tr>
</tbody>
</table>

<p> </p>
<p>I parametri vengono sempre passati per valore. in indica che il valore del parametro deve essere copiato dall'applicazione chiamante prima dell'inizio della funzione. out indica che l'ultimo valore del parametro deve essere copiato e restituito all'applicazione chiamante quando la funzione restituisce . inout è una abbreviazione per specificare entrambi.</p>
<p>Un valore uniforme proviene da un registro costante. Ogni vertex shader o pixel shader chiamata visualizza lo stesso valore iniziale per una variabile uniforme. Le variabili globali vengono considerate come se fossero dichiarate uniformi. Per le funzioni non di primo livello, uniform è sinonimo di <strong>in</strong>. Se non viene specificato alcun utilizzo dei parametri, si presuppone che l'utilizzo del parametro sia <strong>in</strong>.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>digitare</strong></p></td>
<td><p>Tipo di argomento. può essere qualsiasi tipo HLSL <a href="dx-graphics-hlsl-data-types.md">valido.</a></p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nome</strong></p></td>
<td><p>Stringa ASCII che identifica in modo univoco il nome della funzione shader.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantica</strong></p></td>
<td><p>Stringa facoltativa che identifica l'utilizzo previsto dei dati (vedere <a href="dx-graphics-hlsl-semantics.md">Semantica (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolazioneModifier</strong></p></td>
<td><p>Modificatore <a href="dx-graphics-hlsl-struct.md">di interpolazione facoltativo</a> che consente a uno shader di determinare il metodo di interpolazione. Un modificatore di interpolazione su un argomento di funzione si applica solo a un argomento usato come input per una pixel shader funzione.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inizializzatori</strong></p></td>
<td><p>Valori facoltativi per l'inizializzazione; Per inizializzare i tipi di dati multi-componente sono necessari più valori.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Gli argomenti della funzione sono elencati in un elenco di argomenti delimitati da virgole in una dichiarazione di funzione. Come nelle funzioni C, ogni argomento deve avere un nome di parametro e un tipo dichiarati; Facoltativamente, un argomento per una funzione HLSL può includere una semantica, un valore iniziale e un input pixel shader può includere un tipo di interpolazione.

Il *tipo di* un argomento di funzione può essere una struttura che può includere un modificatore di interpolazione per membro. Se l'argomento della funzione ha anche un modificatore di interpolazione, il modificatore di argomento della funzione esegue l'override dei modificatori di interpolazione dichiarati all'interno di Type.

## <a name="examples"></a>Esempio

Questo esempio [(dall'esempio BasicHLSL10)](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)illustra input uniformi e non uniformi per una funzione vertex shader.


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



Questo esempio (dall'esempio [ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) usa una struttura di input per passare argomenti a una pixel shader funzione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





