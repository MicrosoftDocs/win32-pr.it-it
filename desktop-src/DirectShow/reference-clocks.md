---
description: Orologi di riferimento
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Orologi di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303902"
---
# <a name="reference-clocks"></a>Orologi di riferimento

Una funzione del gestore del grafo del filtro è la sincronizzazione di tutti i filtri nel grafico con lo stesso clock, denominato *clock di riferimento*.

Qualsiasi oggetto che espone l'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) può fungere da orologio di riferimento. L'orologio di riferimento potrebbe essere fornito da un filtro DirectShow, in genere il renderer audio, che ha accesso a un timer hardware. Come fallback, il gestore del grafo del filtro può utilizzare l'ora di sistema.

Nominalmente, un orologio di riferimento misura il tempo in intervalli di 100 nanosecondi, sebbene l'accuratezza effettiva dell'orologio potrebbe essere minore. Per recuperare l'ora corrente del clock, chiamare il metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) . La linea di base del clock, ovvero l'ora da cui inizia il conteggio, dipende dall'implementazione, quindi il valore restituito da **getTime** non è intrinsecamente significativo. Ciò che conta è il Delta rispetto all'avvio dell'esecuzione del grafico.

Sebbene l'accuratezza di un clock di riferimento possa variare, le ore restituite dal metodo [**getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) sono garantite per un aumento progressivo costante. In altre parole, i tempi di clock non verranno mai superati. Se un orologio di riferimento genera tempi di clock da un'origine hardware e il clock dell'hardware viene interrotto indietro (ad esempio, se è presente una regolazione dell'orologio), il metodo **getTime** deve continuare a restituire l'ora dell'ultimo report fino a quando l'orologio hardware non viene aggiornato. Per ulteriori informazioni, vedere la [**classe CBaseReferenceClock**](cbasereferenceclock.md).

**Clock di riferimento predefinito**

Il gestore del grafico dei filtri seleziona automaticamente un orologio di riferimento quando il grafico viene eseguito. Usa l'algoritmo seguente per selezionare il clock:

-   Se l'applicazione ha selezionato un clock (vedere di seguito), usare tale clock.
-   Se il grafico contiene un filtro di origine live che supporta [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), usare tale filtro. Per la definizione di un'origine live, vedere [Live](live-sources.md)sources.
-   Se il grafico non contiene filtri di origine attivi, usare qualsiasi filtro nel grafico che supporta [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), a partire dai renderer e lavorando a Monte. Preferisce i filtri connessi su filtri non connessi. Se il grafico sta eseguendo il rendering di un flusso audio, questo passaggio nell'algoritmo normalmente selezionerà il filtro renderer audio.
-   Se nessun filtro fornisce un clock appropriato, utilizzare l' [orologio di riferimento del sistema](system-reference-clock.md), basato sull'ora di sistema.

**Impostazione dell'orologio di riferimento**

Un'applicazione può selezionare un clock chiamando il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) in gestione grafico dei filtri. Questa operazione deve essere eseguita solo se si dispone di un motivo specifico per preferire un altro Clock.

È possibile indicare a Filter Graph Manager di non usare un clock di riferimento chiamando [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) con il valore **null**. Ad esempio, è possibile eseguire questa operazione per elaborare i campioni il più rapidamente possibile. Per ripristinare l'orologio di riferimento predefinito, chiamare il metodo [**IFilterGraph:: SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) in gestione grafico dei filtri.

Ogni volta che viene modificato l'orologio di riferimento, il gestore del grafico dei filtri invia una notifica a ogni filtro chiamando il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) . Le applicazioni non devono mai chiamare questo metodo sui filtri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione del clock del grafico](setting-the-graph-clock.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



