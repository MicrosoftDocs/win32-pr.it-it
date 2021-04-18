---
description: Il metodo EndFlush comunica al filtro proprietario di terminare un'operazione di svuotamento. La classe derivata deve implementare questo metodo.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Metodo CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331169"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="64ecc-104">CPullPin. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="64ecc-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="64ecc-105">Il `EndFlush` Metodo comunica al filtro proprietario di terminare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="64ecc-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="64ecc-106">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="64ecc-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ecc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64ecc-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="64ecc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="64ecc-108">Parameters</span></span>

<span data-ttu-id="64ecc-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="64ecc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64ecc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64ecc-110">Return value</span></span>

<span data-ttu-id="64ecc-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64ecc-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ecc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="64ecc-112">Remarks</span></span>

<span data-ttu-id="64ecc-113">Il metodo [**CPullPin:: Seek**](cpullpin-seek.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="64ecc-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="64ecc-114">Implementare questo metodo per chiamare il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) su ogni pin di input downstream che riceve i dati da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="64ecc-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="64ecc-115">Se i pin di output del filtro derivano da **CBaseOutputPin**, chiamare il metodo **CBaseOutputPin::D eliverendflush** .</span><span class="sxs-lookup"><span data-stu-id="64ecc-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="64ecc-116">Questa progettazione consente al filtro di cercare il flusso semplicemente chiamando **Seek** sull'oggetto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="64ecc-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ecc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64ecc-117">Requirements</span></span>



| <span data-ttu-id="64ecc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="64ecc-118">Requirement</span></span> | <span data-ttu-id="64ecc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="64ecc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ecc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64ecc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="64ecc-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="64ecc-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="64ecc-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="64ecc-122">Library</span></span><br/> | <dl> <span data-ttu-id="64ecc-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="64ecc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ecc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64ecc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ecc-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="64ecc-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




