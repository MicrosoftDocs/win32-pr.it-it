---
description: riercare
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: riercare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e087ce981d6548dfeef7ac8d3cb7bc17a69ff952ce95646cd896ace30af941
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951926"
---
# <a name="seeking"></a>riercare

I filtri supportano la ricerca [**tramite l'interfaccia IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) L'applicazione esegue una query su Filter Graph Manager per **IMediaSeeking** e lo usa per eseguire i comandi di ricerca. Gestione Graph distribuisce ogni comando di ricerca a tutti i filtri renderer nel grafico. Ogni renderer passa il comando a monte, attraverso i pin di output dei filtri upstream, fino a raggiungere un filtro in grado di eseguire la ricerca. In genere, un filtro di origine o un filtro parser, ad esempio la barra di divisione [AVI,](avi-splitter-filter.md)esegue l'operazione di ricerca.

Quando un filtro esegue un'operazione di ricerca, scarica tutti i dati in sospeso. Il risultato è ridurre al minimo la latenza dei comandi di ricerca, perché i dati esistenti vengono scaricati dal grafico. Dopo un comando di ricerca, l'ora del flusso viene reimpostata su zero.

Il diagramma seguente illustra la sequenza di eventi.

![sequenza di eventi](images/seeking.png)

Se un filtro del parser ha più di un pin di output, in genere ne designa uno per accettare i comandi di ricerca. Gli altri pin rifiutano o ignorano i comandi di ricerca ricevuti. In questo modo, il parser mantiene sincronizzati tutti i flussi. Tuttavia, tutti i pin di output devono [**implementare IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) e [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) per restituire le funzionalità di ricerca del filtro. In questo modo si garantisce che Graph Manager restituisca il valore corretto all'applicazione.

[**L'interfaccia IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) è stata deprecata per i filtri. I client di automazione devono comunque usare questa interfaccia in Filter Graph Manager, perché **IMediaSeeking** non è compatibile con Automazione, ma Filter Graph Manager converte tutte le chiamate **IMediaPosition** in **chiamate IMediaSeeking.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flushing](flushing.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



