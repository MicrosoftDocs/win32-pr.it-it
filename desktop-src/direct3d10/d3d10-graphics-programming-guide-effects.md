---
description: Un effetto DirectX è una raccolta dello stato della pipeline, impostata dalle espressioni scritte in HLSL e da una sintassi specifica per il Framework degli effetti.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Effetti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305119"
---
# <a name="effects-direct3d-10"></a>Effetti (Direct3D 10)

Un effetto DirectX è una raccolta dello stato della pipeline, impostata dalle espressioni scritte in [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) e da una sintassi specifica per il Framework degli effetti. Dopo la compilazione di un effetto, utilizzare le API del Framework effetti per eseguire il rendering. La funzionalità degli effetti può variare da qualcosa di semplice come un vertex shader che trasforma la geometria e un pixel shader che restituisce un colore a tinta unita, a una tecnica di rendering che richiede più sessioni, utilizza ogni fase della pipeline grafica e modifica lo stato dello shader, nonché lo stato della pipeline non associato agli shader programmabili.

Il primo passaggio consiste nell'organizzare lo stato che si vuole controllare in un effetto. Questo include lo stato dello shader (Vertex, Geometry e pixel shader), lo stato di trama e campionatore usato dagli shader e altro stato della pipeline non programmabile. È possibile creare un effetto in memoria come una stringa di testo, ma in genere la dimensione diventa sufficientemente grande da poter archiviare lo stato dell'effetto in un file di effetti (un file di testo che termina con l'estensione FX). Per usare un effetto, è necessario compilarlo (per verificare la sintassi di HLSL e la sintassi del Framework di effetto), inizializzare lo stato dell'effetto tramite chiamate API e modificare il ciclo di rendering per chiamare le API di rendering.

-   [Organizzazione dello stato in un effetto](d3d10-graphics-programming-guide-effects-organize.md)
-   [Interfacce di sistema effetti](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Interfacce specializzate](d3d10-graphics-reference-effect-specializing.md)
-   [Rendering di un effetto](d3d10-graphics-programming-guide-effects-render.md)

Un effetto incapsula tutto lo stato di rendering richiesto da un particolare effetto in una singola funzione di rendering denominata tecnica. Un passaggio è un subset di una tecnica che contiene lo stato di rendering. Per implementare un effetto di rendering a più passaggi, implementare uno o più passaggi all'interno di una tecnica. Si immagini, ad esempio, di voler eseguire il rendering di una geometria con un set di buffer di profondità/stencil, quindi disegnare alcuni sprite. È possibile implementare il rendering Geometry nel primo passaggio e il disegno sprite nel secondo passaggio. Per eseguire il rendering dell'effetto, è sufficiente eseguire il rendering di entrambi i passaggi nel ciclo di rendering. È possibile implementare un numero qualsiasi di tecniche in un effetto. Naturalmente, maggiore è il numero di tecniche, maggiore è il tempo di compilazione per l'effetto. Un modo per sfruttare questa funzionalità consiste nel creare effetti con tecniche progettate per l'esecuzione su hardware diverso. Questo consente a un'applicazione di eseguire correttamente il downgrade delle prestazioni in base alle funzionalità hardware rilevate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
