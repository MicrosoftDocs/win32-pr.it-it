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
# <a name="system-reference-clock"></a><span data-ttu-id="79d12-103">Orologio di riferimento del sistema</span><span class="sxs-lookup"><span data-stu-id="79d12-103">System Reference Clock</span></span>

<span data-ttu-id="79d12-104">L'oggetto System Reference Clock implementa un clock di riferimento che restituisce l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="79d12-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="79d12-105">Se nessuno dei filtri nel grafico fornisce un orologio di riferimento, il gestore del grafico dei filtri usa questo componente per sincronizzare il grafico.</span><span class="sxs-lookup"><span data-stu-id="79d12-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="79d12-106">Creare questo oggetto chiamando **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="79d12-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="79d12-107">Label</span><span class="sxs-lookup"><span data-stu-id="79d12-107">Label</span></span> | <span data-ttu-id="79d12-108">Valore</span><span class="sxs-lookup"><span data-stu-id="79d12-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d12-109">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="79d12-109">Class Identifier</span></span> | <span data-ttu-id="79d12-110">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="79d12-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="79d12-111">Interfacce</span><span class="sxs-lookup"><span data-stu-id="79d12-111">Interfaces</span></span>       | <span data-ttu-id="79d12-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="79d12-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="79d12-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79d12-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d12-114">DirectShow Objects</span><span class="sxs-lookup"><span data-stu-id="79d12-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="79d12-115">Orologi di riferimento</span><span class="sxs-lookup"><span data-stu-id="79d12-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="79d12-116">Ora e orologi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="79d12-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



