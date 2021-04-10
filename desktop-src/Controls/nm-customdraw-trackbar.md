---
title: Codice di notifica di NM_CUSTOMDRAW (TrackBar) (COMmctrl. h)
description: Inviato da un controllo TrackBar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Codice di notifica di NM_CUSTOMDRAW (TrackBar)-controlli Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121731"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="bfa18-105">Codice di notifica di NM \_ CUSTOMDRAW (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="bfa18-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="bfa18-106">Inviato da un controllo TrackBar per notificare alle finestre padre le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="bfa18-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="bfa18-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa18-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bfa18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfa18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfa18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa18-110">Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="bfa18-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="bfa18-111">Il membro **dwItemSpec** di questa struttura conterrà uno dei [valori di disegno personalizzati](custom-draw-values.md) che indica quale parte del controllo viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="bfa18-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="bfa18-112">I controlli TrackBar inseriscono i valori seguenti nel membro **dwItemSpec** della struttura per identificare la parte del controllo da disegnare:</span><span class="sxs-lookup"><span data-stu-id="bfa18-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="bfa18-113">Valore</span><span class="sxs-lookup"><span data-stu-id="bfa18-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="bfa18-114">Significato</span><span class="sxs-lookup"><span data-stu-id="bfa18-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="bfa18-115"><dt>**\_canale TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="bfa18-116">Identifica il canale con cui scorre il marcatore Thumb del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bfa18-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="bfa18-117"><dt>**TBCD \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="bfa18-118">Identifica il marcatore Thumb del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bfa18-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="bfa18-119">Si tratta della parte del controllo che l'utente sposta.</span><span class="sxs-lookup"><span data-stu-id="bfa18-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="bfa18-120"><dt>**\_TIC TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="bfa18-121">Identifica i segni di graduazione di incremento visualizzati lungo il bordo del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bfa18-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa18-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfa18-122">Return value</span></span>

<span data-ttu-id="bfa18-123">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="bfa18-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="bfa18-124">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="bfa18-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="bfa18-125">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-125">You must return one of the following values.</span></span>



| <span data-ttu-id="bfa18-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bfa18-126">Return code</span></span>                                                                                            | <span data-ttu-id="bfa18-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa18-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfa18-128"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="bfa18-129">Il controllo viene disegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bfa18-129">The control will draw itself.</span></span> <span data-ttu-id="bfa18-130">Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="bfa18-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="bfa18-131">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="bfa18-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="bfa18-132"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="bfa18-133">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="bfa18-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="bfa18-134">Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="bfa18-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="bfa18-135">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="bfa18-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="bfa18-136"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="bfa18-137">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa18-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="bfa18-138">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="bfa18-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="bfa18-139"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="bfa18-140">Il controllo invierà una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa18-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="bfa18-141">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="bfa18-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="bfa18-142"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="bfa18-143">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="bfa18-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="bfa18-144">Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="bfa18-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="bfa18-145">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="bfa18-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="bfa18-146"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="bfa18-147">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="bfa18-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="bfa18-148">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="bfa18-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="bfa18-149">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="bfa18-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="bfa18-150"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="bfa18-151">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa18-151">Your application drew the item manually.</span></span> <span data-ttu-id="bfa18-152">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="bfa18-152">The control will not draw the item.</span></span> <span data-ttu-id="bfa18-153">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="bfa18-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="bfa18-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfa18-154">Requirements</span></span>



| <span data-ttu-id="bfa18-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa18-155">Requirement</span></span> | <span data-ttu-id="bfa18-156">Valore</span><span class="sxs-lookup"><span data-stu-id="bfa18-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa18-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa18-157">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa18-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfa18-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa18-159">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa18-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfa18-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfa18-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa18-162"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa18-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfa18-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa18-164">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="bfa18-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





