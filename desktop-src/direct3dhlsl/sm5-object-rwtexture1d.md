---
title: RWTexture1D
description: Risorsa di lettura/scrittura. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67fb82897e6b07dad486d134c7d36004ed5bfb1e050ed80446c50df5842eac32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671381"
---
# <a name="rwtexture1d"></a>RWTexture1D

Risorsa di lettura/scrittura.



| Metodo                                                        | Descrizione                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1d-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture1d-load.md)                              | Legge i dati delle trame.           |
| [**Operatore\[\]**](sm5-object-rwtexture1d-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile aggiungere come **prefisso gli oggetti RWTexture1D** alla classe di archiviazione **globalmentecoherent**. Questa classe di archiviazione fa sì che le barriere di memoria e le sincronizzazioni scaricano i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica un UAV solo all'interno del gruppo corrente.

Un **oggetto RWTexture1D** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente è corretta:


```
RWTexture1D<float> tex;
```



Poiché un **oggetto RWTexture1D** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto di tipo SRV (Shader Resource View), ad esempio un [**oggetto Texture1D.**](sm5-object-texture1d.md) Ad esempio, è possibile leggere e scrivere in un **oggetto RWTexture1D,** ma è possibile leggere solo da un **oggetto Texture1D.**

Un **oggetto RWTexture1D** non può usare metodi di un [**oggetto Texture1D,**](sm5-object-texture1d.md) ad esempio [Sample.](dx-graphics-hlsl-to-sample.md) Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come singola trama in più shader. Ad esempio, è possibile dichiarare e usare un **oggetto RWTexture1D** come *tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture1D** come *tex* in un pixel shader.

> [!Note]  
> Il runtime applica determinati modelli di utilizzo quando si creano più tipi di visualizzazione per la stessa risorsa. Ad esempio, il runtime non consente di avere contemporaneamente attivo sia un mapping UAV per una risorsa che un mapping SRV per la stessa risorsa.

 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




