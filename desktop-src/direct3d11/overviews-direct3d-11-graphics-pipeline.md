---
title: Pipeline grafica
description: Questa sezione descrive la pipeline programmabile Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3872fbfaf63a53a07c8c06246088a5eec1791f98be867adbe56ae1d9c7724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565571"
---
# <a name="graphics-pipeline"></a>Pipeline grafica

La pipeline programmabile Direct3D 11 è progettata per la generazione di grafica per applicazioni di gioco in tempo reale. Questa sezione descrive la pipeline programmabile Direct3D 11. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ognuna delle fasi programmabili.

![diagramma del flusso di dati nella pipeline programmabile direct3d 11](images/d3d11-pipeline-stages.jpg)

La pipeline grafica per Microsoft Direct3D 11 supporta le stesse fasi della pipeline grafica [Direct3D 10,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)con fasi aggiuntive per supportare le funzionalità avanzate.

È possibile usare Direct3D 11API per configurare tutte le fasi. Le fasi che presentano core shader comuni (blocchi rettangolari arrotondati) sono programmabili tramite il [linguaggio di programmazione HLSL.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) Come si può vedere, in questo modo la pipeline è estremamente flessibile e adattabile.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fase dell'assembler di input](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | L'API Direct3D 10 e versioni successive separa le aree funzionali della pipeline in fasi; La prima fase della pipeline è la fase input-assembler (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Fase vertex shader](vertex-shader-stage.md)<br/>                                      | La fase vertex shader (VS) elabora i vertici dell'assembler di input, eseguendo operazioni per vertice, ad esempio trasformazioni, interfacciatura, morphing e illuminazione per vertice. I vertex shader operano sempre su un singolo vertice di input e producono un singolo vertice di output. La fase vertex shader deve essere sempre attiva per l'esecuzione della pipeline. Se non è necessaria alcuna modifica o trasformazione del vertice, è necessario creare e impostare un vertex shader pass-through sulla pipeline.<br/> |
| [Fasi a tessellazione](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Il runtime Direct3D 11 supporta tre nuove fasi che implementano la suddivisione a fasi, che converte le superfici di suddivisione con dettagli bassi in primitive più dettagliate nella GPU. Tessere a tessere a tessere (o scomposizioni) superfici di ordine elevato in strutture adatte per il rendering.<br/>                                                                                                                                                                                                                 |
| [Fase geometry shader](geometry-shader-stage.md)<br/>                                  | La fase geometry shader (GS) esegue il codice dello shader specificato dall'applicazione con vertici come input e la possibilità di generare vertici nell'output.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Fase di output del flusso](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | Lo scopo della fase di output del flusso è l'output continuo (o flusso) dei dati dei vertici dalla fase geometry shader (o dalla fase vertex shader se la fase geometry shader è inattiva) a uno o più buffer in memoria (vedere Attività iniziali con la fase [Stream-Output).](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md) <br/>                                                                                                                       |
| [Fase Rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | La fase di rasterizzazione converte le informazioni vettoriali (composte da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale. <br/>                                                                                                                                                                                                                                                                                                 |
| [Fase pixel shader](pixel-shader-stage.md)<br/>                                        | La fase pixel shader consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione. Un pixel shader è un programma che combina variabili costanti, dati di trama, valori interpolati per vertice e altri dati per produrre output per pixel. La fase di rasterizzazione richiama un pixel shader una volta per ogni pixel coperto da una primitiva, tuttavia è possibile specificare uno shader **NULL** per evitare l'esecuzione di uno shader.<br/>                                          |
| [Fase di unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | La fase di unione dell'output genera il colore finale del pixel sottoposto a rendering usando una combinazione di stato della pipeline, i dati pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil. La fase OM è il passaggio finale per determinare quali pixel sono visibili (con test di stencil di profondità) e per unire i colori in pixel finali.<br/>                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compute Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

