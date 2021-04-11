---
description: Si verifica quando la classe InkCollector rileva un pulsante di cursore inattivo.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Evento InkPicture. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233178"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="994e2-103">Evento InkPicture. CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="994e2-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="994e2-104">Si verifica quando la [**classe InkCollector**](inkcollector-class.md) rileva un pulsante di cursore inattivo.</span><span class="sxs-lookup"><span data-stu-id="994e2-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="994e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="994e2-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="994e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="994e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="994e2-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="994e2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="994e2-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonDown** .</span><span class="sxs-lookup"><span data-stu-id="994e2-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="994e2-109">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="994e2-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="994e2-110">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="994e2-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="994e2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="994e2-111">Return value</span></span>

<span data-ttu-id="994e2-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="994e2-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="994e2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="994e2-113">Remarks</span></span>

<span data-ttu-id="994e2-114">Un pulsante su una punta di penna è inattivo quando l'utente abbassa la penna al digitalizzatore e avvia la traccia di un tratto.</span><span class="sxs-lookup"><span data-stu-id="994e2-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="994e2-115">Quando si preme il pulsante, un pulsante su un barino è inattivo.</span><span class="sxs-lookup"><span data-stu-id="994e2-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="994e2-116">Quando si preme il pulsante destro del mouse, si ricevono effettivamente due eventi **CursorButtonDown** , uno per il pulsante destro premuto e uno per il pulsante sinistro premuto.</span><span class="sxs-lookup"><span data-stu-id="994e2-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="994e2-117">Questo metodo di evento viene definito in **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) con l'ID DISPID \_ ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="994e2-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="994e2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="994e2-118">Requirements</span></span>



| <span data-ttu-id="994e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="994e2-119">Requirement</span></span> | <span data-ttu-id="994e2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="994e2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994e2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="994e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="994e2-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="994e2-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="994e2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="994e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="994e2-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="994e2-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="994e2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="994e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="994e2-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="994e2-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="994e2-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="994e2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="994e2-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="994e2-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="994e2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="994e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994e2-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="994e2-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="994e2-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="994e2-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="994e2-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="994e2-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="994e2-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="994e2-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="994e2-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="994e2-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




