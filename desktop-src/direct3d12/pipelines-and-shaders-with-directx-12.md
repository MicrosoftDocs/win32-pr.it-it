---
title: Pipelines e shader con Direct3D 12
description: La pipeline programmabile Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd4ab60573fca9b9dce6759b5f87969199f83aed08aaa44a01f1501c402080e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952932"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipelines e shader con Direct3D 12

La pipeline programmabile Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.

-   [Pipeline grafica Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Oggetti di stato della pipeline](#pipeline-state-objects)
-   [Pipeline di calcolo Direct3D 12](#direct3d-12-compute-pipeline)
-   [Argomenti correlati](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Pipeline grafica Direct3D 12

Il diagramma seguente illustra la pipeline grafica Direct3D 12 e lo stato.

![Diagramma che illustra la pipeline e lo stato direct3d 12](images/pipeline.png)

Una pipeline grafica è il flusso sequenziale di input e output di dati durante il rendering dei fotogrammi da parte della GPU. Dato lo stato e gli input della pipeline, la GPU esegue una serie di operazioni per creare le immagini risultanti. Una pipeline grafica contiene shader, che eseguono calcoli e effetti di rendering programmabili, e operazioni di funzione fissa.

Quando si fa riferimento al diagramma di stato della pipeline, tenere presente quanto segue:

-   Le tabelle e gli heap dei descrittori possono essere disposti in modo arbitrario: è possibile fare riferimento a SRV, CBV e UAV e allocare in qualsiasi ordine.
-   Alcune operazioni della pipeline sono configurabili. Ad esempio, l'unione dell'output viene in genere opera in lettura/modifica/scrittura con la destinazione di rendering e le depth stencil di output. È tuttavia possibile configurare la pipeline in modo che una di queste viste sia di sola lettura o di sola scrittura.
-   I campionatori statici non fanno parte degli argomenti radice perché sono statici.

## <a name="pipeline-state-objects"></a>Oggetti di stato della pipeline

Direct3D 12 introduce l'oggetto stato della pipeline (PSO). Anziché archiviare e rappresentare lo stato della pipeline in un numero elevato di oggetti di alto livello, gli stati dei componenti della pipeline come assembler di input, rasterizzazione, pixel shader e unione di output vengono archiviati in un pso. Un oggetto pso è un oggetto stato della pipeline unificato che non è modificabile dopo la creazione. Il PSO attualmente selezionato può essere modificato rapidamente e dinamicamente e l'hardware e i driver possono convertire direttamente un PSO in istruzioni e stato hardware nativi, preparando la GPU per l'elaborazione grafica. Per applicare un pso, l'hardware copia una quantità minima di stato pre-calcolato direttamente nei registri hardware. In questo modo viene rimosso il sovraccarico causato dal driver di grafica che ricalcola continuamente lo stato hardware in base a tutte le impostazioni di rendering e pipeline attualmente applicabili. Il risultato è una riduzione significativa dell'overhead delle chiamate di disegno, un aumento delle prestazioni e un numero maggiore di chiamate di disegno per frame.

L'oggetto PSO attualmente applicato definisce e connette tutti gli shader usati nella pipeline di rendering. [Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) è precompilato in oggetti shader, che vengono quindi usati in fase di esecuzione come input per gli oggetti di stato della pipeline. Per altre informazioni sul funzionamento di PSO all'interno della pipeline grafica, vedere [Managing graphics pipeline state in Direct3D 12 (Gestione dello stato della pipeline grafica in Direct3D 12).](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="direct3d-12-compute-pipeline"></a>Pipeline di calcolo Direct3D 12

Il diagramma seguente illustra lo stato e la pipeline di calcolo Direct3D 12.

![Diagramma che mostra la pipeline di calcolo Direct3D 12.](images/compute-pipeline.png)

In questa pipeline non sono presenti unità di funzione fisse, tuttavia gli heap dei descrittori, gli heap dei campionatori e i campionatori statici sono ancora disponibili nelle risorse di calcolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 