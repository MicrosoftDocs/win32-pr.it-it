---
description: Ore di clock
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Ore di clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401101"
---
# <a name="clock-times"></a>Ore di clock

DirectShow definisce due ore di clock correlate: ora di riferimento e tempo di flusso.

-   L' *ora di riferimento* è il tempo assoluto restituito dall'orologio di riferimento. Vedere [clock di riferimento](reference-clocks.md).
-   Il *tempo di flusso* viene definito rispetto al momento in cui è stata avviata l'ultima esecuzione del grafico.
    -   Mentre il grafico è in esecuzione, l'ora del flusso è uguale all'ora di riferimento meno l'ora di inizio.
    -   Quando il grafico è sospeso, il tempo di flusso rimane in corrispondenza dell'ora del flusso in cui è stato sospeso.
    -   Dopo un'operazione di ricerca, l'ora del flusso viene reimpostata su zero.
    -   Quando il grafico viene arrestato, il tempo di flusso non è definito.

Quando un esempio di supporto presenta un timestamp *t*, significa che è necessario eseguire il rendering dell'esempio in corrispondenza del tempo di flusso *t*. Per questo motivo, il tempo di flusso viene definito anche *tempo di presentazione*.

Quando un'applicazione chiama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico dei filtri, il gestore del grafo del filtro chiama [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) in ogni filtro. Per compensare la lieve quantità di tempo necessaria per l'avvio dell'esecuzione dei filtri, il gestore del grafico del filtro specifica un'ora di inizio leggermente in futuro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Timestamp](time-stamps.md)
</dt> </dl>

 

 



