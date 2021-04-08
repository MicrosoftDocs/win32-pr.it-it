---
description: Le interfacce di rendering per Direct3D sono costituite da metodi che consentono di eseguire il rendering di primitive dai dati dei vertici archiviati in uno o più buffer di dati.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flussi di dati dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746103"
---
# <a name="vertex-data-streams-direct3d-9"></a>Flussi di dati dei vertici (Direct3D 9)

Le interfacce di rendering per Direct3D sono costituite da metodi che consentono di eseguire il rendering di primitive dai dati dei vertici archiviati in uno o più buffer di dati. I dati dei vertici sono costituiti da elementi Vertex combinati per formare componenti del vertice. Gli elementi vertice, ovvero l'unità più piccola di un vertice, rappresentano entità quali la posizione, il normale o il colore.

I componenti Vertex sono uno o più elementi Vertex archiviati in modo contiguo (interfoliazione per vertice) in un singolo buffer di memoria. Un vertice completo è costituito da uno o più componenti, in cui ogni componente si trova in un buffer di memoria separato. Per eseguire il rendering di una primitiva, vengono letti e assemblati più componenti del vertice in modo che i vertici completi siano disponibili per l'elaborazione del vertice. Il diagramma seguente illustra il processo di rendering delle primitive usando i componenti dei vertici.

![diagramma del processo per il rendering delle primitive usando i componenti dei vertici](images/vertexdata.png)

Il rendering delle primitive è costituito da due passaggi. Per prima cosa, configurare uno o più flussi del componente vertex; in secondo luogo, richiamare un metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per eseguire il rendering da tali flussi. L'identificazione di elementi Vertex all'interno di questi flussi di componenti è specificata dal vertex shader.

I metodi [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) specificano un offset nei flussi di dati dei vertici, in modo che sia possibile eseguire il rendering di un subset arbitrario contiguo delle primitive all'interno di un set di dati dei vertici a ogni chiamata di disegna. In questo modo è possibile modificare lo stato di rendering del dispositivo tra gruppi di primitivi di cui viene eseguito il rendering dagli stessi buffer dei vertici.

Sono supportati sia i metodi di disegno indicizzati che quelli non indicizzati. Per altre informazioni, vedere [rendering da vertex buffer e index buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di rendering](rendering-primitives.md)
</dt> </dl>

 

 
