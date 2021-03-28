---
title: Pipeline grafica
description: Questa sezione descrive la pipeline programmabile Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8e6b0b4d249c46dafe960f4f25a9a7598d6e2c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399944"
---
# <a name="graphics-pipeline"></a>Pipeline grafica

La pipeline programmabile Direct3D 11 è progettata per la generazione di elementi grafici per applicazioni di gioco in tempo reale. Questa sezione descrive la pipeline programmabile Direct3D 11. Il diagramma seguente illustra il flusso di dati dall'input all'output attraverso ogni fase programmabile.

![diagramma del flusso di dati nella pipeline programmabile Direct3D 11](images/d3d11-pipeline-stages.jpg)

La pipeline grafica per Microsoft Direct3D 11 supporta le stesse fasi della [pipeline grafica Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), con fasi aggiuntive per il supporto delle funzionalità avanzate.

È possibile usare Direct3D 11API per configurare tutte le fasi. Le fasi che dispongono di core shader comuni (blocchi rettangolari arrotondati) sono programmabili usando il linguaggio di programmazione [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) . Come si vedrà, la pipeline diventa estremamente flessibile e adattabile.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fase input-assembler](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | L'API Direct3D 10 e versioni successive separa le aree funzionali della pipeline in fasi. la prima fase della pipeline è la fase di input-assembler (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Fase vertex shader](vertex-shader-stage.md)<br/>                                      | La fase vertex-shader (VS) elabora i vertici dall'assembler di input, eseguendo operazioni per vertice, ad esempio le trasformazioni, il skinning, il morphing e l'illuminazione per vertice. I vertex shader operano sempre su un singolo vertice di input e producono un singolo vertice di output. Per eseguire la pipeline è necessario che la fase vertex shader sia sempre attiva. Se non è richiesta alcuna modifica o trasformazione del vertice, è necessario creare un vertex shader pass-through e impostarlo sulla pipeline.<br/> |
| [Fasi a mosaico](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Il runtime di Direct3D 11 supporta tre nuove fasi che implementano lo schema a mosaico, che converte le aree di sottodivisione con dettagli più bassi in primitive di dettaglio nella GPU. Tessere a mosaico (o suddividere) superfici di ordine superiore in strutture appropriate per il rendering.<br/>                                                                                                                                                                                                                 |
| [Fase geometry shader](geometry-shader-stage.md)<br/>                                  | La fase geometry-shader (GS) esegue il codice shader specificato dall'applicazione con i vertici come input e la possibilità di generare vertici nell'output.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Fase flusso-output](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | Lo scopo della fase di output del flusso è quello di restituire o trasmettere continuamente i dati dei vertici dalla fase geometry-shader (o dalla fase vertex shader se la fase geometry-shader è inattiva) a uno o più buffer in memoria (vedere [Introduzione con la fase di Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)). <br/>                                                                                                                       |
| [Fase Rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | La fase di rasterizzazione converte le informazioni vettoriali (costituite da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale. <br/>                                                                                                                                                                                                                                                                                                 |
| [Fase pixel shader](pixel-shader-stage.md)<br/>                                        | La fase pixel shader (PS) consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione. Un pixel shader è un programma che combina variabili costanti, dati di trama, valori interpolati per vertice e altri dati per produrre output per pixel. La fase di rasterizzazione richiama una pixel shader una volta per ogni pixel coperto da una primitiva, ma è possibile specificare uno shader **null** per evitare l'esecuzione di uno shader.<br/>                                          |
| [Output-fase di Unione](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | La fase di Unione degli output genera il colore del pixel finale sottoposto a rendering utilizzando una combinazione di stato della pipeline, i dati dei pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil. La fase OM è il passaggio finale per determinare quali pixel sono visibili (con test di stencil Depth) e fondere i colori finali dei pixel.<br/>                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compute Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

