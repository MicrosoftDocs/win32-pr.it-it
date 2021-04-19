---
description: 'Il metodo ReceiveCanBlock determina se le chiamate al metodo IMemInputPin:: Receive potrebbero bloccarsi. Questo metodo implementa il metodo IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Metodo CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333214"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="8e691-104">CBaseInputPin. ReceiveCanBlock, metodo</span><span class="sxs-lookup"><span data-stu-id="8e691-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="8e691-105">Il `ReceiveCanBlock` metodo determina se le chiamate al metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) potrebbero bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="8e691-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="8e691-106">Questo metodo implementa il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .</span><span class="sxs-lookup"><span data-stu-id="8e691-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e691-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e691-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="8e691-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e691-108">Parameters</span></span>

<span data-ttu-id="8e691-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e691-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e691-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e691-110">Return value</span></span>

<span data-ttu-id="8e691-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e691-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8e691-112">Il valore possibile include quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8e691-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="8e691-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8e691-113">Return code</span></span>                                                                             | <span data-ttu-id="8e691-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e691-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="8e691-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8e691-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="8e691-116">Il PIN non si bloccherà in una chiamata a **Receive**.</span><span class="sxs-lookup"><span data-stu-id="8e691-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="8e691-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e691-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="8e691-118">Il PIN potrebbe bloccarsi in una chiamata a **Receive**.</span><span class="sxs-lookup"><span data-stu-id="8e691-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8e691-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e691-119">Remarks</span></span>

<span data-ttu-id="8e691-120">Restituisce \_ false se è garantita la mancata blocco delle chiamate al metodo **Receive** .</span><span class="sxs-lookup"><span data-stu-id="8e691-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="8e691-121">In caso contrario, restituire S \_ OK o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="8e691-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="8e691-122">Se il metodo **Receive** chiama **Receive** su un pin downstream, il pin downstream potrebbe bloccarsi; `ReceiveCanBlock` è necessario tenere conto di questo fattore.</span><span class="sxs-lookup"><span data-stu-id="8e691-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="8e691-123">Un filtro upstream può utilizzare questo metodo per determinare la strategia di Threading.</span><span class="sxs-lookup"><span data-stu-id="8e691-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="8e691-124">Se il metodo **Receive** potrebbe bloccarsi, il filtro upstream potrebbe decidere di usare un thread di lavoro che memorizza nel buffer i dati.</span><span class="sxs-lookup"><span data-stu-id="8e691-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="8e691-125">Per un'implementazione di questa strategia, vedere la classe [**COutputQueue**](coutputqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="8e691-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="8e691-126">Nella classe di base, questo metodo restituisce S \_ OK quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e691-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="8e691-127">Il filtro non ha pin di output.</span><span class="sxs-lookup"><span data-stu-id="8e691-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="8e691-128">Un pin di input connesso a questo filtro segnala che potrebbe bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="8e691-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="8e691-129">Un pin di input connesso a questo filtro non supporta l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="8e691-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e691-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e691-130">Requirements</span></span>



| <span data-ttu-id="8e691-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e691-131">Requirement</span></span> | <span data-ttu-id="8e691-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8e691-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e691-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e691-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8e691-134"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e691-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e691-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e691-135">Library</span></span><br/> | <dl> <span data-ttu-id="8e691-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e691-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e691-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e691-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e691-138">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="8e691-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




