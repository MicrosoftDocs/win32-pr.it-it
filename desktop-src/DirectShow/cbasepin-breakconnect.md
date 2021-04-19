---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Metodo CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332770"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="6f46d-103">CBasePin. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="6f46d-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="6f46d-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="6f46d-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f46d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f46d-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="6f46d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f46d-106">Parameters</span></span>

<span data-ttu-id="6f46d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6f46d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f46d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f46d-108">Return value</span></span>

<span data-ttu-id="6f46d-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f46d-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f46d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f46d-110">Remarks</span></span>

<span data-ttu-id="6f46d-111">Questo metodo viene chiamato durante la disconnessione del PIN tramite il metodo [**CBasePin::D la connessione**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="6f46d-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="6f46d-112">Viene anche chiamato durante un tentativo di connessione se il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6f46d-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="6f46d-113">Questo metodo deve liberare tutte le risorse ottenute dal metodo **CheckConnect** .</span><span class="sxs-lookup"><span data-stu-id="6f46d-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="6f46d-114">Se, ad esempio, **CheckConnect** alloca memoria, `BreakConnect` deve liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="6f46d-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="6f46d-115">Se **CheckConnect** esegue una query sul pin di connessione per un'interfaccia, `BreakConnect` deve liberare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f46d-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="6f46d-116">Si noti che `BreakConnect` può essere chiamato senza una chiamata corrispondente a **CompleteConnect**.</span><span class="sxs-lookup"><span data-stu-id="6f46d-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="6f46d-117">Pertanto, non è possibile presupporre che **CompleteConnect** sia stato chiamato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6f46d-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f46d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f46d-118">Requirements</span></span>



| <span data-ttu-id="6f46d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f46d-119">Requirement</span></span> | <span data-ttu-id="6f46d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6f46d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f46d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f46d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6f46d-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f46d-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6f46d-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f46d-123">Library</span></span><br/> | <dl> <span data-ttu-id="6f46d-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f46d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f46d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f46d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f46d-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6f46d-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




