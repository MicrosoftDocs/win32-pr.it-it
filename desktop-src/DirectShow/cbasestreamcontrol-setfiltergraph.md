---
description: Il metodo SetFilterGraph specifica il sink di evento per gli eventi di controllo del flusso.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Metodo CBaseStreamControl. SetFilterGraph (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324038"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="1cdcc-103">CBaseStreamControl. SetFilterGraph, metodo</span><span class="sxs-lookup"><span data-stu-id="1cdcc-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="1cdcc-104">Il `SetFilterGraph` metodo specifica il sink di evento per gli eventi di controllo del flusso.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdcc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cdcc-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="1cdcc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cdcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cdcc-107">*pSink*</span><span class="sxs-lookup"><span data-stu-id="1cdcc-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="1cdcc-108">Puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) dell'oggetto Filter Graph Manager oppure **null** quando il filtro lascia il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cdcc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cdcc-109">Return value</span></span>

<span data-ttu-id="1cdcc-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cdcc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cdcc-111">Remarks</span></span>

<span data-ttu-id="1cdcc-112">Chiamare questo metodo dall'interno del metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="1cdcc-113">La classe **CBaseStreamControl** usa l'interfaccia **IMediaEventSink** per inviare il controllo del [**flusso EC \_ \_ \_ avviato**](ec-stream-control-started.md) e gli eventi di [**controllo del flusso EC \_ \_ \_ interrotti**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="1cdcc-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="1cdcc-114">Se il filtro deriva da **CBaseFilter**, chiamare prima il metodo [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , che imposta la variabile membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="1cdcc-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="1cdcc-115">Passare quindi **m \_ pSink** al `SetFilterGraph` metodo.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="1cdcc-116">Si noti che **m \_ PSink** è **null** quando il filtro esce dal grafico, che è corretto.</span><span class="sxs-lookup"><span data-stu-id="1cdcc-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="1cdcc-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cdcc-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1cdcc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cdcc-118">Requirements</span></span>



| <span data-ttu-id="1cdcc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cdcc-119">Requirement</span></span> | <span data-ttu-id="1cdcc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1cdcc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cdcc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cdcc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1cdcc-122"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cdcc-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1cdcc-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cdcc-123">Library</span></span><br/> | <dl> <span data-ttu-id="1cdcc-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1cdcc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cdcc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cdcc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cdcc-126">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="1cdcc-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




