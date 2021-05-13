---
title: Coordinate di trama generate automaticamente (Direct3D 9)
description: Il sistema può usare la posizione trasformata dello spazio della fotocamera o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elemento usati per affrontare una mappa cubica dell'ambiente.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843292"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Coordinate di trama generate automaticamente (Direct3D 9)

Il sistema può usare la posizione trasformata dello spazio della fotocamera o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per affrontare una mappa cubica dell'ambiente. Analogamente alle coordinate di trama specificate in modo esplicito in un vertice, è possibile usare le coordinate di trama generate automaticamente come input per le trasformazioni delle coordinate di trama.

Le coordinate di trama generate automaticamente possono ridurre significativamente la larghezza di banda necessaria per i dati geometrici eliminando la necessità di coordinate di trama esplicite nel formato vertice. In molti casi, le coordinate di trama generate dal sistema possono essere usate con trasformazioni per produrre effetti speciali. Naturalmente, si tratta di una funzionalità speciale e si useranno coordinate di trama esplicite per molte occasioni.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Configurazione delle coordinate di trama generate automaticamente

In C++ lo stato della trama D3DTSS \_ TEXCOORDINDEX (dal tipo enumerato [**D3DTEXTURESTAGESTATETYPE)**](./d3dtexturestagestatetype.md) controlla il modo in cui il sistema genera le coordinate di trama.

In genere, questo stato indica al sistema di usare un particolare set di coordinate di trama codificate nel formato vertice. Quando si includono i flag D3DTSS \_ TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION o D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR nel valore assegnato a questo stato, il comportamento del sistema è piuttosto diverso. Se uno di questi flag è presente, la fase della trama ignora le coordinate della trama all'interno del formato vertice a favore delle coordinate generate dal sistema. I significati per ogni flag sono indicati nell'elenco seguente.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Usare la normale vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinate della trama di input. Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.

I flag dell'indice delle coordinate di trama si escludono a vicenda. Questo esempio usa:

-   Posizione del vertice (nello spazio della fotocamera) come coordinate della trama di input per questa fase della trama
-   Modalità di ritorno a capo impostata nello stato di rendering D3DRENDERSTATE \_ WRAP1


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Le coordinate di trama generate automaticamente sono particolarmente utili come valori di input per una trasformazione delle coordinate di trama o per eliminare la necessità che l'applicazione calcoli vettori a tre elementi per le mappe dell'ambiente cubico.

Il mapping sphere usa una mappa di trama pre-ricalcolata (in fase di modello) che contiene l'intero ambiente come riflesso da una sfera cromata. Direct3D ha una funzionalità di generazione delle coordinate di trama che usa lo stato di rendering D3DTSS \_ TCI CAMERASPACENORMAL, che accetta la normale del vertice nello spazio della fotocamera e la inserisce in una trasformazione di trama per generare le coordinate della \_ trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elaborazione delle coordinate di trama](texture-coordinate-processing.md)
</dt> <dt>

[Trasformazioni delle coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Mapping dell'ambiente cubico (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
