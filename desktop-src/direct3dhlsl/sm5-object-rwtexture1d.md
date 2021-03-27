---
title: RWTexture1D
description: Una risorsa di lettura/scrittura. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- HLSL RWTexture1D
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981151"
---
# <a name="rwtexture1d"></a>RWTexture1D

Una risorsa di lettura/scrittura.



| Metodo                                                        | Descrizione                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1d-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture1d-load.md)                              | Legge i dati della trama.           |
| [**Operatore\[\]**](sm5-object-rwtexture1d-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile anteporre gli oggetti **RWTexture1D** alla classe di archiviazione **globallycoherent**. Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.

Un oggetto **RWTexture1D** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente è corretta:


```
RWTexture1D<float> tex;
```



Poiché un oggetto **RWTexture1D** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto tipo di visualizzazione risorse shader (SRV), ad esempio un oggetto [**Texture1D**](sm5-object-texture1d.md) . Ad esempio, è possibile leggere e scrivere in un oggetto **RWTexture1D** , ma è possibile leggere solo da un oggetto **Texture1D** .

Un oggetto **RWTexture1D** non può usare i metodi di un oggetto [**Texture1D**](sm5-object-texture1d.md) , ad esempio [Sample](dx-graphics-hlsl-to-sample.md). Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come una singola trama in più shader. Ad esempio, è possibile dichiarare e usare un oggetto **RWTexture1D** come *Tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture1D** come *Tex* in una pixel shader.

> [!Note]  
> Il Runtime impone determinati modelli di utilizzo quando si creano più tipi di visualizzazione nella stessa risorsa. Il runtime, ad esempio, non consente di avere un mapping UAV per una risorsa e un mapping SRV per la stessa risorsa attiva allo stesso tempo.

 

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

 

 




