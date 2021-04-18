---
description: Recupera l'handle per il thread nell'oggetto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Metodo CMsgThread. GetThreadHandle (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328832"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="c0458-103">CMsgThread. GetThreadHandle, metodo</span><span class="sxs-lookup"><span data-stu-id="c0458-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="c0458-104">Recupera l'handle per il thread nell'oggetto [**CMsgThread**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="c0458-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0458-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0458-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="c0458-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0458-106">Parameters</span></span>

<span data-ttu-id="c0458-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c0458-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0458-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0458-108">Return value</span></span>

<span data-ttu-id="c0458-109">Restituisce l'handle del thread.</span><span class="sxs-lookup"><span data-stu-id="c0458-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0458-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0458-110">Remarks</span></span>

<span data-ttu-id="c0458-111">È possibile passare l'handle del thread alle funzioni di attesa, ad esempio [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="c0458-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="c0458-112">L'handle del thread viene segnalato quando il thread è terminato.</span><span class="sxs-lookup"><span data-stu-id="c0458-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0458-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0458-113">Requirements</span></span>



| <span data-ttu-id="c0458-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0458-114">Requirement</span></span> | <span data-ttu-id="c0458-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c0458-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0458-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0458-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c0458-117"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0458-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0458-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0458-118">Library</span></span><br/> | <dl> <span data-ttu-id="c0458-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0458-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0458-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0458-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0458-121">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="c0458-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

