---
title: Fase geometry shader
description: La fase geometry-shader (GS) esegue il codice shader specificato dall'applicazione con i vertici come input e la possibilità di generare vertici nell'output.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da66b1e3f9abf4e7db8010887f3e78676d02a874
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728386"
---
# <a name="geometry-shader-stage"></a>Fase geometry shader

La fase geometry-shader (GS) esegue il codice shader specificato dall'applicazione con i vertici come input e la possibilità di generare vertici nell'output.

## <a name="the-geometry-shader"></a>Geometry shader

Diversamente dai vertex shader, che operano su un singolo vertice, gli input di Geometry shader sono i vertici di una primitiva completa (due vertici per le linee, tre vertici per i triangoli o un vertice singolo per Point). I geometry shader possono anche inserire i dati dei vertici per le primitive adiacenti al bordo come input (altri due vertici per una linea, tre ulteriori per un triangolo). La figura seguente mostra un triangolo e una linea con vertici adiacenti.

![illustrazione di un triangolo e di una linea con vertici adiacenti](images/d3d10-gs.png)

|     |                 |
|-----|-----------------|
| TV  | Vertice triangolo |
| AV  | Vertice adiacente |
| LV  | Vertice linea     |



 

La fase geometry-shader può utilizzare il \_ [valore generato dal sistema](d3d10-graphics-programming-guide-input-assembler-stage-using.md) SV PrimitiveID generato automaticamente dall'IA. In questo modo è possibile recuperare o calcolare i dati per primitive, se lo si desidera.

La fase geometry-shader è in grado di restituire più vertici che formano una singola topologia selezionata (le topologie di output della fase GS disponibili sono: tristrip, LineStrip e elenco di puntatori). Il numero di primitive emesse può variare liberamente all'interno di qualsiasi chiamata del geometry shader, sebbene il numero massimo di vertici che è possibile emettere debba essere dichiarato in modo statico. Le lunghezze di striscia emesse da una chiamata di shader Geometry possono essere arbitrarie e le nuove strisce possono essere create tramite la funzione [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL.

L'output di Geometry shader può essere alimentato alla fase di rasterizzazione e/o a un buffer dei vertici in memoria tramite la fase di output del flusso. L'output alimentato alla memoria viene espanso nei singoli elenchi punto/linea/triangolo (esattamente come verrebbero passati al rasterizzatore).

Quando un geometry shader è attivo, viene richiamato una volta per ogni primitiva passata o generata in precedenza nella pipeline. Ogni chiamata di Geometry shader considera come input i dati per la primitiva chiamante, sia che si tratti di un singolo punto, di una singola riga o di un singolo triangolo. Una striscia di triangolo precedente nella pipeline comporterebbe una chiamata del geometry shader per ogni singolo triangolo nella striscia (come se la striscia venisse espansa in un elenco di triangolo). Sono disponibili tutti i dati di input per ogni vertice della primitiva, ovvero 3 vertici per il triangolo, oltre ai dati dei vertici adiacenti, se applicabili o disponibili.

Un geometry shader restituisce i dati un vertice alla volta aggiungendo i vertici a un oggetto del flusso di output. La topologia dei flussi è determinata da una dichiarazione fixed, scegliendo uno dei seguenti: PointStream, LineStream o TriangleStream come output per la fase GS. Sono disponibili tre tipi di oggetti flusso, PointStream, LineStream e TriangleStream, che sono tutti oggetti basati su modelli. La topologia dell'output è determinata dal rispettivo tipo di oggetto, mentre il formato dei vertici accodati al flusso è determinato dal tipo di modello. L'esecuzione di un'istanza geometry shader è atomica da altre chiamate, ad eccezione del fatto che i dati aggiunti ai flussi sono di tipo seriale. Gli output di una determinata chiamata di uno shader Geometry sono indipendenti dalle altre chiamate (anche se l'ordinamento è rispettato). Un geometry shader che genera strisce triangolari avvierà una nuova striscia a ogni chiamata.

Quando un output di Geometry shader viene identificato come valore interpretato dal sistema (ad esempio \_ , SV RenderTargetArrayIndex o SV \_ position), l'hardware esamina questi dati ed esegue un comportamento dipendente dal valore, oltre a essere in grado di passare i dati alla fase successiva dello shader per l'input. Quando l'output di questo tipo di dati di Geometry shader ha un significato per l'hardware in base ai primitivi (ad esempio, SV \_ RenderTargetArrayIndex o SV \_ ViewportArrayIndex), anziché in base al singolo vertice (ad esempio \_ , SV Clipdistance \[ n \] o SV \_ position), i dati per primitivi vengono presi dal vertice principale emesso per la primitiva.

Le primitive parzialmente completate potrebbero essere generate dalla geometria shader se il geometry shader termina e la primitiva è incompleta. Le primitive incomplete vengono scartate automaticamente. Questa operazione è simile al modo in cui l'IA tratta le primitive parzialmente completate.

Geometry shader può eseguire operazioni di campionamento del carico e della trama in cui i derivati dello spazio dello schermo non sono obbligatori (samplelevel, SampleCmpLevelZero, samplegrad).

Gli algoritmi che possono essere implementati in Geometry shader includono:

-   Espansione sprite punto
-   Sistemi particellari dinamici
-   Generazione di pellicce/pinna
-   Generazione del volume shadow
-   Rendering a passaggio singolo-a-mappa cubi
-   Scambio di materiali Per-Primitive
-   Per-Primitive la configurazione del materiale, inclusa la generazione di coordinate baricentrica come dati primitivi, in modo che un pixel shader possa eseguire l'interpolazione di attributi personalizzati (per un esempio di interpolazione normale di ordine superiore, vedere [esempio di CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 