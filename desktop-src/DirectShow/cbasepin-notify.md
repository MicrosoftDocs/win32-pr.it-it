---
description: 'Metodo CBasePin.Notify: il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl::Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Metodo CBasePin.Notify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096019"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="9ad53-104">Metodo CBasePin.Notify</span><span class="sxs-lookup"><span data-stu-id="9ad53-104">CBasePin.Notify method</span></span>

<span data-ttu-id="9ad53-105">Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="9ad53-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="9ad53-106">Questo metodo implementa il [**metodo IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="9ad53-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad53-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ad53-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="9ad53-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ad53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad53-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="9ad53-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="9ad53-110">Puntatore [**all'interfaccia IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro che ha recapitato il messaggio di controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="9ad53-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="9ad53-111">*D*</span><span class="sxs-lookup"><span data-stu-id="9ad53-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="9ad53-112">Specifica una struttura [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="9ad53-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad53-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ad53-113">Return value</span></span>

<span data-ttu-id="9ad53-114">La classe di base restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9ad53-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ad53-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ad53-115">Remarks</span></span>

<span data-ttu-id="9ad53-116">I pin di output devono eseguire l'override di questo metodo per accettare messaggi di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="9ad53-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="9ad53-117">Se è stato installato un gestore qualità esterno (vedere [**CBasePin::SetSink),**](cbasepin-setsink.md)passare il messaggio a tale responsabile qualità.</span><span class="sxs-lookup"><span data-stu-id="9ad53-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="9ad53-118">In caso contrario, il filtro deve gestire il messaggio stesso o passare il messaggio a monte.</span><span class="sxs-lookup"><span data-stu-id="9ad53-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="9ad53-119">Per altre informazioni, vedere [Quality-Control Management.](quality-control-management.md)</span><span class="sxs-lookup"><span data-stu-id="9ad53-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad53-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ad53-120">Requirements</span></span>



| <span data-ttu-id="9ad53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ad53-121">Requirement</span></span> | <span data-ttu-id="9ad53-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9ad53-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad53-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ad53-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9ad53-124"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad53-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ad53-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ad53-125">Library</span></span><br/> | <dl> <span data-ttu-id="9ad53-126"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad53-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad53-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ad53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad53-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="9ad53-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




