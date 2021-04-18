---
description: Il metodo DoneWithWindow Elimina la finestra.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Metodo CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325332"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="ea781-103">CBaseWindow. DoneWithWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="ea781-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="ea781-104">Il `DoneWithWindow` metodo elimina la finestra.</span><span class="sxs-lookup"><span data-stu-id="ea781-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea781-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea781-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="ea781-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea781-106">Parameters</span></span>

<span data-ttu-id="ea781-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ea781-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea781-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea781-108">Return value</span></span>

<span data-ttu-id="ea781-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea781-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea781-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea781-110">Remarks</span></span>

<span data-ttu-id="ea781-111">Chiamare questo metodo dal metodo distruttore dell'oggetto derivato.</span><span class="sxs-lookup"><span data-stu-id="ea781-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="ea781-112">Se questo metodo viene chiamato dallo stesso thread che ha creato la finestra, il metodo esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea781-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="ea781-113">Chiama il metodo [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , che disattiva la finestra.</span><span class="sxs-lookup"><span data-stu-id="ea781-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="ea781-114">Chiama il metodo [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , che rilascia le risorse usate dalla finestra.</span><span class="sxs-lookup"><span data-stu-id="ea781-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="ea781-115">Elimina definitivamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="ea781-115">Destroys the window.</span></span>

<span data-ttu-id="ea781-116">Se il thread `DoneWithWindow` che chiama non è il thread che ha creato la finestra, il metodo invia un messaggio "Destroy" privato alla finestra.</span><span class="sxs-lookup"><span data-stu-id="ea781-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="ea781-117">Quando la finestra riceve questo messaggio, chiama `DoneWithWindow` su se stesso.</span><span class="sxs-lookup"><span data-stu-id="ea781-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="ea781-118">Se [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) è **true**, la finestra Invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea781-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="ea781-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea781-119">Requirements</span></span>



| <span data-ttu-id="ea781-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea781-120">Requirement</span></span> | <span data-ttu-id="ea781-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ea781-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea781-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea781-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ea781-123"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea781-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea781-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea781-124">Library</span></span><br/> | <dl> <span data-ttu-id="ea781-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ea781-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea781-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea781-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea781-127">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ea781-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




