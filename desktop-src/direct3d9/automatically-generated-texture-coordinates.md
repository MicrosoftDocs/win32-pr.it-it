---
title: Coordinate di trama generate automaticamente (Direct3D 9)
description: Il sistema può usare la posizione di spazio della fotocamera trasformata o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per indirizzare una mappa dell'ambiente cubica.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305113"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Coordinate di trama generate automaticamente (Direct3D 9)

Il sistema può usare la posizione di spazio della fotocamera trasformata o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per indirizzare una mappa dell'ambiente cubica. Analogamente alle coordinate di trama specificate in modo esplicito in un vertice, è possibile usare le coordinate di trama generate automaticamente come input per le trasformazioni di coordinate di trama.

Le coordinate di trama generate automaticamente possono ridurre significativamente la larghezza di banda necessaria per i dati di geometria eliminando la necessità di coordinate di trama esplicite nel formato vertice. In molti casi, le coordinate di trama generate dal sistema possono essere usate con le trasformazioni per produrre effetti speciali. Naturalmente, si tratta di una funzionalità per scopi specifici e si useranno coordinate di trama esplicite per molte occasioni.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Configurazione delle coordinate di trama generate automaticamente

In C++ lo stato della \_ fase di trama D3DTSS TEXCOORDINDEX (dal tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) controlla il modo in cui il sistema genera le coordinate di trama.

In genere, questo stato indica al sistema di usare un particolare set di coordinate di trama codificate in formato vertice. Quando si includono i \_ flag D3DTSS TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION o D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR nel valore assegnato a questo stato, il comportamento del sistema è piuttosto diverso. Se uno di questi flag è presente, la fase di trama ignora le coordinate di trama all'interno del formato del vertice a favore delle coordinate generate dal sistema. I significati per ogni flag sono riportati nell'elenco seguente.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Usare il vertice normale, trasformato nello spazio della fotocamera, come coordinate di trama di input.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate di trama di input.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinate di trama di input. Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.

I flag di indice delle coordinate di trama si escludono a vicenda. Questo esempio USA:

-   Posizione del vertice (nello spazio della fotocamera) come coordinate di trama di input per questa fase della trama
-   Modalità a capo impostata nello stato di \_ rendering WRAP1 di D3DRENDERSTATE


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Le coordinate di trama generate automaticamente sono più utili come valori di input per una trasformazione di coordinate di trama o per eliminare la necessità che l'applicazione calcoli i vettori di tre elementi per le mappe dell'ambiente cubico.

Il mapping di Sphere usa una mappa di trama pre-calcolata (al momento del modello) che contiene l'intero ambiente come riflesso da una sfera cromata. Direct3D dispone di una funzionalità di generazione di coordinate di trama che usa lo stato di rendering D3DTSS \_ TCI \_ CAMERASPACENORMAL, che usa la normale parte del vertice nello spazio della fotocamera e la inserisce in una trasformazione di trama per generare coordinate di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elaborazione delle coordinate di trama](texture-coordinate-processing.md)
</dt> <dt>

[Trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Mapping dell'ambiente cubico (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
