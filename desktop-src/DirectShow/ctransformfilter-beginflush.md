---
description: "Metodo CTransformFilter.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Metodo CTransformFilter.BeginFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085159"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="6854a-103">Metodo CTransformFilter.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="6854a-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="6854a-104">Il `BeginFlush` metodo avvia un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="6854a-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6854a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6854a-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="6854a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6854a-106">Parameters</span></span>

<span data-ttu-id="6854a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6854a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6854a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6854a-108">Return value</span></span>

<span data-ttu-id="6854a-109">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6854a-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6854a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6854a-110">Remarks</span></span>

<span data-ttu-id="6854a-111">All'inizio di un'operazione di scaricamento, il metodo [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) del pin di input chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6854a-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="6854a-112">Questo metodo passa la `BeginFlush` chiamata a valle.</span><span class="sxs-lookup"><span data-stu-id="6854a-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="6854a-113">Se la classe derivata usa un thread di lavoro per recapitare i campioni, deve rimuovere tutti i dati in coda durante un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="6854a-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="6854a-114">Questa operazione può essere eseguita nel `BeginFlush` metodo o nel metodo [**EndFlush.**](ctransformfilter-endflush.md)</span><span class="sxs-lookup"><span data-stu-id="6854a-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="6854a-115">Si noti tuttavia che le chiamate a `BeginFlush` non sono sincronizzate con il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="6854a-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="6854a-116">Se il metodo elimina i dati in coda, il filtro deve prestare attenzione a non elaborare altri dati tra le `BeginFlush` `BeginFlush` chiamate **endFlush** e .</span><span class="sxs-lookup"><span data-stu-id="6854a-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="6854a-117">Per altre informazioni, vedere Flusso di dati [per sviluppatori di filtri.](data-flow-for-filter-developers.md)</span><span class="sxs-lookup"><span data-stu-id="6854a-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6854a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6854a-118">Requirements</span></span>



| <span data-ttu-id="6854a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6854a-119">Requirement</span></span> | <span data-ttu-id="6854a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6854a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6854a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6854a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6854a-122"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6854a-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6854a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6854a-123">Library</span></span><br/> | <dl> <span data-ttu-id="6854a-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6854a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6854a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6854a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6854a-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="6854a-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




