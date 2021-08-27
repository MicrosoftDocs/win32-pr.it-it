---
description: La pipeline programmabile Direct3D 10 è progettata per la generazione di grafica per applicazioni di gioco in tempo reale. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ognuna delle fasi programmabili.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Fasi della pipeline (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942e2594f1f2eeb83f92b3ee517804a68b6074d85bf5c9205828a08e024112df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119977"
---
# <a name="pipeline-stages-direct3d-10"></a>Fasi della pipeline (Direct3D 10)

La pipeline programmabile Direct3D 10 è progettata per la generazione di grafica per applicazioni di gioco in tempo reale. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ognuna delle fasi programmabili.

![diagramma del flusso di dati nella pipeline programmabile direct3d 10](images/d3d10-pipeline-stages.png)

Tutte le fasi possono essere configurate usando l'API . Le fasi con core di shader comuni (blocchi rettangolari arrotondati) sono programmabili usando il linguaggio di programmazione HLSL. Come si può vedere, in questo modo la pipeline è estremamente flessibile e adattabile. Lo scopo di ognuna delle fasi è elencato di seguito.

-   [Fase dell'assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) di input: la fase input-assembler è responsabile dell'immissione di dati (triangoli, linee e punti) alla pipeline.
-   [Fase vertex-shader](https://www.bing.com/search?q=Vertex-Shader+Stage). La fase vertex-shader elabora i vertici, eseguendo generalmente operazioni come trasformazioni, applicazione di interfacce e illuminazione. Un vertex shader accetta sempre un singolo vertice di input e produce un singolo vertice di output.
-   [Fase geometry-shader:](https://www.bing.com/search?q=Geometry-Shader+Stage) la fase geometry shader elabora intere primitive. L'input è una primitiva completa (ovvero tre vertici per un triangolo, due vertici per una linea o un singolo vertice per un punto). Inoltre, ogni primitiva può includere anche i dati dei vertici per qualsiasi primitiva adiacente al bordo. Può includere al massimo tre vertici aggiuntivi per un triangolo o altri due vertici per una linea. Geometry Shader supporta anche l'amplificazione e la de-amplificazione della geometria limitate. Data una primitiva di input, Geometry Shader può eliminare la primitiva o generare una o più nuove primitive.
-   [Fase stream-output:](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) la fase stream-output è progettata per trasmettere i dati primitivi dalla pipeline alla memoria verso il rasterizzatore. I dati possono essere inviati come flusso di output e/o passati all'unità di rasterizzazione. I dati trasmessi in streaming alla memoria possono essere rimessi in circolazione nella pipeline come dati di input oppure letti di nuovo dalla CPU.
-   [Fase di rasterizzazione:](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) il rasterizzatore è responsabile del ritaglio delle primitive, della preparazione delle primitive per il pixel shader e della determinazione di come richiamare i pixel shader.
-   [Fase pixel-shader](https://www.bing.com/search?q=Pixel-Shader+Stage). La fase pixel-shader riceve i dati interpolati per una primitiva e genera dati per pixel, come il colore.
-   [Fase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) di unione dell'output: la fase di unione dell'output è responsabile della combinazione di vari tipi di dati di output (valori pixel shader, informazioni di profondità e stencil) con il contenuto della destinazione di rendering e dei buffer di profondità/stencil per generare il risultato finale della pipeline.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
