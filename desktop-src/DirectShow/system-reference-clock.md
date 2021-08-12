---
description: Clock di riferimento di sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Clock di riferimento di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651841"
---
# <a name="system-reference-clock"></a>Clock di riferimento di sistema

L'oggetto System Reference Clock implementa un clock di riferimento che restituisce l'ora di sistema. Se nessuno dei filtri nel grafico fornisce un orologio di riferimento, il gestore del grafico dei filtri usa questo componente per sincronizzare il grafico. Creare questo oggetto chiamando **CoCreateInstance**.



| Etichetta | Valore |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificatore di classe | CLSID \_ SystemClock                                                                                                                                       |
| Interfacce       | [**IAMClockAdjust,**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) [**IReferenceClock,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Oggetti](directshow-objects.md)
</dt> <dt>

[Clock di riferimento](reference-clocks.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



