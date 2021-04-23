---
description: Orologio di riferimento del sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Orologio di riferimento del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909489"
---
# <a name="system-reference-clock"></a>Orologio di riferimento del sistema

L'oggetto System Reference Clock implementa un clock di riferimento che restituisce l'ora di sistema. Se nessuno dei filtri nel grafico fornisce un orologio di riferimento, il gestore del grafico dei filtri usa questo componente per sincronizzare il grafico. Creare questo oggetto chiamando **CoCreateInstance.**



| Label | Valore |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificatore di classe | CLSID \_ SystemClock                                                                                                                                       |
| Interfacce       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Objects](directshow-objects.md)
</dt> <dt>

[Orologi di riferimento](reference-clocks.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



