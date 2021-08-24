---
title: Risoluzione timer
description: Risoluzione timer
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- timer multimediali, risoluzione
- timer, risoluzione
- risoluzione minima del timer
- risoluzione massima del timer
- timer multimediali, risoluzione massima
- timer, risoluzione massima
- timer multimediali, risoluzione minima
- timer, risoluzione minima
- Funzione timeGetDevCaps
- Funzione timeBeginPeriod
- Funzione timeEndPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e81228acec27e41d43d41de7393ad64345acce25a450e91c815b1bbbf5164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781831"
---
# <a name="timer-resolution"></a>Risoluzione timer

Per determinare le risoluzioni minime e massime del timer supportate dai servizi timer, usare la [**funzione timeGetDevCaps.**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) Questa funzione riempie i **membri wPeriodMin** e **wPeriodMax** della struttura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con le risoluzioni minima e massima. Questo intervallo può variare tra computer e Windows piattaforme.

Dopo aver determinato le risoluzioni minime e massime disponibili del timer, è necessario stabilire la risoluzione minima da usare per l'applicazione. Usare le [**funzioni timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) [**e timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) per impostare e cancellare questa risoluzione. È necessario associare ogni chiamata a **timeBeginPeriod** con una chiamata a **timeEndPeriod**, specificando la stessa risoluzione minima in entrambe le chiamate. Un'applicazione può effettuare **più chiamate timeBeginPeriod,** purché ogni chiamata corrisponda a una chiamata a **timeEndPeriod**.

In [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)il *parametro uPeriod* indica la risoluzione minima del timer, in millisecondi. È possibile specificare qualsiasi valore di risoluzione del timer compreso nell'intervallo supportato dal timer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui timer multimediali](about-multimedia-timers.md)
</dt> </dl>

 

 




