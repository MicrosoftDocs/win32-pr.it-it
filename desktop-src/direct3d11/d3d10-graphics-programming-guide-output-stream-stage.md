---
title: Fase Stream-Output
description: Lo scopo della fase di output del flusso è quello di restituire o trasmettere continuamente i dati dei vertici dalla fase geometry-shader (o dalla fase vertex shader se la fase geometry-shader è inattiva) a uno o più buffer in memoria (vedere Introduzione con la fase di Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- fase output flusso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474684"
---
# <a name="stream-output-stage"></a>Fase Stream-Output

Lo scopo della fase di output del flusso è quello di restituire o trasmettere continuamente i dati dei vertici dalla fase geometry-shader (o dalla fase vertex shader se la fase geometry-shader è inattiva) a uno o più buffer in memoria (vedere [Introduzione con la fase di Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).

La fase di output del flusso (quindi) si trova nella pipeline immediatamente dopo la fase geometry-shader e immediatamente prima della fase di rasterizzazione, come illustrato nella figura seguente.

![diagramma della posizione della fase di output del flusso nella pipeline](images/d3d10-pipeline-stages-so.png)

I dati trasmessi alla memoria possono essere letti nuovamente nella pipeline in un passaggio di rendering successivo oppure possono essere copiati in una risorsa di staging, in modo che possano essere letti dalla CPU. La quantità di dati trasmessi può variare. l'API [**sul ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) è progettata per gestire i dati senza la necessità di eseguire query (GPU) sulla quantità di dati scritti.

Quando una striscia o un triangolo è associato alla fase input-assembler, ogni striscia viene convertita in un elenco prima che vengano trasmessi. I vertici vengono sempre scritti come primitive complete (ad esempio, 3 vertici alla volta per i triangoli); le primitive incomplete non vengono mai trasmesse. I tipi primitivi con adiacenza scartano i dati adiacenza prima di trasmettere i dati in uscita.

Esistono due modi per inserire i dati di output del flusso nella pipeline:

-   Stream: i dati di output possono essere inseriti nella fase input-assembler.
-   I dati di output di flusso possono essere letti da shader programmabili usando funzioni di caricamento (ad esempio, [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).

Per usare un buffer come risorsa di output del flusso, creare il buffer con il flag di [**\_ output del \_ flusso \_ di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) . La fase Stream-output supporta fino a 4 buffer contemporaneamente.

-   Se si esegue il flusso di dati in più buffer, ogni buffer può acquisire solo un singolo elemento (fino a 4 componenti) di dati per vertice, con uno stride di dati implicito uguale alla larghezza dell'elemento in ogni buffer (compatibile con la modalità di associazione dei buffer a singolo elemento per l'input nelle fasi dello shader). Inoltre, se i buffer hanno dimensioni diverse, la scrittura viene arrestata non appena uno dei buffer è pieno.
-   Se si esegue il flusso di dati in un singolo buffer, il buffer può acquisire fino a 64 componenti scalari di dati per vertice (256 byte o meno) o lo stride del vertice può essere fino a 2048 byte.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                               | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Introduzione con la fase di Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | Questa sezione descrive come usare un geometry shader con la fase di output del flusso.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

