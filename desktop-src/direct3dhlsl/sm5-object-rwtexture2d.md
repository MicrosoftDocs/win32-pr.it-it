---
title: RWTexture2D
description: Risorsa di lettura/scrittura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c015aaa8606f5d04386b7839584203c5672e4ac1bf031b89eb4c41ca69f7dd14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985931"
---
# <a name="rwtexture2d"></a>RWTexture2D

Risorsa di lettura/scrittura.



| Metodo                                                        | Descrizione                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture2d-load.md)                              | Legge i dati delle trame.           |
| [**Operatore\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile aggiungere come prefisso gli oggetti RWTexture2D alla classe di archiviazione **globalmentecoherent**. Questa classe di archiviazione fa sì che le barriere di memoria e le sincronizzazioni scaricano i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica solo una visualizzazione di accesso non ordinata (UAV) all'interno del gruppo corrente.

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



Poiché un oggetto RWTexture2D è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto di tipo SRV (Shader Resource View), ad esempio un [oggetto Texture2D.](sm5-object-texture2d.md) Ad esempio, è possibile leggere e scrivere in un oggetto RWTexture2D, ma è possibile leggere solo da un oggetto Texture2D.

Un oggetto RWTexture2D non può usare metodi di un [oggetto Texture2D,](sm5-object-texture2d.md) ad esempio [Sample.](dx-graphics-hlsl-to-sample.md) Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come singola trama in più shader. Ad esempio, i frammenti di codice seguenti illustrano come dichiarare e usare un oggetto RWTexture2D come *tex* in un compute shader e quindi dichiarare e usare un oggetto Texture2D come *tex* in un pixel shader.

> [!Note]  
> Il runtime applica determinati modelli di utilizzo quando si creano più tipi di visualizzazione per la stessa risorsa. Ad esempio, il runtime non consente di avere contemporaneamente attivo sia un mapping UAV per una risorsa che un mapping SRV per la stessa risorsa.

 

Il codice seguente è per lo shader di calcolo:


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



Il codice seguente è per l'pixel shader:


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



## <a name="minimum-shader-model"></a>Modello shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




