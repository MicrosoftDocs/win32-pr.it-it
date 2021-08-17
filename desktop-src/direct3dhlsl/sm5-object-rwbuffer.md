---
title: RWBuffer
description: Buffer di lettura/scrittura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88992a60148b58e4a252770c2be65625130378d56837a8c8c93958b57a9a3980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725176"
---
# <a name="rwbuffer"></a>RWBuffer

Buffer di lettura/scrittura.



| Metodo                                                     | Descrizione                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.          |
| [**Caricamento**](rwbuffer-load.md)                              | Ottiene un valore in un buffer di lettura/scrittura. |
| [**Operatore\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Restituisce una variabile di risorsa.           |



 

Una variabile di risorsa può anche essere passata a qualsiasi operazione non ordinata o interlocked.

**Gli oggetti RWBuffer** possono essere preceduti dalla classe di archiviazione **globalmentecoherente**. Questa classe di archiviazione causa barriere di memoria e sincronizzazioni per scaricare i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica un UAV solo all'interno del gruppo corrente.

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

 

 




