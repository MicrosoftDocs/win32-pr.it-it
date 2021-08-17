---
title: RWTexture2DArray
description: Risorsa di lettura/scrittura. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9ae4d4c7c47012b71a70916f5861975176b86e6612cb2a4fec3ea6c9c6e17cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095131"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Risorsa di lettura/scrittura.



| Metodo                                                             | Descrizione                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture2darray-load.md)                              | Legge i dati delle trame.           |
| [**Operatore\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile aggiungere come **prefisso gli oggetti RWTexture2DArray** alla classe di archiviazione **globalmentecoherent**. Questa classe di archiviazione fa sì che le barriere di memoria e le sincronizzazioni scaricano i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica un UAV solo all'interno del gruppo corrente.

Un **oggetto RWTexture2DArray** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente è corretta:


```
RWTexture2DArray<float> tex;
```



Poiché un **oggetto RWTexture2DArray** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto di tipo SRV (Shader Resource View), ad esempio un oggetto [**Texture2DArray.**](sm5-object-texture2darray.md) Ad esempio, è possibile leggere e scrivere in un **oggetto RWTexture2DArray,** ma è possibile leggere solo da un **oggetto Texture2DArray.**

Un **oggetto RWTexture2DArray** non può usare metodi di un [**oggetto Texture2DArray,**](sm5-object-texture2darray.md) ad esempio [Sample.](dx-graphics-hlsl-to-sample.md) Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come singola trama in più shader. Ad esempio, è possibile dichiarare e usare un **oggetto RWTexture2DArray** come *tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture2DArray** come *tex* in un pixel shader.

> [!Note]  
> Il runtime applica determinati modelli di utilizzo quando si creano più tipi di visualizzazione per la stessa risorsa. Ad esempio, il runtime non consente di avere contemporaneamente attivo sia un mapping UAV per una risorsa che un mapping SRV per la stessa risorsa.

 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 




