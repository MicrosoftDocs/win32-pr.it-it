---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Metodo CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329554"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="a30b9-103">CBaseOutputPin. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="a30b9-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="a30b9-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="a30b9-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a30b9-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="a30b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a30b9-106">Parameters</span></span>

<span data-ttu-id="a30b9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a30b9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a30b9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a30b9-108">Return value</span></span>

<span data-ttu-id="a30b9-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="a30b9-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a30b9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a30b9-110">Remarks</span></span>

<span data-ttu-id="a30b9-111">Questo metodo esegue l'override del metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a30b9-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="a30b9-112">Elimina il commit dell'allocatore e rilascia le interfacce [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) e [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="a30b9-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="a30b9-113">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo che esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="a30b9-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="a30b9-114">In caso contrario, è possibile che si verifichino perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="a30b9-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30b9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a30b9-115">Requirements</span></span>



| <span data-ttu-id="a30b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30b9-116">Requirement</span></span> | <span data-ttu-id="a30b9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a30b9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30b9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a30b9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a30b9-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a30b9-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a30b9-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="a30b9-120">Library</span></span><br/> | <dl> <span data-ttu-id="a30b9-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a30b9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30b9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a30b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30b9-123">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a30b9-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




