---
description: "Evento facoltativo che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda. Il valore è inizialmente NULL. Chiamare il metodo COutputQueue:: SetPopEvent per specificare un handle di evento."
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membro COutputQueue:: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327343"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="dc4bb-105">Membro hEventPop di COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="dc4bb-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="dc4bb-106">Evento facoltativo che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="dc4bb-107">Il valore è inizialmente **null**.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-107">The value is initially **NULL**.</span></span> <span data-ttu-id="dc4bb-108">Chiamare il metodo [**COutputQueue:: SetPopEvent**](coutputqueue-setpopevent.md) per specificare un handle di evento.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4bb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc4bb-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="dc4bb-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc4bb-110">Requirements</span></span>



| <span data-ttu-id="dc4bb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc4bb-111">Requirement</span></span> | <span data-ttu-id="dc4bb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="dc4bb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4bb-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc4bb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dc4bb-114"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc4bb-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc4bb-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="dc4bb-115">Library</span></span><br/> | <dl> <span data-ttu-id="dc4bb-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dc4bb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4bb-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc4bb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4bb-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="dc4bb-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




