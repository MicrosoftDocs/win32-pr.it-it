---
description: 'Il metodo JoinFilterGraph notifica al filtro che è stato aggiunto o lasciato un grafico di filtro. Questo metodo implementa il metodo IBaseFilter:: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Metodo CBaseFilter. JoinFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331538"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="e7b90-104">CBaseFilter. JoinFilterGraph, metodo</span><span class="sxs-lookup"><span data-stu-id="e7b90-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="e7b90-105">Il `JoinFilterGraph` metodo notifica al filtro che è stato aggiunto o ha lasciato un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="e7b90-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="e7b90-106">Questo metodo implementa il metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="e7b90-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b90-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7b90-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="e7b90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7b90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b90-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="e7b90-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b90-110">Puntatore all'interfaccia [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) dell'oggetto Filter Graph Manager oppure **null** se il filtro sta uscendo dal grafico.</span><span class="sxs-lookup"><span data-stu-id="e7b90-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="e7b90-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7b90-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b90-112">Puntatore a una stringa Unicode contenente un nome per il filtro.</span><span class="sxs-lookup"><span data-stu-id="e7b90-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b90-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7b90-113">Return value</span></span>

<span data-ttu-id="e7b90-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7b90-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b90-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7b90-115">Remarks</span></span>

<span data-ttu-id="e7b90-116">Questo metodo imposta la variabile membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) uguale al parametro *pGraph* .</span><span class="sxs-lookup"><span data-stu-id="e7b90-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="e7b90-117">Viene inoltre eseguita una query per un puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) e viene archiviato nella variabile membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b90-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="e7b90-118">Tuttavia, il filtro non mantiene un conteggio dei riferimenti in nessuna di queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="e7b90-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="e7b90-119">In questo modo si creerebbe un conteggio dei riferimenti circolari, perché il gestore del grafico del filtro mantiene un conteggio dei riferimenti sul filtro.</span><span class="sxs-lookup"><span data-stu-id="e7b90-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="e7b90-120">Il metodo copia la stringa specificata da *pname* nella variabile membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b90-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b90-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b90-121">Requirements</span></span>



| <span data-ttu-id="e7b90-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b90-122">Requirement</span></span> | <span data-ttu-id="e7b90-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b90-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b90-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b90-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b90-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b90-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e7b90-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7b90-126">Library</span></span><br/> | <dl> <span data-ttu-id="e7b90-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b90-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b90-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b90-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b90-129">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e7b90-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




