---
title: Risoluzione del timer
description: Risoluzione del timer
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- timer multimediali, risoluzione
- timer, risoluzione
- risoluzione minima del timer
- risoluzione del timer massima
- timer multimediali, risoluzione massima
- timer, risoluzione massima
- timer multimediali, risoluzione minima
- timer, risoluzione minima
- timeGetDevCaps (funzione)
- timeBeginPeriod (funzione)
- timeEndPeriod (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/28/2019
ms.locfileid: "103706991"
---
# <a name="timer-resolution"></a>Risoluzione del timer

Per determinare le risoluzioni del timer minime e massime supportate dai servizi timer, utilizzare la funzione [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) . Questa funzione compila i membri **wPeriodMin** e **WPeriodMax** della struttura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con le risoluzioni minime e massime. Questo intervallo può variare tra computer e piattaforme Windows.

Dopo aver determinato le risoluzioni timer minime e massime disponibili, è necessario stabilire la risoluzione minima che si desidera venga utilizzata dall'applicazione. Usare le funzioni [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) per impostare e cancellare questa risoluzione. È necessario associare ogni chiamata a **timeBeginPeriod** con una chiamata a **timeEndPeriod**, specificando la stessa risoluzione minima in entrambe le chiamate. Un'applicazione può effettuare più chiamate **timeBeginPeriod** , purché ogni chiamata corrisponda a una chiamata a **timeEndPeriod**.

In [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**TimeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)il parametro *uPeriod* indica la risoluzione minima del timer, in millisecondi. È possibile specificare qualsiasi valore di risoluzione del timer compreso nell'intervallo supportato dal timer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui timer multimediali](about-multimedia-timers.md)
</dt> </dl>

 

 




