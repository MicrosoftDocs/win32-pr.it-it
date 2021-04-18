---
description: Il metodo ChangeRate viene chiamato quando cambia la velocità di riproduzione.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Metodo CSourceSeeking. ChangeRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325925"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="cb2d0-103">CSourceSeeking. ChangeRate (metodo)</span><span class="sxs-lookup"><span data-stu-id="cb2d0-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="cb2d0-104">Il `ChangeRate` metodo viene chiamato quando viene modificata la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb2d0-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="cb2d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb2d0-106">Parameters</span></span>

<span data-ttu-id="cb2d0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb2d0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb2d0-108">Return value</span></span>

<span data-ttu-id="cb2d0-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb2d0-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb2d0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb2d0-110">Remarks</span></span>

<span data-ttu-id="cb2d0-111">Il metodo [**CSourceSeeking::**](csourceseeking-setrate.md) SetValue chiama questo metodo, che deve essere implementato dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="cb2d0-112">Il metodo **serate** aggiorna la variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , ma non convalida il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="cb2d0-113">Una frequenza pari a zero deve essere sempre rifiutata.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="cb2d0-114">La velocità inferiore a zero indica una riproduzione negativa.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="cb2d0-115">La maggior parte dei filtri non supporta frequenze negative.</span><span class="sxs-lookup"><span data-stu-id="cb2d0-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="cb2d0-116">Nell'esempio seguente viene illustrata una possibile implementazione:</span><span class="sxs-lookup"><span data-stu-id="cb2d0-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="cb2d0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb2d0-117">Requirements</span></span>



| <span data-ttu-id="cb2d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb2d0-118">Requirement</span></span> | <span data-ttu-id="cb2d0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cb2d0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2d0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb2d0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cb2d0-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb2d0-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb2d0-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb2d0-122">Library</span></span><br/> | <dl> <span data-ttu-id="cb2d0-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb2d0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2d0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb2d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2d0-125">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="cb2d0-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




