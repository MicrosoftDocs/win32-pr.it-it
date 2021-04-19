---
description: Il \_ tipo di dati time di riferimento definisce le unità per i tempi di riferimento in DirectShow. Ogni unità di tempo di riferimento è di 100 nanosecondi.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332182"
---
# <a name="reference_time"></a><span data-ttu-id="f05d9-104">\_ora riferimento</span><span class="sxs-lookup"><span data-stu-id="f05d9-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="f05d9-105">Il tipo di dati **\_ time di riferimento** definisce le unità per i tempi di riferimento in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f05d9-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="f05d9-106">Ogni unità di tempo di riferimento è di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f05d9-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="f05d9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f05d9-107">Remarks</span></span>

<span data-ttu-id="f05d9-108">Il tipo di dati **\_ time di riferimento** è un Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f05d9-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="f05d9-109">I tempi di riferimento vengono in genere misurati in base a una delle linee di base seguenti:</span><span class="sxs-lookup"><span data-stu-id="f05d9-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="f05d9-110">Tempo di clock assoluto.</span><span class="sxs-lookup"><span data-stu-id="f05d9-110">An absolute clock time.</span></span> <span data-ttu-id="f05d9-111">In questo caso, la linea di base dipenderà dall'implementazione del clock.</span><span class="sxs-lookup"><span data-stu-id="f05d9-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="f05d9-112">Per altre informazioni, vedere [clock di riferimento](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="f05d9-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="f05d9-113">Relativo all'inizio della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f05d9-113">Relative to the start of playback.</span></span>

<span data-ttu-id="f05d9-114">Per altre informazioni sui tempi di riferimento, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="f05d9-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f05d9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f05d9-115">Requirements</span></span>



| <span data-ttu-id="f05d9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05d9-116">Requirement</span></span> | <span data-ttu-id="f05d9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f05d9-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f05d9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f05d9-118">Header</span></span><br/> | <dl> <span data-ttu-id="f05d9-119"><dt>Strmif. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f05d9-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05d9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f05d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05d9-121">Tipi di dati DirectShow</span><span class="sxs-lookup"><span data-stu-id="f05d9-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




