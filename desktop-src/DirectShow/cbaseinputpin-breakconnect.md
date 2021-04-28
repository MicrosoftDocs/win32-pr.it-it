---
description: 'Metodo CBaseInputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Metodo CBaseInputPin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099739"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="888a5-103">Metodo CBaseInputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="888a5-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="888a5-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="888a5-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="888a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="888a5-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="888a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="888a5-106">Parameters</span></span>

<span data-ttu-id="888a5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="888a5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="888a5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="888a5-108">Return value</span></span>

<span data-ttu-id="888a5-109">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="888a5-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="888a5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="888a5-110">Remarks</span></span>

<span data-ttu-id="888a5-111">Questo metodo esegue l'override [**del metodo CBasePin::BreakConnect.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="888a5-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="888a5-112">Decomminzione dell'allocatore e rilascio [**dell'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="888a5-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="888a5-113">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.</span><span class="sxs-lookup"><span data-stu-id="888a5-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="888a5-114">In caso contrario, potrebbero verificarsi perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="888a5-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="888a5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="888a5-115">Requirements</span></span>



| <span data-ttu-id="888a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="888a5-116">Requirement</span></span> | <span data-ttu-id="888a5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="888a5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888a5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="888a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="888a5-119"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="888a5-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="888a5-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="888a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="888a5-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="888a5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888a5-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="888a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888a5-123">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="888a5-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




