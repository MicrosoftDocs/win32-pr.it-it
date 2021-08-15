---
description: Orario di clock
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Orario di clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0075dc2d8c2273c8ade612244f0f7d551996756e55000043ffe3bc952227fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402071"
---
# <a name="clock-times"></a>Orario di clock

DirectShow definisce due ore di clock correlate: l'ora di riferimento e l'ora del flusso.

-   *L'ora di* riferimento è l'ora assoluta restituita dal clock di riferimento. Vedere [Clock di riferimento.](reference-clocks.md)
-   *L'ora di* flusso è definita in relazione all'ultima esecuzione del grafo.
    -   Mentre il grafico è in esecuzione, l'ora del flusso è uguale all'ora di riferimento meno l'ora di inizio.
    -   Mentre il grafico è in pausa, il tempo di flusso rimane al momento della sospensione del flusso.
    -   Dopo un'operazione di ricerca, l'ora del flusso viene reimpostata su zero.
    -   Mentre il grafico viene arrestato, il tempo di flusso non è definito.

Quando un campione multimediale ha un timestamp *t*, significa che il rendering dell'esempio deve essere eseguito all'ora del *flusso t*. Per questo motivo, l'ora del flusso è detta anche *ora di presentazione.*

Quando un'applicazione chiama [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico dei filtri, Filter Graph Manager chiama [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) su ogni filtro. Per compensare la minima quantità di tempo necessario per l'avvio dell'esecuzione dei filtri, Filter Graph Manager specifica un'ora di inizio leggermente futura.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Timestamp](time-stamps.md)
</dt> </dl>

 

 



