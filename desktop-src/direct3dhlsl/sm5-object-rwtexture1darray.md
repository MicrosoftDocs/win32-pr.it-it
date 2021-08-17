---
title: RWTexture1DArray
description: Una risorsa di lettura/scrittura. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- RWTexture1DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c25bbc29e9835f79fa65510d97a3fd0241b06b5ad3415db1059c755a3ac5e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509273"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Una risorsa di lettura/scrittura.



| Metodo                                                             | Descrizione                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture1darray-load.md)                              | Legge i dati della trama.           |
| [**Operatore\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile aggiungere il **prefisso RWTexture1DArray** agli oggetti con la classe di archiviazione **globalmentecoherent.** Questa classe di archiviazione causa barriere di memoria e sincronizzazioni per scaricare i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica un UAV solo all'interno del gruppo corrente.

Un **oggetto RWTexture1DArray** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente è corretta:


```
RWTexture1DArray<float> tex;
```



Poiché un **oggetto RWTexture1DArray** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto di tipo SRV (Shader Resource View), ad esempio un oggetto [**Texture1DArray.**](sm5-object-texture1darray.md) Ad esempio, è possibile leggere e scrivere in un **oggetto RWTexture1DArray,** ma è possibile leggere solo da un **oggetto Texture1DArray.**

Un **oggetto RWTexture1DArray** non può usare i metodi di un [**oggetto Texture1DArray,**](sm5-object-texture1darray.md) ad esempio [Sample.](dx-graphics-hlsl-to-sample.md) Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come singola trama in più shader. Ad esempio, è possibile dichiarare e usare un oggetto **RWTexture1DArray** come *tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture1DArray** come *tex* in un pixel shader.

> [!Note]  
> Il runtime applica determinati modelli di utilizzo quando si creano più tipi di visualizzazione per la stessa risorsa. Ad esempio, il runtime non consente di avere contemporaneamente sia un mapping UAV per una risorsa che un mapping SRV per la stessa risorsa.

 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




