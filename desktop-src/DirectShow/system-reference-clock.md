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
# <a name="system-reference-clock"></a><span data-ttu-id="4c387-103">Clock di riferimento di sistema</span><span class="sxs-lookup"><span data-stu-id="4c387-103">System Reference Clock</span></span>

<span data-ttu-id="4c387-104">L'oggetto clock di riferimento di sistema implementa un orologio di riferimento che restituisce l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="4c387-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="4c387-105">Se nessuno dei filtri nel grafico fornisce un clock di riferimento, il componente di gestione del filtro viene utilizzato per sincronizzare il grafo.</span><span class="sxs-lookup"><span data-stu-id="4c387-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="4c387-106">Creare questo oggetto chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4c387-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c387-107">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="4c387-107">Class Identifier</span></span> | <span data-ttu-id="4c387-108">\_SYSTEMCLOCK CLSID</span><span class="sxs-lookup"><span data-stu-id="4c387-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="4c387-109">Interfacce</span><span class="sxs-lookup"><span data-stu-id="4c387-109">Interfaces</span></span>       | <span data-ttu-id="4c387-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="4c387-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4c387-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c387-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c387-112">Oggetti DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c387-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="4c387-113">Orologi di riferimento</span><span class="sxs-lookup"><span data-stu-id="4c387-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="4c387-114">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c387-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



