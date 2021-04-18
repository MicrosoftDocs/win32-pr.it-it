---
description: Clock di riferimento di sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Clock di riferimento di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315526"
---
# <a name="system-reference-clock"></a>Clock di riferimento di sistema

L'oggetto clock di riferimento di sistema implementa un orologio di riferimento che restituisce l'ora di sistema. Se nessuno dei filtri nel grafico fornisce un clock di riferimento, il componente di gestione del filtro viene utilizzato per sincronizzare il grafo. Creare questo oggetto chiamando **CoCreateInstance**.



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificatore di classe | \_SYSTEMCLOCK CLSID                                                                                                                                       |
| Interfacce       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti DirectShow](directshow-objects.md)
</dt> <dt>

[Orologi di riferimento](reference-clocks.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



