---
description: "Il metodo CBaseInputPin avvia un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: BeginFlush."
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Metodo CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327959"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="59726-104">CBaseInputPin. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="59726-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="59726-105">Il `CBaseInputPin` metodo inizia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="59726-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="59726-106">Questo metodo implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="59726-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59726-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59726-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="59726-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="59726-108">Parameters</span></span>

<span data-ttu-id="59726-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="59726-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59726-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59726-110">Return value</span></span>

<span data-ttu-id="59726-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59726-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="59726-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="59726-112">Remarks</span></span>

<span data-ttu-id="59726-113">Questo metodo imposta il flag [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) su **true**, che fa in modo che il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rifiuti altri esempi.</span><span class="sxs-lookup"><span data-stu-id="59726-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="59726-114">La classe derivata deve eseguire l'override di questo metodo ed eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="59726-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="59726-115">Chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sui pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="59726-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="59726-116">Se il PIN non ha ancora recapitato alcun campione multimediale a valle, è possibile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="59726-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="59726-117">Se i pin di output derivano dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) , è possibile chiamare il metodo [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="59726-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="59726-118">Chiamare il metodo della classe base.</span><span class="sxs-lookup"><span data-stu-id="59726-118">Call the base class method.</span></span>
3.  <span data-ttu-id="59726-119">Inizia l'eliminazione dei dati in coda.</span><span class="sxs-lookup"><span data-stu-id="59726-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="59726-120">Restituisce da qualsiasi chiamata bloccata al metodo **Receive** .</span><span class="sxs-lookup"><span data-stu-id="59726-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59726-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59726-121">Requirements</span></span>



| <span data-ttu-id="59726-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="59726-122">Requirement</span></span> | <span data-ttu-id="59726-123">Valore</span><span class="sxs-lookup"><span data-stu-id="59726-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59726-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59726-124">Header</span></span><br/>  | <dl> <span data-ttu-id="59726-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59726-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59726-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="59726-126">Library</span></span><br/> | <dl> <span data-ttu-id="59726-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59726-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59726-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59726-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59726-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="59726-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




