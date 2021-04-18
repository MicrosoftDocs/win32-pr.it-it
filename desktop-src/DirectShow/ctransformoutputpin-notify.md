---
description: 'Il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Metodo CTransformOutputPin. Notify (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330840"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="0748c-104">Metodo CTransformOutputPin. Notify</span><span class="sxs-lookup"><span data-stu-id="0748c-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="0748c-105">Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="0748c-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="0748c-106">Questo metodo implementa il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="0748c-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0748c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0748c-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="0748c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0748c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0748c-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="0748c-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="0748c-110">Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro che ha recapitato il messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="0748c-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="0748c-111">*d*</span><span class="sxs-lookup"><span data-stu-id="0748c-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="0748c-112">Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="0748c-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0748c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0748c-113">Return value</span></span>

<span data-ttu-id="0748c-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0748c-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0748c-115">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0748c-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0748c-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0748c-116">Return code</span></span>                                                                                       | <span data-ttu-id="0748c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0748c-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="0748c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0748c-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="0748c-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0748c-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="0748c-120"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="0748c-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="0748c-121">Impossibile trovare un oggetto per accettare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="0748c-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0748c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0748c-122">Remarks</span></span>

<span data-ttu-id="0748c-123">Questo metodo chiama il metodo [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) del filtro.</span><span class="sxs-lookup"><span data-stu-id="0748c-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="0748c-124">Se il filtro non gestisce il messaggio di qualità, questo metodo chiama il metodo [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) sul pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="0748c-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="0748c-125">Il metodo **PassNotify** passa il messaggio di qualità upstream (o a un gestore di qualità personalizzato, se ne è stato installato uno).</span><span class="sxs-lookup"><span data-stu-id="0748c-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="0748c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0748c-126">Requirements</span></span>



| <span data-ttu-id="0748c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0748c-127">Requirement</span></span> | <span data-ttu-id="0748c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0748c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0748c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0748c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0748c-130"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0748c-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0748c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0748c-131">Library</span></span><br/> | <dl> <span data-ttu-id="0748c-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0748c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




