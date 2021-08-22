---
description: Scegliere una classe di base come parte della scrittura di un filtro di trasformazione. Informazioni sulle classi appropriate per i filtri di trasformazione.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Passaggio 1. Scegliere una classe di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140beba3df02ace21d99779c152a79632fe0b4a1a916c4412c467b0f4ac5627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315881"
---
# <a name="step-1-choose-a-base-class"></a>Passaggio 1. Scegliere una classe di base

Questo è il passaggio 1 dell'esercitazione [Scrittura di filtri di trasformazione](writing-transform-filters.md).

Supponendo che si decida di scrivere un filtro e non un DMO, il primo passaggio consiste nella scelta della classe di base da usare. Le classi seguenti sono appropriate per i filtri di trasformazione:

-   [**CTransformFilter è**](ctransformfilter.md) progettato per i filtri di trasformazione che usano buffer di input e output separati. Questo tipo di filtro viene talvolta definito filtro di copia-trasformazione. Quando un filtro di copia-trasformazione riceve un esempio di input, scrive nuovi dati in un esempio di output e recapita l'esempio di output al filtro successivo.
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) è progettato per i filtri che modificano i dati nel buffer originale, detti anche filtri trans-in-place. Quando un filtro trans-in-place riceve un campione, modifica i dati all'interno di tale esempio e recapita lo stesso esempio a valle. Il pin di input e il pin di output del filtro si connettono sempre con i tipi di supporti corrispondenti.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) è progettato principalmente per decodificatori video. Deriva da **CTransformFilter, ma** include funzionalità per l'eliminazione di frame se il renderer downstream è in ritardo.
-   [**CBaseFilter è**](cbasefilter.md) una classe di filtro generica. Tutte le altre classi di questo elenco derivano tutte **da CBaseFilter**. Se nessuna di esse è adatta, è possibile eseguire il fall back su questa classe. Tuttavia, questa classe richiede anche la maggior parte del lavoro da parte dell'utente.
-   \[! Importante\]  
    > Le trasformazioni video sul posto possono avere un impatto significativo sulle prestazioni di rendering. Le trasformazioni sul posto richiedono operazioni di lettura-modifica/scrittura nel buffer. Se la memoria si trova in una scheda grafica, le operazioni di lettura sono notevolmente più lente. Inoltre, anche una trasformazione di copia può causare operazioni di lettura non intenzionali se non viene implementata con attenzione. Pertanto, è consigliabile eseguire sempre test delle prestazioni se si scrive una trasformazione video.

     

Per il codificatore RLE di esempio, la scelta migliore è **CTransformFilter** o **CVideoTransformFilter**. In realtà, le differenze tra di essi sono per lo più interne, quindi è facile eseguire la conversione da una all'altra. Poiché i tipi di supporti devono essere diversi sui due pin, la **classe CTransInPlaceFilter** non è appropriata per questo filtro. In questo esempio verrà utilizzato **CTransformFilter**.

Successivo: [Passaggio 2. Dichiarare la classe Filter](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



