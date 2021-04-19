---
description: Il metodo CompleteConnect completa una connessione a un pin di input.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Metodo CDynamicOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333449"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="c9d23-103">CDynamicOutputPin. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="c9d23-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="c9d23-104">Il `CompleteConnect` metodo completa una connessione a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="c9d23-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9d23-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c9d23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9d23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d23-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="c9d23-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d23-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="c9d23-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d23-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9d23-109">Return value</span></span>

<span data-ttu-id="c9d23-110">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c9d23-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d23-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9d23-111">Remarks</span></span>

<span data-ttu-id="c9d23-112">Questo metodo esegue l'override del metodo [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d23-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="c9d23-113">Per supportare la riconnessione dinamica, questo metodo consente di eseguire il commit dell'allocatore se il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="c9d23-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="c9d23-114">Nella classe di base le connessioni possono verificarsi solo quando il filtro viene arrestato, quindi viene sempre eseguito il commit dell'allocatore nel metodo [**CBaseOutputPin:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d23-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d23-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9d23-115">Requirements</span></span>



| <span data-ttu-id="c9d23-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d23-116">Requirement</span></span> | <span data-ttu-id="c9d23-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c9d23-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d23-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9d23-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c9d23-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d23-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c9d23-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="c9d23-120">Library</span></span><br/> | <dl> <span data-ttu-id="c9d23-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d23-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d23-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9d23-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d23-123">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c9d23-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




