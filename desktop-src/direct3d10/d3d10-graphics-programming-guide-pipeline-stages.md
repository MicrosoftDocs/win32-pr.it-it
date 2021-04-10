---
description: La pipeline programmabile Direct3D 10 è progettata per la generazione di elementi grafici per applicazioni di gioco in tempo reale. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ogni fase programmabile.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Fasi della pipeline (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bf6e904051fcac255a5bf1b99ca0f7d43ca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126558"
---
# <a name="pipeline-stages-direct3d-10"></a>Fasi della pipeline (Direct3D 10)

La pipeline programmabile Direct3D 10 è progettata per la generazione di elementi grafici per applicazioni di gioco in tempo reale. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ogni fase programmabile.

![diagramma del flusso di dati nella pipeline programmabile Direct3D 10](images/d3d10-pipeline-stages.png)

Tutte le fasi possono essere configurate tramite l'API. Le fasi con i core shader comuni (blocchi rettangolari arrotondati) sono programmabili usando il linguaggio di programmazione HLSL. Come si vedrà, la pipeline diventa estremamente flessibile e adattabile. Lo scopo di ogni fase è riportato di seguito.

-   [Fase input-assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) : la fase input-assembler è responsabile della distribuzione dei dati (triangoli, linee e punti) alla pipeline.
-   [Fase vertex-shader](https://www.bing.com/search?q=Vertex-Shader+Stage). La fase vertex-shader elabora i vertici, eseguendo generalmente operazioni come trasformazioni, applicazione di interfacce e illuminazione. Un vertex shader accetta sempre un singolo vertice di input e produce un singolo vertice di output.
-   [Fase geometry-shader](https://www.bing.com/search?q=Geometry-Shader+Stage) : la fase geometry-shader elabora intere primitive. L'input è una primitiva completa (tre vertici per un triangolo, due vertici per una linea o un singolo vertice per un punto). Inoltre, ogni primitiva può includere anche i dati dei vertici per tutte le primitive adiacenti Edge. Questo può includere al massimo tre vertici aggiuntivi per un triangolo o due vertici aggiuntivi per una riga. Geometry shader supporta anche l'amplificazione e la deamplificazione di geometria limitate. Data una primitiva di input, geometry shader può rimuovere la primitiva oppure creare una o più nuove primitive.
-   [Fase Stream-output](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) : la fase Stream-output è progettata per lo streaming di dati primitivi dalla pipeline alla memoria nel modo in cui si trova nel rasterizzatore. I dati possono essere inviati come flusso di output e/o passati all'unità di rasterizzazione. I dati trasmessi in streaming alla memoria possono essere rimessi in circolazione nella pipeline come dati di input oppure letti di nuovo dalla CPU.
-   [Fase di rasterizzazione](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) : il rasterizzatore è responsabile per le primitive di ritaglio, per preparare le primitive per l'pixel shader e per determinare come richiamare i pixel shader.
-   [Fase pixel-shader](https://www.bing.com/search?q=Pixel-Shader+Stage). La fase pixel-shader riceve i dati interpolati per una primitiva e genera dati per pixel, come il colore.
-   [Fase di Unione dell'output](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) : la fase di Unione dell'output è responsabile della combinazione di diversi tipi di dati di output (pixel shader valori, informazioni di profondità e stencil) con il contenuto della destinazione di rendering e i buffer di profondità/stencil per generare il risultato finale della pipeline.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
