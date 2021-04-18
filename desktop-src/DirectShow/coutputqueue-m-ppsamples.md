---
description: 'Matrice di campioni di dimensioni COutputQueue:: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membro COutputQueue:: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329523"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="7f8dd-103">Membro ppSamples di COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="7f8dd-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="7f8dd-104">Matrice di campioni di dimensioni [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="7f8dd-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f8dd-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="7f8dd-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7f8dd-106">Remarks</span></span>

<span data-ttu-id="7f8dd-107">Il thread di lavoro estrae gli esempi dalla coda e li inserisce in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="7f8dd-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="7f8dd-108">Passa la matrice al metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="7f8dd-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="7f8dd-109">Se l'oggetto non utilizza un thread di lavoro, l'oggetto inserisce esempi direttamente in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="7f8dd-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="7f8dd-110">La variabile membro dell' [**\_ elenco COutputQueue:: m**](coutputqueue-m-list.md) include la coda.</span><span class="sxs-lookup"><span data-stu-id="7f8dd-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8dd-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f8dd-111">Requirements</span></span>



| <span data-ttu-id="7f8dd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f8dd-112">Requirement</span></span> | <span data-ttu-id="7f8dd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8dd-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8dd-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f8dd-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7f8dd-115"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f8dd-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f8dd-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f8dd-116">Library</span></span><br/> | <dl> <span data-ttu-id="7f8dd-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f8dd-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8dd-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f8dd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8dd-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="7f8dd-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




