---
description: Il metodo DynamicReconnect esegue una riconnessione dinamica con un nuovo tipo di supporto. La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Metodo CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324183"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="c987f-104">CDynamicOutputPin. DynamicReconnect, metodo</span><span class="sxs-lookup"><span data-stu-id="c987f-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="c987f-105">Il `DynamicReconnect` metodo esegue una riconnessione dinamica con un nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c987f-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="c987f-106">La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c987f-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="c987f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c987f-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="c987f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c987f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c987f-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="c987f-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c987f-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c987f-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c987f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c987f-111">Return value</span></span>

<span data-ttu-id="c987f-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c987f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c987f-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c987f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c987f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c987f-114">Return code</span></span>                                                                            | <span data-ttu-id="c987f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c987f-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c987f-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c987f-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c987f-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c987f-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="c987f-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="c987f-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c987f-119">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c987f-119">Failure.</span></span> <span data-ttu-id="c987f-120">Probabilmente il filtro proprietario non ha chiamato il metodo [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c987f-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c987f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c987f-121">Remarks</span></span>

<span data-ttu-id="c987f-122">Questo metodo deve essere chiamato dallo stesso thread che recapita i dati al pin.</span><span class="sxs-lookup"><span data-stu-id="c987f-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="c987f-123">Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c987f-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="c987f-124">Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c987f-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="c987f-125">Chiamare [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c987f-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c987f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c987f-126">Requirements</span></span>



| <span data-ttu-id="c987f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c987f-127">Requirement</span></span> | <span data-ttu-id="c987f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c987f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c987f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c987f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c987f-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c987f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c987f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="c987f-131">Library</span></span><br/> | <dl> <span data-ttu-id="c987f-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c987f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c987f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c987f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c987f-134">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c987f-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




