---
description: Informazioni sugli effetti di Direct3D 10. Un effetto è lo stato della pipeline, impostato da espressioni scritte in HLSL e da una sintassi specifica del framework degli effetti.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Effetti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a9a863fd34c5bb99389139d09860812b16b4fa
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010914"
---
# <a name="effects-direct3d-10"></a>Effetti (Direct3D 10)

Un effetto DirectX è una raccolta di stato della pipeline, impostata da espressioni scritte in [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) e da una sintassi specifica del framework degli effetti. Dopo aver eseguito la compilazione di un effetto, usare le API del framework degli effetti per il rendering. La funzionalità degli effetti può variare da un elemento semplice come un vertex shader che trasforma la geometria e un pixel shader che restituisce un colore a tinta unita, a una tecnica di rendering che richiede più passaggi, usa ogni fase della pipeline grafica e modifica lo stato dello shader e lo stato della pipeline non associato agli shader programmabili.

Il primo passaggio consiste nell'organizzare lo stato che si vuole controllare in un effetto. Sono inclusi lo stato dello shader (vertex, geometry e pixel shader), lo stato della trama e del campionatore usato dagli shader e altri stati della pipeline non programmabili. È possibile creare un effetto in memoria come stringa di testo, ma in genere le dimensioni sono sufficienti per archiviare lo stato dell'effetto in un file di effetto (un file di testo che termina con un'estensione fx). Per usare un effetto, è necessario compilarlo (per controllare la sintassi HLSL e la sintassi del framework degli effetti), inizializzare lo stato dell'effetto tramite chiamate API e modificare il ciclo di rendering per chiamare le API di rendering.

-   [Organizzazione dello stato in un effetto](d3d10-graphics-programming-guide-effects-organize.md)
-   [Interfacce del sistema di effetti](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Specializing Interfaces](d3d10-graphics-reference-effect-specializing.md)
-   [Rendering di un effetto](d3d10-graphics-programming-guide-effects-render.md)

Un effetto incapsula tutto lo stato di rendering richiesto da un determinato effetto in una singola funzione di rendering denominata tecnica. Un passaggio è un sotto-set di una tecnica, che contiene lo stato di rendering. Per implementare un effetto di rendering a più passaggi, implementare uno o più passaggi all'interno di una tecnica. Si supponga, ad esempio, di voler eseguire il rendering di una geometria con un set di buffer di profondità/stencil e quindi di disegnare alcuni sprite sopra di questo. È possibile implementare il rendering della geometria nel primo passaggio e il disegno dello sprite nel secondo passaggio. Per eseguire il rendering dell'effetto, è sufficiente eseguire il rendering di entrambi i passaggi nel ciclo di rendering. È possibile implementare un numero qualsiasi di tecniche in un effetto. Naturalmente, maggiore è il numero di tecniche, maggiore sarà il tempo di compilazione per l'effetto. Un modo per sfruttare questa funzionalità consiste nel creare effetti con tecniche progettate per l'esecuzione su hardware diverso. Ciò consente a un'applicazione di eseguire normalmente il downgrade delle prestazioni in base alle funzionalità hardware rilevate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
