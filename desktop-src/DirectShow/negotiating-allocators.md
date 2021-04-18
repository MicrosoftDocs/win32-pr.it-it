---
description: Negozi di allocatori
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Negozi di allocatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303737"
---
# <a name="negotiating-allocators"></a>Negozi di allocatori

Quando due pin si connettono, devono disporre di un meccanismo per lo scambio di dati multimediali. Questo meccanismo viene chiamato *trasporto*. In generale, l'architettura DirectShow è neutra per i trasporti. Due filtri possono accettare la connessione utilizzando qualsiasi trasporto supportato da entrambi.

Il trasporto più comune è il trasporto di *memoria locale* , in cui i dati multimediali si trovano nella memoria principale. Esistono due tipi di trasporto di memoria locale, il *modello push* e il *modello pull*. Nel modello push, il filtro di origine inserisce i dati nel filtro downstream usando l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input del filtro downstream. Nel modello pull il filtro downstream richiede i dati dal filtro di origine, usando l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sul pin di output del filtro di origine. Per altre informazioni su questi due modelli di flusso di dati, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).

Nel trasporto di memoria locale, l'oggetto responsabile dell'allocazione dei buffer di memoria viene definito *allocatore*. Un allocatore supporta l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Entrambi i pin condividono un solo allocatore. Entrambi i pin possono fornire un allocatore, ma il pin di output seleziona l'allocatore da usare.

Il pin di output imposta anche le proprietà dell'allocatore, che determinano il numero di buffer creati dall'allocatore, le dimensioni di ogni buffer e l'allineamento della memoria. Il pin di output potrebbe rinviare al pin di input per i requisiti del buffer.

In una connessione **IMemInputPin** , la negoziazione dell'allocatore funziona nel modo seguente:

1.  Facoltativamente, il pin di output chiama [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Questo metodo recupera i requisiti del buffer del PIN di input, ad esempio l'allineamento della memoria. In generale, il pin di output deve rispettare la richiesta del PIN di input, a meno che non esista un buon motivo per non farlo.
2.  Facoltativamente, il pin di output chiama [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Questo metodo richiede un allocatore dal pin di input. Il pin di input ne fornisce uno oppure restituisce un codice di errore.
3.  Il pin di output seleziona un allocatore. Può utilizzarne una fornita dal pin di input o crearne una personalizzata.
4.  Il pin di output chiama [**IMemAllocator:: seproprietà**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) per impostare le proprietà dell'allocatore. Tuttavia, l'allocatore potrebbe non rispettare le proprietà richieste. Questo può verificarsi, ad esempio, se il pin di input fornisce l'allocatore. L'allocatore restituisce le proprietà effettive come parametro di output nel metodo **seproperties** .
5.  Outpin chiama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) per informare il pin di input della selezione.
6.  Il pin di input deve chiamare [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) per verificare se le proprietà dell'allocatore sono accettabili.
7.  Il pin di output è responsabile del commit e del commit dell'allocatore. Questo errore si verifica quando il flusso viene avviato e interrotto.

In una connessione **IAsyncReader** , la negoziazione dell'allocatore funziona nel modo seguente:

1.  Il pin di input chiama [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) sul pin di output. Il pin di input specifica i requisiti del buffer e, facoltativamente, fornisce un allocatore.
2.  Il pin di output seleziona un allocatore. Può usare quello fornito dal pin di input, se disponibile, o crearne uno proprio.
3.  Il pin di output restituisce l'allocatore come parametro in uscita nel metodo **RequestAllocator** . Il pin di input deve controllare le proprietà dell'allocatore.
4.  Il pin di input è responsabile del commit e del decommit dell'allocatore.
5.  In qualsiasi momento durante il processo di negoziazione dell'allocatore, il PIN potrebbe non riuscire a connettersi.
6.  Se il pin di output usa l'allocatore del PIN di input, può usare tale allocatore solo per recapitare campioni al pin di input. Il filtro proprietario non deve usare l'allocatore per recapitare esempi ad altri pin.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fornire un allocatore personalizzato](providing-a-custom-allocator.md)
</dt> </dl>

 

 



