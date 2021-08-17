---
title: RWTexture3D
description: Risorsa di lettura/scrittura. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bc2630d339bfb465b570ba62b346cd931301425f4feeb4367407ffd52336e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789864"
---
# <a name="rwtexture3d"></a>RWTexture3D

Risorsa di lettura/scrittura.



| Metodo                                                        | Descrizione                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](rwtexture3d-load.md)                              | Legge i dati delle trame.           |
| [**Operatore\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Ottiene una variabile di risorsa.     |



 

È possibile aggiungere come **prefisso gli oggetti RWTexture3D** alla classe di archiviazione **globalmentecoherent**. Questa classe di archiviazione fa sì che le barriere di memoria e le sincronizzazioni scaricano i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica un UAV solo all'interno del gruppo corrente.

Un **oggetto RWTexture3D** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto. Ad esempio, la dichiarazione seguente è corretta:


```
RWTexture3D<float> tex;
```



Poiché un **oggetto RWTexture3D** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto di tipo SRV (Shader Resource View), ad esempio un [**oggetto Texture3D.**](sm5-object-texture3d.md) Ad esempio, è possibile leggere e scrivere in un **oggetto RWTexture3D,** ma è possibile leggere solo da un **oggetto Texture3D.**

Un **oggetto RWTexture3D** non può usare metodi di un [**oggetto Texture3D,**](sm5-object-texture3d.md) ad esempio [Sample.](dx-graphics-hlsl-to-sample.md) Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come singola trama in più shader. Ad esempio, è possibile dichiarare e usare un **oggetto RWTexture3D** come *tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture3D** come *tex* in un pixel shader.

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

 

 




