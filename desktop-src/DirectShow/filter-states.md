---
description: Filtrare gli stati
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Filtrare gli stati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015739"
---
# <a name="filter-states"></a>Filtrare gli stati

I filtri hanno tre stati possibili: arrestato, sospeso ed in esecuzione. Lo scopo dello stato sospeso è quello di aggiungere dati nel grafico, in modo che un comando run risponda immediatamente. Il filtro Graph Manager controlla tutte le transizioni di stato. Quando un'applicazione chiama [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)o [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), Filter Graph Manager chiama il metodo [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) corrispondente su tutti i filtri. Le transizioni tra l'arresto e l'esecuzione passano  sempre attraverso lo stato sospeso, quindi se l'applicazione chiama Esegui in un grafico arrestato, Filter Graph Manager sospende il grafico prima di eseguirlo.

Per la maggior parte dei filtri, gli stati in esecuzione e in pausa sono identici. Si consideri il grafico di filtro seguente:

Renderer > transform > di origine

Si supponga per il momento che il filtro di origine non sia un'origine di acquisizione live. Quando il filtro di origine viene sospeso, crea un thread che genera nuovi dati e li scrive in campioni multimediali il più rapidamente possibile. Il thread "esegue il push" degli esempi a valle chiamando [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input del filtro di trasformazione. Il filtro di trasformazione riceve gli esempi nel thread del filtro di origine. Può usare un thread di lavoro per recapitare gli esempi al renderer, ma in genere li recapita nello stesso thread. Mentre il renderer è sospeso, attende di ricevere un esempio. Dopo averne ricevuto uno, blocca e mantiene l'esempio a tempo indeterminato. Se si tratta di un renderer video, visualizza l'esempio come immagine poster, ridisegnando l'immagine in base alle esigenze.

A questo punto, il flusso è completamente cued e pronto per il rendering. Se il grafo rimane sospeso, gli esempi si "accumulano" nel grafico dietro il primo campione, fino a quando ogni filtro non viene bloccato in [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Non vengono tuttavia persi dati. Dopo che il thread di origine è stato sbloccato, riprende semplicemente dal punto in cui è stato bloccato.

Il filtro di origine e il filtro di trasformazione ignorano la transizione da sospesa a in esecuzione. Continuano semplicemente a elaborare i dati il più velocemente possibile. Tuttavia, quando il renderer viene eseguito, avvia il rendering degli esempi. Esegue prima di tutto il rendering dell'esempio che ha mantenuto mentre è stato sospeso. Quindi, ogni volta che riceve un nuovo esempio, calcola l'ora di presentazione dell'esempio. Per informazioni dettagliate, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md). Il renderer mantiene ogni campione fino all'ora di presentazione, a quel punto esegue il rendering dell'esempio. Durante l'attesa del tempo di presentazione, si blocca nel metodo [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o riceve nuovi esempi in un thread di lavoro con una coda. I filtri upstream dal renderer non sono coinvolti nella pianificazione.

Le origini in tempo reale, ad esempio i dispositivi di acquisizione, sono un'eccezione a questa architettura generale. Con un'origine in tempo reale, non è appropriato segnalere in anticipo i dati. L'applicazione potrebbe sospendere il grafo e quindi attendere molto tempo prima di eseguire il grafico. Il grafico non deve eseguire il rendering degli esempi "non obsoleti". Pertanto, un'origine live non produce campioni durante la sospensione, solo durante l'esecuzione. Per segnalare questo fatto a Filter Graph Manager, il metodo [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) del filtro di origine restituisce VFW \_ S \_ CANT \_ CUE. Questo codice restituito indica che il filtro è stato sospeso, anche se il renderer non ha ricevuto dati.

Quando un filtro si arresta, rifiuta altri campioni recapitati. I filtri di origine arrestano i thread di streaming e altri filtri arrestano tutti i thread di lavoro creati. I pin dismettono i relativi allocatori.

### <a name="state-transitions"></a>Transizioni di stato

Filter Graph Manager esegue tutte le transizioni di stato in ordine upstream, a partire dal renderer e procedendo a ritroso fino al filtro di origine. Questo ordinamento è necessario per evitare che i campioni vengano eliminati e per impedire il deadlock del grafo. Le transizioni di stato più importanti sono tra sospese e arrestate:

-   Arrestato per essere sospeso: quando ogni filtro viene sospeso, diventa pronto a ricevere campioni dal filtro successivo. Il filtro di origine è l'ultimo da sospendere. Crea il thread di streaming e inizia a fornire esempi. Poiché tutti i filtri downstream vengono sospesi, nessun filtro rifiuta gli esempi. Filter Graph Manager non completa la transizione fino a quando ogni renderer nel grafo non ha ricevuto un campione (ad eccezione delle origini in tempo reale, come descritto in precedenza).
-   Sospeso per essere arrestato: quando un filtro si arresta, rilascia tutti i campioni che contiene, che sblocca eventuali filtri upstream in attesa in [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Se il filtro è in attesa di una risorsa all'interno del [**metodo Receive,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) interrompe l'attesa e restituisce da **Receive**, che sblocca il filtro chiamante. Pertanto, quando Filter Graph Manager arresta il filtro upstream successivo, tale filtro non viene bloccato in **GetBuffer** o **Receive** e può rispondere al comando stop. Il filtro upstream potrebbe fornire alcuni esempi aggiuntivi prima di ottenere il comando stop, ma il filtro downstream li rifiuta semplicemente, perché è già stato arrestato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati Flow nel filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



