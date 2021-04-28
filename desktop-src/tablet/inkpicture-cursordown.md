---
description: 'Evento InkPicture.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4b6128589ba2d0b87d4369e8bb58aa66eabf23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116699"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="f4cdf-103">Evento InkPicture.CursorDown</span><span class="sxs-lookup"><span data-stu-id="f4cdf-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="f4cdf-104">Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4cdf-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="f4cdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4cdf-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f4cdf-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4cdf-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="f4cdf-109">*Tratto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f4cdf-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4cdf-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento **CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4cdf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4cdf-111">Return value</span></span>

<span data-ttu-id="f4cdf-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4cdf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4cdf-113">Remarks</span></span>

<span data-ttu-id="f4cdf-114">Questi metodi di evento sono definiti nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents.**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="f4cdf-115">Le interfacce **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementano [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="f4cdf-116">Usare questo evento con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="f4cdf-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="f4cdf-117">Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkpicture-mousedown.md) e [**MouseUp.**](inkpicture-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="f4cdf-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cdf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4cdf-118">Requirements</span></span>



| <span data-ttu-id="f4cdf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4cdf-119">Requirement</span></span> | <span data-ttu-id="f4cdf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f4cdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cdf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4cdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4cdf-122">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="f4cdf-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f4cdf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4cdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4cdf-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f4cdf-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f4cdf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4cdf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4cdf-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdf-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f4cdf-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4cdf-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4cdf-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdf-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f4cdf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4cdf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cdf-130">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="f4cdf-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f4cdf-131">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="f4cdf-132">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f4cdf-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="f4cdf-134">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="f4cdf-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

