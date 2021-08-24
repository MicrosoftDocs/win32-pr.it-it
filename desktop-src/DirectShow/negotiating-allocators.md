---
description: Negoziazione degli allocatori
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Negoziazione degli allocatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710b8315bfd44371a82d995afa56483414623136a6ce5c510babd5ea07b4b8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790941"
---
# <a name="negotiating-allocators"></a>Negoziazione degli allocatori

Quando due pin si connettono, è necessario un meccanismo per lo scambio di dati multimediali. Questo meccanismo è denominato *trasporto*. In generale, l'architettura DirectShow è neutra per i trasporti. Due filtri possono accettare di connettersi usando qualsiasi trasporto che entrambi supportano.

Il trasporto più comune è il *trasporto di memoria* locale, in cui i dati multimediali risiedono nella memoria principale. Esistono due tipi di trasporto della memoria locale, il *modello push* e il *modello pull.* Nel modello push il filtro di origine inserisce i dati nel filtro downstream usando [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input del filtro downstream. Nel modello pull il filtro downstream richiede i dati dal filtro di origine, usando [**l'interfaccia IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sul pin di output del filtro di origine. Per altre informazioni su questi due modelli di flusso di dati, vedere [Data Flow in Filter Graph](data-flow-in-the-filter-graph.md).

Nel trasporto della memoria locale, l'oggetto responsabile dell'allocazione dei buffer di memoria è denominato *allocatore*. Un allocatore supporta [**l'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) Entrambi i pin condividono un singolo allocatore. Entrambi i pin possono fornire un allocatore, ma il pin di output seleziona l'allocatore da usare.

Il pin di output imposta anche le proprietà dell'allocatore, che determinano il numero di buffer creati dall'allocatore, le dimensioni di ogni buffer e l'allineamento della memoria. Il pin di output potrebbe rinviare al pin di input per i requisiti del buffer.

In una **connessione IMemInputPin** la negoziazione dell'allocatore funziona come segue:

1.  Facoltativamente, il pin di output [**chiama IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Questo metodo recupera i requisiti del buffer del pin di input, ad esempio l'allineamento della memoria. In generale, il pin di output deve rispettare la richiesta del pin di input, a meno che non vi sia un motivo valido per non.
2.  Facoltativamente, il pin di output chiama [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Questo metodo richiede un allocatore dal pin di input. Il pin di input ne fornisce uno o restituisce un codice di errore.
3.  Il pin di output seleziona un allocatore. Può usare uno fornito dal pin di input o crearne uno proprio.
4.  Il pin di output chiama [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) per impostare le proprietà dell'allocatore. Tuttavia, l'allocatore potrebbe non rispettare le proprietà richieste. Ad esempio, questo problema può verificarsi se il pin di input fornisce l'allocatore. L'allocatore restituisce le proprietà effettive come parametro di output nel **metodo SetProperties.**
5.  L'elemento outpin [**chiama IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) per informare il pin di input della selezione.
6.  Il pin di input deve chiamare [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) per verificare se le proprietà dell'allocatore sono accettabili.
7.  Il pin di output è responsabile del commit e del decommitting dell'allocatore. Ciò si verifica all'avvio e all'arresto del flusso.

In una **connessione IAsyncReader** la negoziazione dell'allocatore funziona come segue:

1.  Il pin di input [**chiama IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) sul pin di output. Il pin di input specifica i requisiti del buffer e, facoltativamente, fornisce un allocatore.
2.  Il pin di output seleziona un allocatore. Può usare quello fornito dal pin di input, se presente, o crearne uno proprio.
3.  Il pin di output restituisce l'allocatore come parametro in uscita nel **metodo RequestAllocator.** Il pin di input deve controllare le proprietà dell'allocatore.
4.  Il pin di input è responsabile del commit e del decommitting dell'allocatore.
5.  In qualsiasi momento durante il processo di negoziazione dell'allocatore, entrambi i pin possono non riuscire a stabilire la connessione.
6.  Se il pin di output usa l'allocatore del pin di input, può usare tale allocatore solo per distribuire campioni a tale pin di input. Il filtro proprietario non deve usare l'allocatore per distribuire campioni ad altri segnaposto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica di un allocatore personalizzato](providing-a-custom-allocator.md)
</dt> </dl>

 

 



