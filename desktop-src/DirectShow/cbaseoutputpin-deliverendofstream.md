---
description: Il metodo DeliverEndOfStream recapita una notifica di fine del flusso al pin di input connesso.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Metodo CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332066"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="41355-103">CBaseOutputPin. DeliverEndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="41355-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="41355-104">Il `DeliverEndOfStream` Metodo recapita una notifica di fine flusso al pin di input connesso.</span><span class="sxs-lookup"><span data-stu-id="41355-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="41355-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41355-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="41355-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41355-106">Parameters</span></span>

<span data-ttu-id="41355-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="41355-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41355-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41355-108">Return value</span></span>

<span data-ttu-id="41355-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41355-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="41355-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="41355-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="41355-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="41355-111">Return code</span></span>                                                                                           | <span data-ttu-id="41355-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41355-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="41355-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41355-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="41355-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="41355-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="41355-115"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="41355-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="41355-116">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="41355-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41355-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="41355-117">Remarks</span></span>

<span data-ttu-id="41355-118">Questo metodo chiama il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="41355-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="41355-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41355-119">Requirements</span></span>



| <span data-ttu-id="41355-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="41355-120">Requirement</span></span> | <span data-ttu-id="41355-121">Valore</span><span class="sxs-lookup"><span data-stu-id="41355-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41355-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41355-122">Header</span></span><br/>  | <dl> <span data-ttu-id="41355-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41355-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="41355-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="41355-124">Library</span></span><br/> | <dl> <span data-ttu-id="41355-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="41355-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41355-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41355-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41355-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="41355-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




