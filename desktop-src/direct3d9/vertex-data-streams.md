---
description: Le interfacce di rendering per Direct3D sono costituite da metodi che eseguono il rendering delle primitive dai dati dei vertici archiviati in uno o più buffer di dati.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Vertex Data Flussi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f154621da4ba03f78beee87767130e37da9e9ab9ba899af737b968fb20f0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290386"
---
# <a name="vertex-data-streams-direct3d-9"></a>Vertex Data Flussi (Direct3D 9)

Le interfacce di rendering per Direct3D sono costituite da metodi che eseguono il rendering delle primitive dai dati dei vertici archiviati in uno o più buffer di dati. I dati dei vertici sono costituiti da elementi vertice combinati per formare componenti dei vertici. Gli elementi vertice, l'unità più piccola di un vertice, rappresentano entità come posizione, normale o colore.

I componenti vertice sono uno o più elementi vertice archiviati in modo contiguo (interleaved per vertice) in un singolo buffer di memoria. Un vertice completo è costituito da uno o più componenti, in cui ogni componente si trova in un buffer di memoria separato. Per eseguire il rendering di una primitiva, vengono letti e assemblati più componenti vertice in modo che siano disponibili vertici completi per l'elaborazione dei vertici. Il diagramma seguente illustra il processo di rendering delle primitive usando i componenti dei vertici.

![diagramma del processo di rendering delle primitive usando i componenti dei vertici](images/vertexdata.png)

Le primitive di rendering sono costituite da due passaggi. Configurare prima di tutto uno o più flussi dei componenti vertice. richiamare quindi un [**metodo IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per eseguire il rendering da tali flussi. L'identificazione degli elementi vertice all'interno di questi flussi di componenti viene specificata dal vertex shader.

I metodi [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) specificano un offset nei flussi di dati dei vertici in modo che sia possibile eseguire il rendering di un subset contiguo arbitrario delle primitive all'interno di un set di dati vertice con ogni chiamata di disegno. In questo modo è possibile modificare lo stato di rendering del dispositivo tra gruppi di primitive di cui viene eseguito il rendering dagli stessi buffer dei vertici.

Sono supportati sia i metodi di disegno indicizzati che non indicizzati. Per altre informazioni, vedere [Rendering da vertex buffer e index buffer (Direct3D 9).](rendering-from-vertex-and-index-buffers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di rendering](rendering-primitives.md)
</dt> </dl>

 

 
