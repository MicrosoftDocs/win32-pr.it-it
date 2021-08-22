---
title: Stream-Output fase
description: Lo scopo della fase di output del flusso è l'output continuo (o flusso) dei dati dei vertici dalla fase geometry shader (o dalla fase vertex shader se la fase geometry shader è inattiva) a uno o più buffer in memoria (vedere Attività iniziali con la fase Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- Fase di output del flusso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f630208b60b107b211f8bb6f6ee0f1efac3ed736c96756dbe1e95e24032b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538575"
---
# <a name="stream-output-stage"></a>Stream-Output fase

Lo scopo della fase di output del flusso è l'output continuo (o flusso) dei dati dei vertici dalla fase geometry shader (o dalla fase vertex shader se la fase geometry shader è inattiva) a uno o più buffer in memoria (vedere Attività iniziali con la fase [Stream-Output).](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)

La fase stream-output (SO) si trova nella pipeline subito dopo la fase geometry shader e subito prima della fase di rasterizzazione, come illustrato nel diagramma seguente.

![diagramma della posizione della fase stream-output nella pipeline](images/d3d10-pipeline-stages-so.png)

I dati trasmessi in memoria possono essere letti di nuovo nella pipeline in un passaggio di rendering successivo o copiati in una risorsa di staging (in modo che possano essere letti dalla CPU). La quantità di dati trasmessi può variare. [**L'API ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) è progettata per gestire i dati senza la necessità di eseguire query (GPU) sulla quantità di dati scritti.

Quando un triangolo o una striscia di linee è associata alla fase dell'assembler di input, ogni striscia viene convertita in un elenco prima di essere trasmessa in streaming. I vertici vengono sempre scritti come primitive complete (ad esempio, 3 vertici alla volta per i triangoli); Le primitive incomplete non vengono mai trasmesse. I tipi primitivi con adicenza eliminano i dati di adizia prima di trasmettere i dati.

Esistono due modi per eseguire il feed dei dati di output di flusso nella pipeline:

-   I dati di output di flusso possono essere nuovamente immessi nella fase input-assembler.
-   I dati di output del flusso possono essere letti dagli shader programmabili usando funzioni di caricamento , ad esempio [Load.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)

Per usare un buffer come risorsa di output del flusso, creare il buffer con il flag [**D3D11 \_ BIND \_ STREAM \_ OUTPUT.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) La fase stream-output supporta fino a 4 buffer contemporaneamente.

-   Se si esegua lo streaming dei dati in più buffer, ogni buffer può acquisire solo un singolo elemento (fino a 4 componenti) di dati per vertice, con uno stride dati implicito uguale alla larghezza dell'elemento in ogni buffer (compatibile con il modo in cui i buffer dei singoli elementi possono essere associati per l'input nelle fasi dello shader). Inoltre, se i buffer hanno dimensioni diverse, la scrittura si interrompe non appena uno dei buffer è pieno.
-   Se si tras streaming dei dati in un singolo buffer, il buffer può acquisire fino a 64 componenti scalari di dati per vertice (al massimo 256 byte) oppure lo stride del vertice può essere fino a 2048 byte.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                               | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Attività iniziali con la fase Stream-Output lavoro](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | Questa sezione descrive come usare uno shader geometry con la fase di output del flusso.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

