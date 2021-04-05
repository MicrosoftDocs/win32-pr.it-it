---
description: Scrittura di filtri di trasformazione
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Scrittura di filtri di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967689"
---
# <a name="writing-transform-filters"></a>Scrittura di filtri di trasformazione

In questa sezione viene descritto come scrivere un filtro di trasformazione, definito come filtro con un pin di input e un pin di output identici. Per illustrare i passaggi, in questa sezione viene descritto un filtro di trasformazione ipotetico che restituisce il video codificato in fase di esecuzione (RLE). Non viene descritto l'algoritmo di codifica RLE, ma solo le attività specifiche di DirectShow. DirectShow fornisce già un codec RLE tramite il filtro del [compressore AVI](avi-compressor-filter.md) .

Questa sezione presuppone che si userà la libreria di classi base DirectShow per creare filtri. Sebbene sia possibile scrivere un filtro senza di esso, è consigliabile utilizzare la libreria di classi di base.

> [!Note]  
> Prima di scrivere un filtro di trasformazione, valutare se un oggetto DMO (DirectX Media Object) soddisfi i requisiti. DMOs può eseguire molte delle stesse operazioni dei filtri e il modello di programmazione per DMOs è più semplice. DMOs sono ospitati in DirectShow tramite il filtro del [wrapper DMO](dmo-wrapper-filter.md) , ma possono essere usati anche all'esterno di DirectShow. DMOs è ora la soluzione consigliata per codificatori e decodificatori.

 

Questa sezione include gli argomenti seguenti:

-   [Passaggio 1. Scegliere una classe di base](step-1--choose-a-base-class.md)
-   [Passaggio 2. Dichiarare la classe filter](step-2--declare-the-filter-class.md)
-   [Passaggio 3. Negoziazione del tipo di supporto multimediale](step-3--support-media-type-negotiation.md)
-   [Passaggio 4. Imposta proprietà allocatore](step-4--set-allocator-properties.md)
-   [Passaggio 5. Trasforma l'immagine](step-5--transform-the-image.md)
-   [Passaggio 6. Aggiunta del supporto per COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di filtri DirectShow](building-directshow-filters.md)
</dt> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



