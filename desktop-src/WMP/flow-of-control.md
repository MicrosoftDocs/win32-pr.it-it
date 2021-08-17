---
title: Flow di controllo
description: Flow di controllo
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualizzazioni, flusso di programma
- visualizzazioni personalizzate, flusso di programma
- visualizzazioni, flusso di controllo
- visualizzazioni personalizzate, flusso di controllo
- visualizzazioni, eventi temporizzazione
- visualizzazioni personalizzate, eventi temporizzazione
- visualizzazioni,funzione Render
- visualizzazioni personalizzate,funzione Render
- visualizzazioni,funzione RenderWindow
- visualizzazioni personalizzate,funzione RenderWindow
- Funzione di rendering, flusso del programma di visualizzazione
- Funzione RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332d9c907e7c25f81d01bc8adf48c6d4d91a7b17763a1b0daf0007a8534ac4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934740"
---
# <a name="flow-of-control"></a>Flow di controllo

I dati audio vengono Windows Media Player in modo continuo tramite un file o un flusso. I dati vengono passati alla visualizzazione. Si disegna su una superficie definita e la si passa nuovamente Windows Media Player. Questo interscambio si verifica più volte al secondo e per l'utente il risultato è un'animazione piacevole che passa nel tempo alla musica.

Ecco la sequenza specifica del flusso del programma di visualizzazione:

1.  A un intervallo temporale, Windows Media Player snapshot dell'audio in riproduzione.
2.  Windows Media Player fornisce i dati da tale snapshot alla visualizzazione tramite la **funzione Render** e la **funzione RenderWindowed.**
3.  È necessario scrivere codice che verrà eseguito quando **vengono chiamati Render** **e RenderWindowed.** Il codice viene creato usando un contesto di dispositivo definito da Windows Media Player rendering senza finestra o usando una finestra creata durante il rendering con finestra.
4.  In un'area specificata dall'interfaccia utente corrente Windows Media Player il codice disegnato.
5.  Questo processo si ripete più volte al secondo, creando animazioni grafiche che vengono temporizzazione per la musica. Quando la riproduzione della musica viene interrotta, la visualizzazione viene arrestata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori**](developer-overview.md)
</dt> </dl>

 

 




