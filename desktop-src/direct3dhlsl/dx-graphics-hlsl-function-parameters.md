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
# <a name="function-arguments"></a>Argomenti della funzione

Una funzione accetta uno o più argomenti di input. utilizzare la sintassi seguente per dichiarare ogni argomento.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[Nome del tipo di InputModifier \] \[ : Semantic \] \[ InterpolationModifier \] \[ = initializers\]** |



 

\[\]Nome tipo modificatore \[ : Semantic \] \[ : modificatore interpolazione \] \[ = inizializzatore/i\]

Se sono presenti più argomenti della funzione, sono separati da virgole.

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
<td><strong>Uniform</strong></td>
<td>Input solo di dati costanti</td>
</tr>
</tbody>
</table>

<p> </p>
<p>I parametri vengono sempre passati per valore. in indica che il valore del parametro deve essere copiato dall'applicazione chiamante prima che venga avviata la funzione. out indica che l'ultimo valore del parametro deve essere copiato e restituito all'applicazione chiamante quando la funzione restituisce. Inout è una sintassi abbreviata per specificare entrambi.</p>
<p>Un valore uniforme deriva da un registro costante. ogni vertex shader o pixel shader chiamata Visualizza lo stesso valore iniziale per una variabile uniforme. Le variabili globali vengono considerate come se fossero dichiarate uniformi. Per le funzioni non di primo livello, Uniform è sinonimo di <strong>in</strong>. Se non viene specificato alcun utilizzo del parametro, si presuppone che l'utilizzo del parametro sia <strong>in</strong>.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Tipo</strong></p></td>
<td><p>Tipo di argomento; può essere qualsiasi <a href="dx-graphics-hlsl-data-types.md">tipo</a>HLSL valido.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nome</strong></p></td>
<td><p>Stringa ASCII che identifica in modo univoco il nome della funzione shader.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantica</strong></p></td>
<td><p>Stringa facoltativa che identifica l'utilizzo previsto dei dati (vedere <a href="dx-graphics-hlsl-semantics.md">semantica (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p><a href="dx-graphics-hlsl-struct.md">Modificatore di interpolazione</a> facoltativo che consente a uno shader di determinare il metodo di interpolazione. Un modificatore di interpolazione su un argomento della funzione si applica solo a un argomento usato come input per una funzione pixel shader.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inizializzatori</strong></p></td>
<td><p>Valori facoltativi per l'inizializzazione. per inizializzare i tipi di dati multicomponente sono necessari più valori.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Gli argomenti della funzione sono elencati in un elenco di argomenti delimitati da virgole in una dichiarazione di funzione. Come nelle funzioni C, ogni argomento deve avere un nome di parametro e un tipo dichiarato; un argomento di una funzione HLSL può includere facoltativamente una semantica, un valore iniziale e un input pixel shader può includere un tipo di interpolazione.

Il *tipo* di un argomento della funzione può essere una struttura, che può includere un modificatore di interpolazione per singolo membro. Se l'argomento della funzione dispone anche di un modificatore di interpolazione, il modificatore di argomenti della funzione sostituisce i modificatori di interpolazione dichiarati nel tipo

## <a name="examples"></a>Esempio

Questo esempio (dall' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustra gli input uniformi e non uniformi a una funzione vertex shader.


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



Questo esempio (dall' [esempio ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) usa una struttura di input per passare argomenti a una funzione pixel shader.


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

 

 





