---
description: La ricerca
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: La ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104552430"
---
# <a name="seeking"></a>La ricerca

I filtri supportano la ricerca tramite l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . L'applicazione esegue una query su Filter Graph Manager per **IMediaSeeking** e la usa per emettere comandi Seek. Filter Graph Manager distribuisce ogni comando seek a tutti i filtri renderer presenti nel grafico. Ogni renderer passa il comando upstream, tramite i pin di output dei filtri upstream, fino a raggiungere un filtro in grado di eseguire la ricerca. In genere un filtro di origine o un filtro del parser, ad esempio il [separatore AVI](avi-splitter-filter.md), esegue l'operazione di ricerca.

Quando un filtro esegue un'operazione di ricerca, Scarica tutti i dati in sospeso. Il risultato è ridurre al minimo la latenza dei comandi Seek, perché i dati esistenti vengono scaricati dal grafico. Dopo un comando seek, il flusso dell'ora viene reimpostato su zero.

Nel diagramma seguente viene illustrata la sequenza di eventi.

![sequenza di eventi](images/seeking.png)

Se un filtro del parser ha più di un pin di output, in genere designa uno di essi per accettare i comandi Seek. Gli altri pin rifiutano o ignorano i comandi di ricerca ricevuti. In questo modo, il parser mantiene tutti i flussi sincronizzati. Tuttavia, tutti i pin di output devono implementare [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) e [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) per restituire le funzionalità di ricerca del filtro. In questo modo, il gestore del grafico del filtro restituisce il valore corretto per l'applicazione.

L'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) è stata deprecata per i filtri. I client di automazione devono ancora usare questa interfaccia nel gestore del grafo dei filtri, perché **IMediaSeeking** non è compatibile con l'automazione, ma il gestore del grafo del filtro converte tutte le chiamate **IMediaPosition** in chiamate **IMediaSeeking** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flushing](flushing.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



