---
title: Texture (oggetto)
description: In Direct3D 10 specificare i sampler e le trame in modo indipendente; il campionamento della trama viene implementato usando un oggetto con trama basata su modelli. Questo oggetto con trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL oggetto trama
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234915"
---
# <a name="texture-object"></a>Texture (oggetto)

In Direct3D 10 specificare i sampler e le trame in modo indipendente; il campionamento della trama viene implementato usando un oggetto con trama basata su modelli. Questo oggetto con trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D9 e Direct3D10: in Direct3D 9 i sampler sono associati a trame specifiche; in Direct3D 10, le trame e i sampler sono oggetti indipendenti. Ogni oggetto con trama basata su modelli implementa metodi di campionamento di trama che accettano sia la trama sia il campionatore come parametri di input.<br/> |



 

Di seguito è illustrata la sintassi per la creazione di tutti gli oggetti texture (eccetto gli oggetti multicampionati).



| \[ <  > \] *Nome* tipo Oggetto1; |
|------------------------------------|



 

Per gli oggetti multicampionati (Texture2DMS e Texture2DMSArray) è necessario che la dimensione della trama venga dichiarata in modo esplicito e espressa come numero di campioni.



| \[ < *Tipo oggetto2,* > \] *nome* degli esempi; |
|---------------------------------------------|



 

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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em><br/></td>
<td>Oggetto texture. Deve essere uno dei seguenti tipi. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo Oggetto1</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>trama 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Matrice di trame 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>trama 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Matrice di trame 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>trama 3D</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>Trama cubo</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Matrice di trame del cubo</td>
</tr>
<tr class="odd">
<td>Tipo oggetto2</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>trama multicampionata 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Matrice di trame multicampionate 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>Il tipo di buffer supporta la maggior parte dei metodi dell'oggetto texture ad eccezione di GetDimensions</li>
<li>TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</li>
<li>Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em></p></td>
<td><p>facoltativo. Qualsiasi tipo <a href="dx-graphics-hlsl-scalar.md">scalare HLSL</a> o <a href="dx-graphics-hlsl-vector.md"><strong>vettore HLSL</strong></a>, racchiuso tra parentesi angolari. Il tipo predefinito è <strong>float4</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nome</em></p></td>
<td><p>Stringa ASCII che specifica il nome dell'oggetto texture.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Campioni</em></p></td>
<td><p>Numero di campioni (compreso tra 1 e 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Esempio 1

Di seguito è riportato un esempio di dichiarazione di un oggetto texture.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Metodi dell'oggetto texture

Ogni oggetto texture implementa determinati metodi; Ecco la tabella in cui sono elencati tutti i metodi. Vedere la pagina di riferimento per ogni metodo per vedere quali oggetti possono usare il metodo.



| Texture (metodo)                                                                     | Descrizione                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calcolare il valore LOD, restituire un risultato bloccato.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcolare il valore LOD, restituire un risultato non bloccato.                                                                    |          |           |          | x         |          |           |
| [Raccogliere](dx-graphics-hlsl-to-gather.md)                                           | Ottiene i quattro campioni (solo per il componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Ottiene la dimensione di trama per un livello di mipmap specificato.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (multisample)](dx-graphics-hlsl-to-getdimensions.md)               | Ottiene la dimensione di trama per un livello di mipmap specificato.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Ottiene la posizione dell'esempio specificato.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Caricare i dati senza alcun filtro o campionamento.                                                                      | x        | x         | x        | x         | x        | x         |
| [Load (campionamento)](dx-graphics-hlsl-to-load.md)                                 | Caricare i dati senza alcun filtro o campionamento.                                                                      |          | x         | x        | x         |          | x         |
| [Esempio](dx-graphics-hlsl-to-sample.md)                                           | Campionare una trama.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Campionare una trama, usando un valore di confronto per rifiutare gli esempi.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Campionare una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Campionare una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Campiona una trama sul livello mipmap specificato.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Tipo restituito

Il tipo restituito di un metodo dell'oggetto texture è float4, a meno che non sia specificato diversamente, ad eccezione degli oggetti trama con anti-aliasing multicampionato che richiedono sempre il tipo e il numero di campione specificati. Il tipo restituito è uguale al tipo di risorsa trama ([**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). In altre parole, può essere uno qualsiasi dei seguenti tipi.



| Tipo                       | Descrizione                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | float a 32 bit (vedere [le regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float)                            |
| INT                        | Intero con segno a 32 bit                                                                                                                                                   |
| int senza segno               | Intero senza segno a 32 bit                                                                                                                                                 |
| russare                      | 32 bit float nell'intervallo compreso tra 1 e 1 (vedere [le regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float) |
| unorm                      | 32 bit float nell'intervallo compreso tra 0 e 1 (vedere [regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float)  |
| qualsiasi tipo di trama o struct | Il numero di componenti restituiti deve essere compreso tra 1 e 3.                                                                                                    |



 

Inoltre, il tipo restituito può essere qualsiasi tipo di trama, inclusa una struttura, ma deve essere inferiore a 4 componenti, ad esempio un tipo float1 che restituisce un componente.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valori predefiniti per i componenti mancanti in una trama

Il valore predefinito per i componenti mancanti in un tipo di risorsa trama è zero per qualsiasi componente eccetto il componente alfa (A); il valore predefinito per l'oggetto mancante è uno. Il modo in cui questo aspetto viene visualizzato nello shader dipende dal tipo di risorsa trama. Prende il formato del primo componente tipizzato che è effettivamente presente nel tipo di risorsa trama (a partire da sinistra nell'ordine RGBA). Se il formato è UNORM o FLOAT, il valore predefinito per l'oggetto mancante A è 1,0 f. Se il form è SINT o UINT, il valore predefinito per l'oggetto mancante A è 0x1.

Ad esempio, quando uno shader legge il [**formato DXGI \_ \_ R24 \_ UNORM \_ x8 \_ tipo**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) di risorsa trama, i valori predefiniti per G e B sono pari A zero e il valore predefinito per a è 1,0 f; quando uno shader legge il [**formato DXGI \_ \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) trama tipo di risorsa, il valore predefinito per B è zero e il valore predefinito per a è 0x00000001; quando uno shader legge il [**formato DXGI \_ \_ R16 \_ Sint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture tipo di risorsa, i valori predefiniti per G e B sono pari a zero e il valore predefinito per a è 0x00000001.

## <a name="example-2"></a>Esempio 2

Di seguito è riportato un esempio di campionamento di trama usando un metodo texture.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

