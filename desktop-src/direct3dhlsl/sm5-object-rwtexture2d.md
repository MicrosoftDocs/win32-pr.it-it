---
title: RWTexture2D
description: Una risorsa di lettura/scrittura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352971"
---
# <a name="rwtexture2d"></a>RWTexture2D

Una risorsa di lettura/scrittura.



| Metodo                                                        | Descrizione                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture2d-load.md)                              | Legge i dati della trama.           |
| [**Operatore\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile anteporre gli oggetti RWTexture2D alla classe di archiviazione **globallycoherent**. Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica solo una visualizzazione di accesso non ordinato (UAV) nel gruppo corrente.

Un oggetto RWTexture2D richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente non è corretta:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



La dichiarazione seguente è corretta:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Poiché un oggetto RWTexture2D è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto tipo di visualizzazione risorse shader (SRV), ad esempio un oggetto [Texture2D](sm5-object-texture2d.md) . Ad esempio, è possibile leggere e scrivere in un oggetto RWTexture2D, ma è possibile leggere solo da un oggetto Texture2D.

Un oggetto RWTexture2D non può usare i metodi di un oggetto [Texture2D](sm5-object-texture2d.md) , ad esempio [Sample](dx-graphics-hlsl-to-sample.md). Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come una singola trama in più shader. Ad esempio, i frammenti di codice seguenti illustrano come dichiarare e usare un oggetto RWTexture2D come *Tex* in un compute shader e quindi dichiarare e usare un oggetto Texture2D come *tex* in una pixel shader.

> [!Note]  
> Il Runtime impone determinati modelli di utilizzo quando si creano più tipi di visualizzazione nella stessa risorsa. Il runtime, ad esempio, non consente di avere un mapping UAV per una risorsa e un mapping SRV per la stessa risorsa attiva allo stesso tempo.

 

Il codice seguente è per compute shader:


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



Il codice seguente è per il pixel shader:


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




