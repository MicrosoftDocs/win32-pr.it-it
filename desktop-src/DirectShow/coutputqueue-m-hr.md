---
description: Valore HRESULT che indica se l'oggetto accetterà esempi. Se il valore è \_ OK, l'oggetto accetterà esempi. In caso contrario, rifiuta gli esempi.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327342"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="63ca1-105">Membro HR COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="63ca1-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="63ca1-106">Valore **HRESULT** che indica se l'oggetto accetterà esempi.</span><span class="sxs-lookup"><span data-stu-id="63ca1-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="63ca1-107">Se il valore è \_ OK, l'oggetto accetterà esempi.</span><span class="sxs-lookup"><span data-stu-id="63ca1-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="63ca1-108">In caso contrario, rifiuta gli esempi.</span><span class="sxs-lookup"><span data-stu-id="63ca1-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ca1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63ca1-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="63ca1-110">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="63ca1-110">Remarks</span></span>

<span data-ttu-id="63ca1-111">Questa variabile membro viene utilizzata per coordinare le attività tra thread.</span><span class="sxs-lookup"><span data-stu-id="63ca1-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="63ca1-112">Se il pin di input downstream rifiuta un campione o se l'oggetto inizia lo scaricamento, il valore viene impostato su S \_ false o su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="63ca1-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="63ca1-113">L'oggetto non fornirà altri esempi fino al completamento dello scaricamento oppure fino a quando non viene chiamato il metodo [**COutputQueue:: Reset**](coutputqueue-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="63ca1-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ca1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63ca1-114">Requirements</span></span>



| <span data-ttu-id="63ca1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ca1-115">Requirement</span></span> | <span data-ttu-id="63ca1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="63ca1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ca1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63ca1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="63ca1-118"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63ca1-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63ca1-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="63ca1-119">Library</span></span><br/> | <dl> <span data-ttu-id="63ca1-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63ca1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ca1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63ca1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ca1-122">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="63ca1-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




