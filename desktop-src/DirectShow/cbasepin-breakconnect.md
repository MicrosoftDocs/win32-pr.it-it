---
description: 'Metodo CBasePin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Metodo CBasePin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099439"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="b0186-103">Metodo CBasePin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="b0186-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="b0186-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="b0186-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0186-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0186-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="b0186-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0186-106">Parameters</span></span>

<span data-ttu-id="b0186-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b0186-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0186-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0186-108">Return value</span></span>

<span data-ttu-id="b0186-109">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0186-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0186-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0186-110">Remarks</span></span>

<span data-ttu-id="b0186-111">Questo metodo viene chiamato durante la disconnessione del pin dal [**metodo CBasePin::D isconnect.**](cbasepin-disconnect.md)</span><span class="sxs-lookup"><span data-stu-id="b0186-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="b0186-112">Viene chiamato anche durante un tentativo di connessione se il [**metodo CBasePin::CheckConnect ha**](cbasepin-checkconnect.md) esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b0186-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="b0186-113">Questo metodo deve liberare tutte le risorse ottenute dal **metodo CheckConnect.**</span><span class="sxs-lookup"><span data-stu-id="b0186-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="b0186-114">Ad esempio, se **CheckConnect alloca** memoria, `BreakConnect` deve liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="b0186-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="b0186-115">Se **CheckConnect esegue** una query sul pin di connessione per un'interfaccia, `BreakConnect` deve liberare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b0186-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="b0186-116">Si noti `BreakConnect` che può essere chiamato senza una chiamata corrispondente a **CompleteConnect.**</span><span class="sxs-lookup"><span data-stu-id="b0186-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="b0186-117">Pertanto, non è possibile **presupporre che CompleteConnect** sia stato chiamato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b0186-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0186-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0186-118">Requirements</span></span>



| <span data-ttu-id="b0186-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0186-119">Requirement</span></span> | <span data-ttu-id="b0186-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b0186-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0186-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0186-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b0186-122"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0186-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b0186-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0186-123">Library</span></span><br/> | <dl> <span data-ttu-id="b0186-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0186-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0186-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0186-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0186-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b0186-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




