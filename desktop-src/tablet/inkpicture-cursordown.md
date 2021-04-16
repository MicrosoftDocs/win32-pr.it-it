---
description: Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529898"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="f477b-103">Evento InkPicture. CursorDown</span><span class="sxs-lookup"><span data-stu-id="f477b-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="f477b-104">Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="f477b-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f477b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f477b-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="f477b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f477b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f477b-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f477b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f477b-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="f477b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="f477b-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f477b-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f477b-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che è stato avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'attivazione dell'evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="f477b-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f477b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f477b-111">Return value</span></span>

<span data-ttu-id="f477b-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f477b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f477b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f477b-113">Remarks</span></span>

<span data-ttu-id="f477b-114">Questi metodi di evento sono definiti nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="f477b-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="f477b-115">Le interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementano l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="f477b-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="f477b-116">Utilizzare attentamente questo evento perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se nei gestori eventi viene eseguita una quantità eccessiva di codice.</span><span class="sxs-lookup"><span data-stu-id="f477b-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="f477b-117">Per migliorare le prestazioni in tempo reale dell'input penna, nascondere o mostrare il cursore del mouse nei gestori eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="f477b-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f477b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f477b-118">Requirements</span></span>



| <span data-ttu-id="f477b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f477b-119">Requirement</span></span> | <span data-ttu-id="f477b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f477b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f477b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f477b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f477b-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f477b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f477b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f477b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f477b-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f477b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f477b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f477b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f477b-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f477b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f477b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f477b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f477b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f477b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f477b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f477b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f477b-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f477b-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f477b-131">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="f477b-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="f477b-132">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="f477b-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f477b-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="f477b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="f477b-134">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="f477b-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

