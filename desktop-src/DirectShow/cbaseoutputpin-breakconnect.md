---
description: 'Metodo CBaseOutputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Metodo CBaseOutputPin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: 746783a73892bc34273da4b020446f2668a19cd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096219"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="cb8b2-103">Metodo CBaseOutputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="cb8b2-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="cb8b2-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb8b2-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="cb8b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb8b2-106">Parameters</span></span>

<span data-ttu-id="cb8b2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb8b2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb8b2-108">Return value</span></span>

<span data-ttu-id="cb8b2-109">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb8b2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb8b2-110">Remarks</span></span>

<span data-ttu-id="cb8b2-111">Questo metodo esegue l'override [**del metodo CBasePin::BreakConnect.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="cb8b2-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="cb8b2-112">Disaccoppia l'allocatore e rilascia [**le interfacce IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) e [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="cb8b2-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="cb8b2-113">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="cb8b2-114">In caso contrario, potrebbero verificarsi perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb8b2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb8b2-115">Requirements</span></span>



| <span data-ttu-id="cb8b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb8b2-116">Requirement</span></span> | <span data-ttu-id="cb8b2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cb8b2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8b2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb8b2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cb8b2-119"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb8b2-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb8b2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb8b2-120">Library</span></span><br/> | <dl> <span data-ttu-id="cb8b2-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb8b2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb8b2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb8b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8b2-123">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cb8b2-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




