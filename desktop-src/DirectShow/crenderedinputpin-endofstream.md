---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene emesso un nuovo comando Run nel filtro. Questo metodo implementa il metodo IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Metodo CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329365"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="201f2-104">CRenderedInputPin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="201f2-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="201f2-105">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi, fino a quando non viene emesso un nuovo comando Run nel filtro.</span><span class="sxs-lookup"><span data-stu-id="201f2-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="201f2-106">Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="201f2-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="201f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="201f2-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="201f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="201f2-108">Parameters</span></span>

<span data-ttu-id="201f2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="201f2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="201f2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="201f2-110">Return value</span></span>

<span data-ttu-id="201f2-111">Restituisce \_ OK se l'esito è positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="201f2-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="201f2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="201f2-112">Remarks</span></span>

<span data-ttu-id="201f2-113">Se il filtro è in esecuzione, questo metodo invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="201f2-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="201f2-114">In caso contrario, viene impostato un flag in modo che l' \_ evento di completamento EC venga inviato al successivo esecuzione del filtro.</span><span class="sxs-lookup"><span data-stu-id="201f2-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="201f2-115">Lo svuotamento del filtro Cancella il flag.</span><span class="sxs-lookup"><span data-stu-id="201f2-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="201f2-116">È necessario eseguire l'override di questo metodo per mantenere il blocco di streaming del PIN:</span><span class="sxs-lookup"><span data-stu-id="201f2-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="201f2-117">Se, inoltre, il filtro elabora **le chiamate in** modo asincrono, il PIN deve attendere l'invio dell'evento di completamento EC fino a \_ quando il filtro non ha elaborato tutti gli esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="201f2-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="201f2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="201f2-118">Requirements</span></span>



| <span data-ttu-id="201f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="201f2-119">Requirement</span></span> | <span data-ttu-id="201f2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="201f2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="201f2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="201f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="201f2-122"><dt>Amextra. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="201f2-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="201f2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="201f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="201f2-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="201f2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="201f2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="201f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201f2-126">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="201f2-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




