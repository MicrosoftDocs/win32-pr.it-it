---
title: Fase geometry shader
description: La fase geometry shader (GS) esegue il codice dello shader specificato dall'applicazione con vertici come input e la possibilità di generare vertici nell'output.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d568b9eb62b2545721acebfda865f7f2553597fb999a3a647164106c836369
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952911"
---
# <a name="geometry-shader-stage"></a>Fase geometry shader

La fase geometry shader (GS) esegue il codice dello shader specificato dall'applicazione con vertici come input e la possibilità di generare vertici nell'output.

## <a name="the-geometry-shader"></a>Shader geometrico

A differenza dei vertex shader, che operano su un singolo vertice, gli input del geometry shader sono i vertici per una primitiva completa (due vertici per le linee, tre vertici per i triangoli o un singolo vertice per il punto). I geometry shader possono anche inserire i dati dei vertici per le primitive adiacenti ai bordi come input (altri due vertici per una linea, altri tre per un triangolo). La figura seguente mostra un triangolo e una linea con vertici adiacenti.

![illustrazione di un triangolo e di una linea con vertici adiacenti](images/d3d10-gs.png)

|     | Tipo                |
|-----|-----------------|
| **TV**  | Vertice triangolare |
| **Av**  | Vertice adiacente |
| **Lv**  | Vertice linea     |



 

La fase geometry shader può utilizzare il valore SV PrimitiveID generato dal sistema generato automaticamente \_ dall'IA. [](d3d10-graphics-programming-guide-input-assembler-stage-using.md) In questo modo i dati per primitivi possono essere recuperati o calcolati, se necessario.

La fase geometry shader è in grado di eseguire l'output di più vertici che formano una singola topologia selezionata(le topologie di output della fase GS disponibili sono: tristrip, linestrip e pointlist). Il numero di primitive emesse può variare liberamente all'interno di qualsiasi chiamata dello shader geometry, anche se il numero massimo di vertici che possono essere generati deve essere dichiarato in modo statico. Le lunghezze di strip emesse da una chiamata geometry shader possono essere arbitrarie ed è possibile creare nuove strisce tramite la funzione [HLSL RestartStrip.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip)

L'output dello shader geometrico può essere trasmesso alla fase di rasterizzazione e/o a un buffer dei vertici in memoria tramite la fase di output del flusso. L'output immesso in memoria viene espanso in singoli elenchi di punti/linee/triangoli (esattamente come verrebbero passati al rasterizzatore).

Quando uno shader geometry è attivo, viene richiamato una volta per ogni primitiva passata o generata in precedenza nella pipeline. Ogni chiamata dello shader geometry vede come input i dati per la primitiva di richiamo, sia che si tratta di un singolo punto, di una singola riga o di un singolo triangolo. Una striscia di triangoli precedente nella pipeline comporta una chiamata dello shader geometrico per ogni singolo triangolo nella striscia (come se la striscia fosse espansa in un elenco di triangoli). Sono disponibili tutti i dati di input per ogni vertice nella singola primitiva (ad esempio 3 vertici per il triangolo), più i dati dei vertici adiacenti, se applicabile/disponibili.

Un geometry shader restituisce i dati un vertice alla volta aggiungendo i vertici a un oggetto flusso di output. La topologia dei flussi è determinata da una dichiarazione fissa, scegliendo una delle seguenti: PointStream, LineStream o TriangleStream come output per la fase GS. Sono disponibili tre tipi di oggetti flusso, PointStream, LineStream e TriangleStream, che sono tutti oggetti modello. La topologia dell'output è determinata dal rispettivo tipo di oggetto, mentre il formato dei vertici aggiunti al flusso è determinato dal tipo di modello. L'esecuzione di un'istanza geometry shader è atomica da altre chiamate, ad eccezione del fatto che i dati aggiunti ai flussi sono seriali. Gli output di una determinata chiamata di un geometry shader sono indipendenti dalle altre chiamate (anche se l'ordinamento viene rispettato). Un geometry shader che genera strisce di triangoli inizierà una nuova striscia a ogni chiamata.

Quando un output di geometry shader viene identificato come valore interpretato dal sistema (ad esempio, SV RenderTargetArrayIndex o SV Position), l'hardware esamina questi dati ed esegue un comportamento dipendente dal valore, oltre a poter passare i dati stessi alla fase successiva dello shader per \_ \_ l'input. Quando l'output di tali dati dallo shader geometry ha significato per l'hardware in base alla primitiva (ad esempio SV RenderTargetArrayIndex o SV ViewportArrayIndex), anziché per ogni vertice (ad esempio \_ \_ SV \_ ClipDistance n o SV Position), i dati per primitiva vengono prelevati dal vertice iniziale emesso per la \[ \] \_ primitiva.

Le primitive parzialmente completate potrebbero essere generate dallo shader geometry se il geometry shader termina e la primitiva è incompleta. Le primitive incomplete vengono automaticamente eliminate. Questo è simile al modo in cui L'IA considera le primitive parzialmente completate.

Lo shader geometry può eseguire operazioni di caricamento e campionamento trame in cui non sono necessari derivati dello spazio dello schermo (samplelevel, samplecmplevelzero, samplegrad).

Gli algoritmi che possono essere implementati nel geometry shader includono:

-   Espansione Sprite punto
-   Sistemi di particelle dinamiche
-   Generazione di fur/pin
-   Generazione di volumi shadow
-   Rendering a cubi a passaggio singolo
-   Per-Primitive scambio di materiali
-   Per-Primitive Material Setup : inclusa la generazione di coordinate barycentriche come dati primitivi, in modo che un pixel shader possa eseguire l'interpolazione di attributi personalizzati( per un esempio di interpolazione normale di ordine superiore, vedere [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 