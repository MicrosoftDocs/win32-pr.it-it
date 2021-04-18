---
description: Flag che specifica se l'oggetto recapita esempi in batch esatti.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membro COutputQueue:: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330856"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="7a93f-103">Membro bBatchExact di COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="7a93f-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="7a93f-104">Flag che specifica se l'oggetto recapita esempi in batch esatti.</span><span class="sxs-lookup"><span data-stu-id="7a93f-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a93f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a93f-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="7a93f-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7a93f-106">Remarks</span></span>

<span data-ttu-id="7a93f-107">Se il valore è **true**, l'oggetto attende fino a quando non dispone di un batch completo di esempi di supporti prima di recapito.</span><span class="sxs-lookup"><span data-stu-id="7a93f-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="7a93f-108">In caso contrario, recapita gli esempi Man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="7a93f-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="7a93f-109">La variabile membro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) definisce le dimensioni del batch.</span><span class="sxs-lookup"><span data-stu-id="7a93f-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a93f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a93f-110">Requirements</span></span>



| <span data-ttu-id="7a93f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a93f-111">Requirement</span></span> | <span data-ttu-id="7a93f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7a93f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a93f-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a93f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7a93f-114"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a93f-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a93f-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a93f-115">Library</span></span><br/> | <dl> <span data-ttu-id="7a93f-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a93f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a93f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a93f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a93f-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="7a93f-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




