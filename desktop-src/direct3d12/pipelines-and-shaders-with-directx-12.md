---
title: Pipeline e shader con Direct3D 12
description: La pipeline programmabile di Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548815"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipeline e shader con Direct3D 12

La pipeline programmabile di Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.

-   [Pipeline grafica Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Oggetti stato della pipeline](#pipeline-state-objects)
-   [Pipeline di calcolo Direct3D 12](#direct3d-12-compute-pipeline)
-   [Argomenti correlati](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Pipeline grafica Direct3D 12

Il diagramma seguente illustra la pipeline grafica e lo stato di Direct3D 12.

![diagramma che illustra la pipeline e lo stato di Direct3D 12](images/pipeline.png)

Una pipeline grafica è il flusso sequenziale di input e output di dati quando la GPU esegue il rendering dei frame. Dato lo stato e gli input della pipeline, la GPU esegue una serie di operazioni per creare le immagini risultanti. Una pipeline grafica contiene shader, che eseguono effetti e calcoli di rendering programmabili e operazioni di funzione fisse.

Quando si fa riferimento al diagramma di stato della pipeline, tenere presente quanto segue:

-   Le tabelle e gli heap del descrittore possono essere disposti arbitrariamente: è possibile fare riferimento a SRVs, CBVs e UAV e allocarli in qualsiasi ordine.
-   Alcune operazioni della pipeline sono configurabili. La fusione di output, ad esempio, agisce in genere su una base di lettura e modifica con la destinazione di rendering e le visualizzazioni depth stencil. Tuttavia, la pipeline può essere configurata in modo che una di queste viste sia di sola lettura o di sola scrittura.
-   I sampler statici non fanno parte degli argomenti radice perché sono statici.

## <a name="pipeline-state-objects"></a>Oggetti stato della pipeline

Direct3D 12 introduce l'oggetto di stato della pipeline (PSO). Anziché archiviare e rappresentare lo stato della pipeline in un numero elevato di oggetti di alto livello, gli Stati dei componenti della pipeline come Assembler di input, rasterizzatore, pixel shader e Unione di output vengono archiviati in un oggetto PSO. Un oggetto PSO è un oggetto di stato della pipeline unificato che non è modificabile dopo la creazione. Il PSO attualmente selezionato può essere modificato in modo rapido e dinamico e l'hardware e i driver possono convertire direttamente un oggetto PSO in istruzioni e stato hardware nativi, preparando la GPU per l'elaborazione grafica. Per applicare un oggetto PSO, l'hardware copia una quantità minima di stato pre-calcolato direttamente nei registri hardware. In questo modo viene rimosso il sovraccarico causato dal driver grafico che esegue continuamente il ricalcolo dello stato dell'hardware in base a tutte le impostazioni di rendering e pipeline attualmente applicabili. Il risultato è una riduzione significativa del sovraccarico delle chiamate di progetto, delle prestazioni migliorate e di altre chiamate per frame.

Il PSO attualmente applicato definisce e connette tutti gli shader usati nella pipeline di rendering. [Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) è precompilato in oggetti shader, che vengono quindi usati in fase di esecuzione come input per gli oggetti di stato della pipeline. Per ulteriori informazioni sul modo in cui le funzioni PSO all'interno della pipeline grafica, vedere [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="direct3d-12-compute-pipeline"></a>Pipeline di calcolo Direct3D 12

Il diagramma seguente illustra la pipeline di calcolo e lo stato di Direct3D 12.

![Diagramma che mostra la pipeline di calcolo Direct3D 12.](images/compute-pipeline.png)

In questa pipeline non sono presenti unità di funzione fisse, tuttavia gli heap del descrittore, gli heap del campionatore e i sampler statici sono ancora disponibili in calcolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 