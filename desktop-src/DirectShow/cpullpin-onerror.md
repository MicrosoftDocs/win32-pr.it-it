---
description: Il metodo OnError viene chiamato se si verifica un errore durante il flusso. La classe derivata deve implementare questo metodo.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Metodo CPullPin. OnError (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331161"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="c335c-104">Metodo CPullPin. OnError</span><span class="sxs-lookup"><span data-stu-id="c335c-104">CPullPin.OnError method</span></span>

<span data-ttu-id="c335c-105">Il `OnError` metodo viene chiamato se si verifica un errore durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="c335c-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="c335c-106">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c335c-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c335c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c335c-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c335c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c335c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c335c-109">*h*</span><span class="sxs-lookup"><span data-stu-id="c335c-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="c335c-110">Specifica il valore **HRESULT** restituito dal metodo che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c335c-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c335c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c335c-111">Return value</span></span>

<span data-ttu-id="c335c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c335c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c335c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c335c-113">Remarks</span></span>

<span data-ttu-id="c335c-114">L'oggetto chiama questo metodo ogni volta che si verifica un errore che interrompe il thread di pull dei dati.</span><span class="sxs-lookup"><span data-stu-id="c335c-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="c335c-115">Il filtro può utilizzare questo metodo per recuperare gli errori di flusso normalmente.</span><span class="sxs-lookup"><span data-stu-id="c335c-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="c335c-116">Nella maggior parte dei casi, l'errore viene restituito dal filtro upstream, quindi il filtro upstream è responsabile della segnalazione a Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="c335c-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="c335c-117">Se l'errore si verifica all'interno del metodo [**CPullPin:: Receive**](cpullpin-receive.md) , il filtro deve inviare un evento [**\_ ERRORABORT EC**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="c335c-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="c335c-118">Vedere [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).</span><span class="sxs-lookup"><span data-stu-id="c335c-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="c335c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c335c-119">Requirements</span></span>



| <span data-ttu-id="c335c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c335c-120">Requirement</span></span> | <span data-ttu-id="c335c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c335c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c335c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c335c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c335c-123"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="c335c-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c335c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="c335c-124">Library</span></span><br/> | <dl> <span data-ttu-id="c335c-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c335c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c335c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c335c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c335c-127">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="c335c-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




