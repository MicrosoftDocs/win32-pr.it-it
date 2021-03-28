---
title: RWBuffer
description: Un buffer di lettura/scrittura.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL RWBuffer
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334039"
---
# <a name="rwbuffer"></a>RWBuffer

Un buffer di lettura/scrittura.



| Metodo                                                     | Descrizione                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.          |
| [**Caricamento**](rwbuffer-load.md)                              | Ottiene un valore in un buffer di lettura/scrittura. |
| [**Operatore\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Restituisce una variabile di risorsa.           |



 

Una variabile di risorsa può essere passata anche in qualsiasi operazione non ordinata o Interlocked.

Gli oggetti **RWBuffer** possono essere preceduti dalla classe di archiviazione **globallycoherent**. Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.

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

 

 




