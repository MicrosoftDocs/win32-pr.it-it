---
description: Il metodo OnReceiveMessage gestisce i messaggi della finestra.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Metodo CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325761"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="bec75-103">CBaseWindow. OnReceiveMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="bec75-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="bec75-104">Il `OnReceiveMessage` metodo gestisce i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="bec75-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bec75-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="bec75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bec75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec75-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bec75-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bec75-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="bec75-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bec75-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bec75-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bec75-110">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bec75-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bec75-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bec75-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bec75-112">Primo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bec75-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bec75-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bec75-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bec75-114">Secondo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bec75-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec75-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bec75-115">Return value</span></span>

<span data-ttu-id="bec75-116">Restituisce 0 se il messaggio è stato elaborato oppure 1 se il messaggio non è stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="bec75-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec75-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bec75-117">Remarks</span></span>

<span data-ttu-id="bec75-118">La classe base gestisce i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bec75-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="bec75-119">\_chiusura WM</span><span class="sxs-lookup"><span data-stu-id="bec75-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="bec75-120">\_spostamento WM</span><span class="sxs-lookup"><span data-stu-id="bec75-120">WM\_MOVE</span></span>
-   <span data-ttu-id="bec75-121">\_PALETTECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="bec75-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="bec75-122">\_QUERYNEWPALETTE WM</span><span class="sxs-lookup"><span data-stu-id="bec75-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="bec75-123">\_dimensioni WM</span><span class="sxs-lookup"><span data-stu-id="bec75-123">WM\_SIZE</span></span>
-   <span data-ttu-id="bec75-124">\_SYSCOLORCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="bec75-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="bec75-125">Una classe derivata può eseguire l'override di questo metodo per gestire altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="bec75-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="bec75-126">La classe derivata deve chiamare il metodo della classe base per gestire tutti i messaggi ignorati dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="bec75-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec75-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bec75-127">Requirements</span></span>



| <span data-ttu-id="bec75-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec75-128">Requirement</span></span> | <span data-ttu-id="bec75-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bec75-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec75-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bec75-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bec75-131"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bec75-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bec75-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="bec75-132">Library</span></span><br/> | <dl> <span data-ttu-id="bec75-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bec75-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec75-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bec75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec75-135">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="bec75-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




