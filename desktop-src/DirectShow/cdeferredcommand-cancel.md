---
description: 'Il metodo Cancel Annulla una richiesta CDeferredCommand:: Invoke precedentemente accodata.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Metodo CDeferredCommand. Cancel (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333208"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="b325b-103">CDeferredCommand. Cancel, metodo</span><span class="sxs-lookup"><span data-stu-id="b325b-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="b325b-104">Il `Cancel` metodo annulla una richiesta [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) precedentemente accodata.</span><span class="sxs-lookup"><span data-stu-id="b325b-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b325b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b325b-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="b325b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b325b-106">Parameters</span></span>

<span data-ttu-id="b325b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b325b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b325b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b325b-108">Return value</span></span>

<span data-ttu-id="b325b-109">Restituisce VFW \_ E \_ già \_ annullato se **m \_ pQueue** è **null**.</span><span class="sxs-lookup"><span data-stu-id="b325b-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="b325b-110">Restituisce un valore **HRESULT** da [**CCmdQueue:: Remove**](ccmdqueue-remove.md) se la chiamata genera un errore.</span><span class="sxs-lookup"><span data-stu-id="b325b-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="b325b-111">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b325b-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b325b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b325b-112">Remarks</span></span>

<span data-ttu-id="b325b-113">Questa funzione membro implementa il metodo [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .</span><span class="sxs-lookup"><span data-stu-id="b325b-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b325b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b325b-114">Requirements</span></span>



| <span data-ttu-id="b325b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b325b-115">Requirement</span></span> | <span data-ttu-id="b325b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b325b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b325b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b325b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b325b-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b325b-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b325b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b325b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b325b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b325b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b325b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b325b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b325b-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="b325b-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




