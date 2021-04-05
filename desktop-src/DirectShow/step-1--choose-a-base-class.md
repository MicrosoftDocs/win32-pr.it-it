---
description: Passaggio 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Passaggio 1. Scegliere una classe di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883121"
---
# <a name="step-1-choose-a-base-class"></a>Passaggio 1. Scegliere una classe di base

Questo è il passaggio 1 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

Supponendo che si decida di scrivere un filtro e non un DMO, il primo passaggio consiste nella scelta della classe di base da usare. Le classi seguenti sono appropriate per i filtri di trasformazione:

-   [**CTransformFilter**](ctransformfilter.md) è progettato per i filtri di trasformazione che usano buffer di input e output distinti. Questo tipo di filtro viene talvolta definito filtro di copia/trasformazione. Quando un filtro di copia-trasformazione riceve un esempio di input, scrive nuovi dati in un esempio di output e recapita l'esempio di output al filtro successivo.
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) è progettato per i filtri che modificano i dati nel buffer originale, detti anche filtri trans-on-Place. Quando un filtro Trans-on-Place riceve un esempio, modifica i dati all'interno dell'esempio e recapita lo stesso campione downstream. Il pin di input e il pin di output del filtro si connettono sempre con i tipi di supporto corrispondenti.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) è progettato principalmente per i decodificatori video. Deriva da **CTransformFilter**, ma include funzionalità per l'eliminazione di frame se il renderer downstream si trova dietro.
-   [**CBaseFilter**](cbasefilter.md) è una classe di filtro generica. Tutte le altre classi in questo elenco derivano da **CBaseFilter**. Se nessuno di essi è adatto, è possibile eseguire il fallback su questa classe. Tuttavia, questa classe richiede anche il maggior numero di lavoro da parte dell'utente.
-   \[! Importante\]  
    > Le trasformazioni video sul posto possono avere un notevole effetto sulle prestazioni di rendering. Le trasformazioni sul posto richiedono operazioni di lettura-modifica-scrittura nel buffer. Se la memoria si trova in una scheda grafica, le operazioni di lettura sono significativamente più lente. Inoltre, anche una trasformazione copia può causare operazioni di lettura indesiderate se non viene implementata con attenzione. Pertanto, è consigliabile eseguire sempre il test delle prestazioni se si scrive una trasformazione video.

     

Per il codificatore RLE di esempio, la scelta migliore è **CTransformFilter** o **CVideoTransformFilter**. Infatti, le differenze tra di esse sono in gran parte interne, pertanto è facile eseguire la conversione da una all'altra. Poiché i tipi di supporto devono essere diversi nei due pin, la classe **CTransInPlaceFilter** non è appropriata per questo filtro. In questo esempio verrà usato **CTransformFilter**.

Successivo: [passaggio 2. Dichiarare la classe filter](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



