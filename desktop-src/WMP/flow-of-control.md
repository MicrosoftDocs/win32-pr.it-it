---
title: Flusso di controllo
description: Flusso di controllo
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- Visualizzazioni, flusso di programma
- Visualizzazioni personalizzate, flusso di programma
- Visualizzazioni, flusso di controllo
- Visualizzazioni personalizzate, flusso di controllo
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Visualizzazioni, funzione RenderWindow
- Visualizzazioni personalizzate, funzione RenderWindow
- Funzione render, flusso del programma di visualizzazione
- RenderWindow (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955230"
---
# <a name="flow-of-control"></a>Flusso di controllo

I dati audio entrano in Windows Media Player continuamente tramite un file o un flusso. I dati vengono passati alla visualizzazione. Viene disegnato su una superficie definita e viene ripassata la superficie a Windows Media Player. Questo interscambio si verifica più volte al secondo e, per l'utente, il risultato è un'animazione piacevole che si sposta nel tempo per la musica.

Di seguito è illustrata la sequenza specifica del flusso del programma di visualizzazione:

1.  A un intervallo di tempo, Windows Media Player acquisisce uno snapshot dell'audio che sta eseguendo.
2.  Windows Media Player fornisce i dati dallo snapshot alla visualizzazione tramite la funzione **Render** e la funzione **RenderWindowed** .
3.  È necessario scrivere codice che verrà eseguito quando viene chiamato **il metodo Render** e **RenderWindowed** . Il codice viene disegnato usando un contesto di dispositivo definito da Windows Media Player quando viene eseguito il rendering senza finestra o usando una finestra creata durante il rendering con finestra.
4.  In un'area specificata dall'interfaccia corrente, Windows Media Player Visualizza il codice disegnato dall'utente.
5.  Questo processo si ripete più volte al secondo, creando animazioni grafiche temporizzate per la musica. Quando la musica smette di suonare, la visualizzazione viene arrestata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori**](developer-overview.md)
</dt> </dl>

 

 




