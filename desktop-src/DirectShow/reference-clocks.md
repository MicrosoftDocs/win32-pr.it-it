---
description: Orologi di riferimento
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Orologi di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ad0a262b36ce78c6a2f355b30b3c6876c7e78a7807970592b6f15287c0e2c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697111"
---
# <a name="reference-clocks"></a>Orologi di riferimento

Una funzione di Filter Graph Manager è sincronizzare tutti i filtri nel grafico con lo stesso orologio, denominato *clock di riferimento.*

Qualsiasi oggetto che espone [**l'interfaccia IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) può fungere da clock di riferimento. L'orologio di riferimento può essere fornito da un DirectShow, in genere il renderer audio, che ha accesso a un timer hardware. Come fallback, Gestione filtri Graph può usare l'ora di sistema.

Nominalmente, un orologio di riferimento misura il tempo in intervalli di 100 nanosecondi, anche se l'accuratezza effettiva dell'orologio potrebbe essere inferiore. Per recuperare l'ora corrente dell'orologio, chiamare il [**metodo IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) La baseline dell'orologio, ovvero l'ora da cui inizia il conteggio, dipende dall'implementazione, quindi il valore restituito da **GetTime** non è intrinsecamente significativo. Ciò che conta è il delta rispetto all'avvio dell'esecuzione del grafo.

Anche se l'accuratezza di un clock di riferimento può variare, le ore restituite dal [**metodo GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentano in modo monotono. In altre parole, gli orari dell'orologio non andranno mai indietro. Se un clock di riferimento genera gli orari di clock da un'origine hardware e l'orologio dell'hardware passa indietro (ad esempio, se è presente una regolazione dell'orologio), il **metodo GetTime** deve continuare a restituire l'ultima ora segnalata fino a quando l'orologio hardware non viene aggiornato. Per altre informazioni, vedere [**Classe CBaseReferenceClock.**](cbasereferenceclock.md)

**Orologio di riferimento predefinito**

Gestione filtri Graph seleziona automaticamente un orologio di riferimento quando viene eseguito il grafico. Usa l'algoritmo seguente per selezionare l'orologio:

-   Se l'applicazione ha selezionato un orologio (vedere di seguito), usare tale orologio.
-   Se il grafico contiene un filtro di origine live che supporta [**IReferenceClock,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)usare tale filtro. Per la definizione di un'origine live, vedere [Origini live.](live-sources.md)
-   Se il grafico NON contiene filtri di origine attivi, usare qualsiasi filtro nel grafico che supporti [**IReferenceClock,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)a partire dai renderer e funzionando a monte. Preferisce i filtri connessi rispetto ai filtri non connessi. Se il grafico esegue il rendering di un flusso audio, questo passaggio nell'algoritmo selezionerà in genere il filtro del renderer audio.
-   Se nessun filtro fornisce un orologio appropriato, usare l'orologio di riferimento di [sistema](system-reference-clock.md), che si basa sull'ora di sistema.

**Impostazione dell'orologio di riferimento**

Un'applicazione può selezionare un orologio chiamando il [**metodo IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) in Filter Graph Manager. È consigliabile eseguire questa operazione solo se si ha un motivo particolare per preferire un altro orologio.

È possibile indicare a Filter Graph Manager di non usare un clock di riferimento chiamando [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) con il valore **NULL.** Ad esempio, è possibile eseguire questa operazione per elaborare gli esempi il più rapidamente possibile. Per ripristinare l'orologio di riferimento predefinito, chiamare il metodo [**IFilterGraph::SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) in Filter Graph Manager.

Ogni volta che l'orologio di riferimento cambia, Il gestore Graph notifica ogni filtro chiamando il relativo [**metodo IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) Le applicazioni non devono mai chiamare questo metodo sui filtri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell Graph clock](setting-the-graph-clock.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



