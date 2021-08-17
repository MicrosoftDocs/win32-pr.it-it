---
description: Scrittura di filtri di trasformazione
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Scrittura di filtri di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816838"
---
# <a name="writing-transform-filters"></a>Scrittura di filtri di trasformazione

Questa sezione descrive come scrivere un filtro di trasformazione, definito come filtro con esattamente un pin di input e un pin di output. Per illustrare i passaggi, questa sezione descrive un ipotetico filtro di trasformazione che restituisce un video con codifica a lunghezza di esecuzione (RLE). Non descrive l'algoritmo di codifica RLE stesso, ma solo le attività specifiche per DirectShow. (DirectShow fornisce già un codec RLE tramite il filtro [AVI Codec.](avi-compressor-filter.md)

In questa sezione si presuppone che si userà la DirectShow di classi di base per creare filtri. Anche se è possibile scrivere un filtro senza di esso, è consigliabile usare la libreria di classi di base.

> [!Note]  
> Prima di scrivere un filtro di trasformazione, valutare se un oggetto directx media (DMO) soddisfa i requisiti. Le DMO possono eseguire molte delle stesse operazioni dei filtri e il modello di programmazione per le DMO è più semplice. Gli oggetti DMO sono ospitati in DirectShow tramite il filtro [wrapper DMO,](dmo-wrapper-filter.md) ma possono essere usati anche all'esterno DirectShow. I DMO sono ora la soluzione consigliata per codificatori e decodificatori.

 

Questa sezione include gli argomenti seguenti:

-   [Passaggio 1. Scegliere una classe di base](step-1--choose-a-base-class.md)
-   [Passaggio 2. Dichiarare la classe Filter](step-2--declare-the-filter-class.md)
-   [Passaggio 3. Supportare la negoziazione del tipo di supporto](step-3--support-media-type-negotiation.md)
-   [Passaggio 4. Impostare le proprietà dell'allocatore](step-4--set-allocator-properties.md)
-   [Passaggio 5. Trasformare l'immagine](step-5--transform-the-image.md)
-   [Passaggio 6. Aggiungere il supporto per COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione DirectShow filtri](building-directshow-filters.md)
</dt> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



