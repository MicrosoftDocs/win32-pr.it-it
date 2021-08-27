---
title: Oggetto Texture
description: In Direct3D 10 si specificano i campionatori e le trame in modo indipendente. Il campionamento di trame viene implementato usando un oggetto texture basato su modelli. Questo oggetto trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL dell'oggetto Texture
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ac22ba8c9da7d69784d977e2b78b8f0b52a6a3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628117"
---
# <a name="texture-object"></a>Oggetto Texture

In Direct3D 10 si specificano i campionatori e le trame in modo indipendente. Il campionamento di trame viene implementato usando un oggetto texture basato su modelli. Questo oggetto trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.

Differenze tra Direct3D9 e Direct3D10:

- In Direct3D 9 i campionatori sono associati a trame specifiche.
- In Direct3D 10 le trame e i campionatori sono oggetti indipendenti. Ogni oggetto texture basato su modelli implementa metodi di campionamento delle trame che accettano sia la trama che il campionatore come parametri di input.



 

Ecco la sintassi per la creazione di tutti gli oggetti trama (ad eccezione degli oggetti multicampionati).



| Object1 \[ < *Type* > \] *Name*; |
|------------------------------------|



 

Gli oggetti multicampionato (Texture2DMS e Texture2DMSArray) richiedono che le dimensioni della trama siano dichiarate ed espresse in modo esplicito come numero di campioni.



| Object2 \[ < *Type, Samples* > \] *Name*; |
|---------------------------------------------|



 

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col  />
<col  />
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
<td>Oggetto trama. Deve essere uno dei tipi seguenti. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo Object1</th>
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
<td>Trama 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Matrice di trame 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>Trama 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Matrice di trame 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>Trama 3D</td>
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
<td>Tipo Object2</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>Trama multicampionata 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Matrice di trame multicampionamento 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>Il tipo Buffer supporta la maggior parte dei metodi dell'oggetto trama, ad eccezione di GetDimensions.</li>
<li>TextureCubeArray è disponibile nel modello di shader 4.1 o versione successiva.</li>
<li>Il modello di shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Digitare</em></p></td>
<td><p>facoltativo. Qualsiasi <a href="dx-graphics-hlsl-scalar.md">tipo HLSL scalare o</a> tipo <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vettore,</strong></a>racchiuso tra parentesi angolari. Il tipo predefinito è <strong>float4.</strong></p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nome</em></p></td>
<td><p>Stringa ASCII che specifica il nome dell'oggetto trama.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Campioni</em></p></td>
<td><p>Numero di campioni (compreso tra 1 e 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Esempio 1

Di seguito è riportato un esempio di dichiarazione di un oggetto trama.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Metodi dell'oggetto Texture

Ogni oggetto trama implementa determinati metodi. Ecco la tabella che elenca tutti i metodi. Vedere la pagina di riferimento per ogni metodo per vedere quali oggetti possono usare tale metodo.



| Metodo Texture                                                                     | Descrizione                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calcolare il LOD e restituire un risultato con chiusura.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcolare il loD e restituire un risultato senza punti esclamativi.                                                                    |          |           |          | x         |          |           |
| [Raccogliere](dx-graphics-hlsl-to-gather.md)                                           | Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Ottiene la dimensione della trama per un livello mipmap specificato.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (MultiSample)](dx-graphics-hlsl-to-getdimensions.md)               | Ottiene la dimensione della trama per un livello mipmap specificato.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Ottiene la posizione dell'esempio specificato.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Caricare i dati senza filtri o campionamenti.                                                                      | x        | x         | x        | x         | x        | x         |
| [Load (Multisample)](dx-graphics-hlsl-to-load.md)                                 | Caricare i dati senza filtri o campionamenti.                                                                      |          | x         | x        | x         |          | x         |
| [Esempio](dx-graphics-hlsl-to-sample.md)                                           | Campionare una trama.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Campionare una trama usando un valore di confronto per rifiutare i campioni.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Campionare una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Campionare una trama al livello mipmap specificato.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Tipo restituito

Il tipo restituito di un metodo dell'oggetto trama è float4 se non specificato diversamente, ad eccezione degli oggetti di trama con anti-aliasing multicampionato che necessitano sempre del tipo e del numero di campioni specificati. Il tipo restituito è uguale al tipo di risorsa trama ([**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). In altre parole, può essere uno dei tipi seguenti.



| Tipo                       | Descrizione                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | Float a 32 bit (vedere [Regole a virgola mobile](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) per le differenze rispetto a float IEEE)                            |
| int                        | Intero con segno a 32 bit                                                                                                                                                   |
| int senza segno               | Intero senza segno a 32 bit                                                                                                                                                 |
| snorm                      | Float a 32 bit nell'intervallo compreso tra -1 e 1 inclusi (vedere [Regole a virgola](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) mobile per le differenze rispetto a float IEEE) |
| unorm                      | Float a 32 bit nell'intervallo compreso tra 0 e 1 inclusi (vedere [Regole a virgola](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) mobile per le differenze rispetto a float IEEE)  |
| qualsiasi tipo o struct di trama | Il numero di componenti restituiti deve essere compreso tra 1 e 3 inclusi.                                                                                                    |



 

Inoltre, il tipo restituito può essere qualsiasi tipo di trama, inclusa una struttura , ma deve essere minore di 4 componenti, ad esempio un tipo float1 che restituisce un componente.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valori predefiniti per i componenti mancanti in una trama

Il valore predefinito per i componenti mancanti in un tipo di risorsa trama è zero per qualsiasi componente ad eccezione del componente alfa (A); il valore predefinito per la A mancante è uno. Il modo in cui questo elemento viene visualizzato allo shader dipende dal tipo di risorsa trama. Assume la forma del primo componente tipiato effettivamente presente nel tipo di risorsa trama (a partire da sinistra nell'ordine RGBA). Se il formato è UNORM o FLOAT, il valore predefinito per la A mancante è 1,0f. Se il modulo è SINT o UINT, il valore predefinito per la A mancante è 0x1.

Ad esempio, quando uno shader legge il tipo di risorsa trama [**DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) I valori predefiniti per G e B sono zero e il valore predefinito per A è 1,0f. Quando uno shader legge il tipo di risorsa trama [**UINT DXGI \_ FORMAT \_ R16G16, \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) il valore predefinito per B è zero e il valore predefinito per A è 0x00000001; quando uno shader legge il tipo di risorsa trama [**SINT DXGI FORMAT \_ \_ R16, \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) i valori predefiniti per G e B sono zero e il valore predefinito per A è 0x00000001.

## <a name="example-2"></a>Esempio 2

Di seguito è riportato un esempio di campionamento delle trame usando un metodo di trama.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

