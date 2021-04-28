---
description: 'Evento InkPicture.CursorButtonDown: si verifica quando la classe InkCollector rileva un pulsante del cursore verso il basso.'
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Evento InkPicture.CursorButtonDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2017cd7dc2291bdb29aa01df3d94f20211b7cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116779"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="18817-103">Evento InkPicture.CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="18817-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="18817-104">Si verifica quando [**la classe InkCollector**](inkcollector-class.md) rileva un pulsante del cursore verso il basso.</span><span class="sxs-lookup"><span data-stu-id="18817-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="18817-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18817-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="18817-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18817-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18817-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="18817-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18817-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorButtonDown.**</span><span class="sxs-lookup"><span data-stu-id="18817-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="18817-109">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="18817-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18817-110">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="18817-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18817-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18817-111">Return value</span></span>

<span data-ttu-id="18817-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18817-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18817-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="18817-113">Remarks</span></span>

<span data-ttu-id="18817-114">Un pulsante sulla punta di una penna è verso il basso quando l'utente abbassa la penna al digitalizzatore e inizia a tracciare un tratto.</span><span class="sxs-lookup"><span data-stu-id="18817-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="18817-115">Quando si preme il pulsante, un pulsante su un cane è in giù.</span><span class="sxs-lookup"><span data-stu-id="18817-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="18817-116">Quando premi il pulsante destro del mouse, ricevi effettivamente due eventi **CursorButtonDown:** uno per il pulsante destro premuto e uno per il pulsante sinistro premuto.</span><span class="sxs-lookup"><span data-stu-id="18817-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="18817-117">Questo metodo di evento è definito nell'interfaccia di solo invio **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="18817-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="18817-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18817-118">Requirements</span></span>



| <span data-ttu-id="18817-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="18817-119">Requirement</span></span> | <span data-ttu-id="18817-120">Valore</span><span class="sxs-lookup"><span data-stu-id="18817-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18817-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18817-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18817-122">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="18817-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="18817-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18817-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18817-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="18817-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="18817-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18817-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="18817-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="18817-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18817-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="18817-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="18817-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18817-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="18817-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18817-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18817-130">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="18817-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="18817-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="18817-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="18817-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="18817-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="18817-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="18817-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="18817-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="18817-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




