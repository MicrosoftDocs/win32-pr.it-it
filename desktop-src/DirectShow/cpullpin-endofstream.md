---
description: Il metodo EndOfStream viene chiamato dopo che l'oggetto recapita l'ultimo campione. La classe derivata deve implementare questo metodo.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Metodo CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331171"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="9d405-104">CPullPin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="9d405-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="9d405-105">Il `EndOfStream` metodo viene chiamato dopo che l'oggetto recapita l'ultimo campione.</span><span class="sxs-lookup"><span data-stu-id="9d405-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="9d405-106">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9d405-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d405-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d405-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="9d405-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d405-108">Parameters</span></span>

<span data-ttu-id="9d405-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9d405-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d405-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d405-110">Return value</span></span>

<span data-ttu-id="9d405-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d405-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d405-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d405-112">Remarks</span></span>

<span data-ttu-id="9d405-113">Utilizzare questo metodo per chiamare [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) in ogni pin di input downstream che riceve i dati da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="9d405-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="9d405-114">Se i pin di output del filtro derivano da [**CBaseOutputPin**](cbaseoutputpin.md), chiamare il metodo [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="9d405-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d405-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d405-115">Requirements</span></span>



| <span data-ttu-id="9d405-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d405-116">Requirement</span></span> | <span data-ttu-id="9d405-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9d405-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d405-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d405-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9d405-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d405-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="9d405-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="9d405-120">Library</span></span><br/> | <dl> <span data-ttu-id="9d405-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d405-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d405-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d405-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d405-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="9d405-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




