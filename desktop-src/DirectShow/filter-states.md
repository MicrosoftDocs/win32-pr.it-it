---
description: Stati filtro
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Stati filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d61f66e1446d97d289f7e489f116f747f339d9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304199"
---
# <a name="filter-states"></a>Stati filtro

I filtri possono avere tre stati: arrestato, sospeso e in esecuzione. Lo scopo dello stato Paused consiste nel cue i dati nel grafico, in modo che un comando Run risponda immediatamente. Filter Graph Manager controlla tutte le transizioni di stato. Quando un'applicazione chiama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)o [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), il gestore del grafico dei filtri chiama il metodo [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) corrispondente su tutti i filtri. Le transizioni tra arrestato e in esecuzione passano sempre attraverso lo stato sospeso, quindi se l'applicazione chiama l' **esecuzione** su un grafico interrotto, il gestore del grafico del filtro sospende il grafo prima di eseguirlo.

Per la maggior parte dei filtri, gli stati in esecuzione e sospesi sono identici. Si consideri il seguente grafico filtro:

Renderer > di origine > trasformazione

Si supponga ora che il filtro di origine non sia un'origine di acquisizione in tempo reale. Quando il filtro di origine viene sospeso, viene creato un thread che genera nuovi dati e lo scrive in un campione multimediale il più rapidamente possibile. Il thread esegue il push degli esempi downstream chiamando [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input del filtro di trasformazione. Il filtro di trasformazione riceve gli esempi sul thread del filtro di origine. Può usare un thread di lavoro per recapitare gli esempi al renderer, ma in genere li recapita sullo stesso thread. Mentre il renderer viene sospeso, attende la ricezione di un campione. Una volta ricevuto, questo campione viene bloccato e archiviato a tempo indefinito. Se si tratta di un renderer video, viene visualizzato l'esempio come immagine poster, ridisegnando l'immagine in modo necessario.

A questo punto, il flusso è completo e pronto per il rendering. Se il grafo rimane in pausa, gli esempi vengono "ammucchiati" nel grafico dietro il primo campione, fino a quando ogni filtro non è bloccato in [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Tuttavia, non viene perso alcun dato. Quando il thread di origine viene sbloccato, riprende semplicemente dal punto in cui è stato bloccato.

Il filtro di origine e il filtro di trasformazione ignorano la transizione da sospesa a in esecuzione, ma semplicemente continuano a elaborare i dati il più rapidamente possibile. Tuttavia, quando viene eseguito, il renderer avvia il rendering degli esempi. Esegue prima di tutto il rendering dell'esempio mantenuto mentre era sospeso. Quindi, ogni volta che viene ricevuto un nuovo esempio, viene calcolata l'ora di presentazione dell'esempio. Per informazioni dettagliate, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md). Il renderer include ogni campione fino al momento della presentazione, a quel punto viene eseguito il rendering dell'esempio. Sebbene attenda l'ora di presentazione, si blocca nel metodo [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o riceve nuovi esempi in un thread di lavoro con una coda. I filtri upstream dal renderer non sono interessati dalla pianificazione.

Le origini live, ad esempio i dispositivi di acquisizione, rappresentano un'eccezione a questa architettura generale. Con un'origine live, non è opportuno riportare i dati in anticipo. L'applicazione potrebbe sospendere il grafico e attendere molto tempo prima di eseguirlo. Il grafico non deve eseguire il rendering degli esempi "obsoleti". Pertanto, un'origine live non produce alcun campione durante la pausa, solo durante l'esecuzione. Per segnalare questo fatto al gestore del grafico dei filtri, il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) del filtro di origine restituisce il segnale non può essere di tipo VFW \_ \_ \_ . Questo codice restituito indica che il filtro è stato spostato sullo stato sospeso, anche se il renderer non ha ricevuto dati.

Quando si interrompe un filtro, vengono rifiutati tutti gli altri esempi recapitati. I filtri di origine arrestano i thread di streaming e altri filtri arrestano tutti i thread di lavoro che possono avere creato. I pin decommitno gli allocatori.

### <a name="state-transitions"></a>Transizioni di stato

Filter Graph Manager esegue tutte le transizioni di stato nell'ordine upstream, a partire dal renderer e procedendo all'indietro rispetto al filtro di origine. Questo ordinamento è necessario per impedire che gli esempi vengano eliminati e impedire il deadlock del grafo. Le transizioni di stato più cruciali sono sospese e interrotte:

-   Arrestato in sospeso: quando ogni filtro viene sospeso, diventa pronto a ricevere esempi dal filtro successivo. Il filtro di origine è l'ultimo oggetto da sospendere. Crea il thread di streaming e inizia a consegnare gli esempi. Poiché tutti i filtri downstream sono sospesi, nessun filtro rifiuta alcun campione. Il gestore del grafo del filtro non completa la transizione fino a quando ogni renderer del grafico non ha ricevuto un campione (ad eccezione delle origini live, come descritto in precedenza).
-   Sospeso in interrotto: quando si arresta un filtro, vengono rilasciati tutti i campioni che include, che sblocca tutti i filtri upstream in attesa in [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Se il filtro è in attesa di una risorsa all'interno del metodo [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , si interrompe in attesa e viene restituito dalla **ricezione**, che sblocca il filtro chiamante. Pertanto, quando il gestore del grafico del filtro arresta il successivo filtro upstream, il filtro non viene bloccato in **GetBuffer** o **Receive** e può rispondere al comando stop. Il filtro upstream potrebbe recapitare alcuni esempi aggiuntivi prima di ottenere il comando stop, ma il filtro downstream li rifiuta semplicemente perché è già stato arrestato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



