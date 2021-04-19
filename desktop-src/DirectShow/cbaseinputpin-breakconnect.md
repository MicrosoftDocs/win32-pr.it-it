---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Metodo CBaseInputPin. BreakConnect (Amfilter. h)
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
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327958"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="a5572-103">CBaseInputPin. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="a5572-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="a5572-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="a5572-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5572-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5572-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="a5572-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5572-106">Parameters</span></span>

<span data-ttu-id="a5572-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a5572-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5572-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5572-108">Return value</span></span>

<span data-ttu-id="a5572-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="a5572-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5572-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5572-110">Remarks</span></span>

<span data-ttu-id="a5572-111">Questo metodo esegue l'override del metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a5572-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="a5572-112">Elimina il commit dell'allocatore e rilascia l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="a5572-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="a5572-113">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo che esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="a5572-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="a5572-114">In caso contrario, è possibile che si verifichino perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="a5572-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5572-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5572-115">Requirements</span></span>



| <span data-ttu-id="a5572-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5572-116">Requirement</span></span> | <span data-ttu-id="a5572-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a5572-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5572-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5572-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a5572-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5572-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5572-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5572-120">Library</span></span><br/> | <dl> <span data-ttu-id="a5572-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a5572-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5572-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5572-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5572-123">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="a5572-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




