---
description: Panoramica del flusso di dati in DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: Panoramica del flusso di dati in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482260"
---
# <a name="overview-of-data-flow-in-directshow"></a>Panoramica del flusso di dati in DirectShow

Questa sezione offre una panoramica generale del funzionamento del flusso di dati in DirectShow. Informazioni dettagliate sono disponibili in altre sezioni della documentazione.

I dati vengono conservati nei buffer, che sono semplicemente matrici di byte. Ogni buffer è incluso in un oggetto COM denominato *esempio multimediale*, che implementa l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Gli esempi vengono creati da un altro tipo di oggetto, denominato allocatore, che implementa l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Un allocatore viene assegnato per ogni connessione pin, sebbene due o più connessioni pin possano condividere lo stesso allocatore. Questo processo è illustrato nella figura seguente.

![buffer, esempi e allocatori](images/dataflow.png)

Ogni allocatore crea un pool di esempi di supporti e alloca i buffer per ogni campione. Ogni volta che un filtro deve riempire un buffer con i dati, richiede un campione dall'allocatore chiamando [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Se l'allocatore contiene esempi che non sono attualmente in uso da un altro filtro, il metodo **GetBuffer** restituisce immediatamente un puntatore all'esempio. Se tutti gli esempi dell'allocatore sono in uso, il metodo si blocca fino a quando non viene reso disponibile un campione. Quando il metodo restituisce un esempio, il filtro inserisce i dati nel buffer, imposta i flag appropriati nell'esempio (incluso un timestamp) e recapita l'esempio downstream.

Quando un filtro renderer riceve un campione, controlla il timestamp e lo include nell'esempio fino a quando l'orologio di riferimento del grafico del filtro non indica che è necessario eseguire il rendering dei dati. Quando il filtro esegue il rendering dei dati, rilascia l'esempio. L'esempio non torna al pool di campioni dell'allocatore fino a quando il conteggio dei riferimenti dell'esempio non è pari a zero, vale a dire che ogni filtro ha rilasciato l'esempio. Questo processo è illustrato nella figura seguente.

![decodificatore in attesa di un esempio di supporto libero](images/dataflow2.png)

Il filtro upstream può essere eseguito in avanti rispetto al renderer, ovvero potrebbe riempire i buffer più velocemente di quanto il renderer li utilizzi. Anche in questo caso, gli esempi non vengono sottoposti a rendering in anticipo, perché il renderer include ognuno fino al momento della presentazione. Inoltre, il filtro upstream non sovrascrive i buffer accidentalmente, perché **GetSample** restituisce solo campioni che non sono altrimenti in uso. La quantità in base alla quale il filtro upstream può essere eseguito in anticipo è determinato dal numero di campioni nel pool dell'allocatore.

Il diagramma precedente Mostra solo un allocatore, ma in genere sono presenti diversi allocatori per ogni flusso. Pertanto, quando il renderer rilascia un campione, può avere un effetto a catena. Il diagramma seguente illustra una situazione in cui un decodificatore contiene un frame video compresso mentre attende che il renderer rilasci un campione. Un filtro del parser è anche in attesa del decodificatore per rilasciare un campione.

![due filtri in attesa di esempi](images/dataflow3.png)

Quando il renderer rilascia l'esempio, la chiamata in sospeso del decodificatore a **GetBuffer** restituisce. Il decodificatore può quindi decodificare il frame video compresso e rilasciare l'esempio che teneva, sbloccando così la chiamata a **GetBuffer** in sospeso del parser.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



