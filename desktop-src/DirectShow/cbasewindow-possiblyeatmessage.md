---
description: Il metodo PossiblyEatMessage consente a una classe derivata di inviare messaggi a un'altra finestra.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Metodo CBaseWindow. PossiblyEatMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325759"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="25852-103">CBaseWindow. PossiblyEatMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="25852-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="25852-104">Il `PossiblyEatMessage` metodo consente a una classe derivata di inviare messaggi a un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="25852-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="25852-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25852-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="25852-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25852-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="25852-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="25852-108">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="25852-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="25852-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25852-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25852-110">Primo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="25852-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="25852-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25852-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25852-112">Secondo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="25852-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25852-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25852-113">Return value</span></span>

<span data-ttu-id="25852-114">Restituisce **true** se il messaggio è stato inviato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="25852-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="25852-115">La classe base restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="25852-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="25852-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="25852-116">Remarks</span></span>

<span data-ttu-id="25852-117">Prima che il metodo [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) gestisca un messaggio, chiama `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="25852-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="25852-118">Se `PossiblyEatMessage` restituisce **true**, **OnReceiveMessage** ignora il messaggio.</span><span class="sxs-lookup"><span data-stu-id="25852-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="25852-119">Una classe derivata può eseguire l'override `PossiblyEatMessage` di in modo che inoltri alcuni messaggi a una finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="25852-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="25852-120">Ad esempio, la classe [**CBaseControlWindow**](cbasecontrolwindow.md) , che deriva da **CBaseWindow**, trasmette i messaggi della tastiera e del mouse.</span><span class="sxs-lookup"><span data-stu-id="25852-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="25852-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25852-121">Requirements</span></span>



| <span data-ttu-id="25852-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25852-122">Requirement</span></span> | <span data-ttu-id="25852-123">Valore</span><span class="sxs-lookup"><span data-stu-id="25852-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25852-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25852-124">Header</span></span><br/>  | <dl> <span data-ttu-id="25852-125"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25852-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25852-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="25852-126">Library</span></span><br/> | <dl> <span data-ttu-id="25852-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25852-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25852-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25852-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25852-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="25852-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




