---
description: Il Metodo BeginFlush informa il filtro proprietario per scaricare i filtri downstream. La classe derivata deve implementare questo metodo.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Metodo CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328489"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="382d6-104">CPullPin. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="382d6-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="382d6-105">Il `BeginFlush` metodo informa il filtro proprietario per scaricare i filtri downstream.</span><span class="sxs-lookup"><span data-stu-id="382d6-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="382d6-106">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="382d6-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="382d6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="382d6-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="382d6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="382d6-108">Parameters</span></span>

<span data-ttu-id="382d6-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="382d6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="382d6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="382d6-110">Return value</span></span>

<span data-ttu-id="382d6-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="382d6-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="382d6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="382d6-112">Remarks</span></span>

<span data-ttu-id="382d6-113">Il metodo [**CPullPin:: Seek**](cpullpin-seek.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="382d6-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="382d6-114">Implementare questo metodo per chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) su ogni pin di input downstream che riceve i dati da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="382d6-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="382d6-115">Se i pin di output del filtro derivano da [**CBaseOutputPin**](cbaseoutputpin.md), chiamare il metodo [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="382d6-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="382d6-116">Questa progettazione consente al filtro di cercare il flusso semplicemente chiamando **Seek** sull'oggetto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="382d6-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="382d6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="382d6-117">Requirements</span></span>



| <span data-ttu-id="382d6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="382d6-118">Requirement</span></span> | <span data-ttu-id="382d6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="382d6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382d6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="382d6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="382d6-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="382d6-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="382d6-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="382d6-122">Library</span></span><br/> | <dl> <span data-ttu-id="382d6-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="382d6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382d6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="382d6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382d6-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="382d6-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




