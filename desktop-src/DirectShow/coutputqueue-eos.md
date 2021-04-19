---
description: Il metodo EOS recapita una chiamata di fine flusso al pin di input.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Metodo COutputQueue. EOS (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330208"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="8e934-103">Metodo COutputQueue. EOS</span><span class="sxs-lookup"><span data-stu-id="8e934-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="8e934-104">Il `EOS` Metodo recapita una chiamata di fine flusso al pin di input.</span><span class="sxs-lookup"><span data-stu-id="8e934-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e934-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e934-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="8e934-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e934-106">Parameters</span></span>

<span data-ttu-id="8e934-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e934-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e934-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e934-108">Return value</span></span>

<span data-ttu-id="8e934-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8e934-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e934-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e934-110">Remarks</span></span>

<span data-ttu-id="8e934-111">Se l'oggetto usa un thread, Accoda un \_ messaggio di controllo pacchetti EOS.</span><span class="sxs-lookup"><span data-stu-id="8e934-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="8e934-112">Il thread recapita tutti gli esempi in sospeso e chiama il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="8e934-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="8e934-113">Se l'oggetto non utilizza un thread, viene chiamato il metodo [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8e934-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="8e934-114">Chiama quindi **Ipin:: EndOfStream** sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="8e934-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e934-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e934-115">Requirements</span></span>



| <span data-ttu-id="8e934-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e934-116">Requirement</span></span> | <span data-ttu-id="8e934-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8e934-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e934-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e934-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8e934-119"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e934-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e934-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e934-120">Library</span></span><br/> | <dl> <span data-ttu-id="8e934-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e934-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e934-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e934-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e934-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="8e934-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




