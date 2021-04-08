---
title: Codice di notifica di NM_CUSTOMDRAW (descrizione comando) (COMmctrl. h)
description: Inviato da un controllo ToolTip per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW (descrizione comando) il codice di notifica controlli Windows
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743978"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="422e4-105">\_Codice di notifica di CUSTOMDRAW Nm (descrizione comando)</span><span class="sxs-lookup"><span data-stu-id="422e4-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="422e4-106">Inviato da un controllo ToolTip per notificare alla finestra padre le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="422e4-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="422e4-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="422e4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="422e4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="422e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="422e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="422e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="422e4-110">Puntatore a una struttura [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="422e4-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="422e4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="422e4-111">Return value</span></span>

<span data-ttu-id="422e4-112">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="422e4-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="422e4-113">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="422e4-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="422e4-114">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="422e4-114">You must return one of the following values.</span></span>



| <span data-ttu-id="422e4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="422e4-115">Return code</span></span>                                                                                            | <span data-ttu-id="422e4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="422e4-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="422e4-117"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="422e4-118">Il controllo viene disegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="422e4-118">The control will draw itself.</span></span> <span data-ttu-id="422e4-119">Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="422e4-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="422e4-120">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="422e4-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="422e4-121"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="422e4-122">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="422e4-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="422e4-123">Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="422e4-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="422e4-124">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="422e4-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="422e4-125"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="422e4-126">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="422e4-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="422e4-127">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="422e4-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="422e4-128"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="422e4-129">Il controllo invierà una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="422e4-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="422e4-130">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="422e4-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="422e4-131"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="422e4-132">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="422e4-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="422e4-133">Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="422e4-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="422e4-134">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="422e4-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="422e4-135"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="422e4-136">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="422e4-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="422e4-137">Il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="422e4-137">The control will use the new font.</span></span> <span data-ttu-id="422e4-138">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="422e4-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="422e4-139">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="422e4-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="422e4-140"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="422e4-141">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="422e4-141">Your application drew the item manually.</span></span> <span data-ttu-id="422e4-142">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="422e4-142">The control will not draw the item.</span></span> <span data-ttu-id="422e4-143">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="422e4-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="422e4-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="422e4-144">Requirements</span></span>



| <span data-ttu-id="422e4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="422e4-145">Requirement</span></span> | <span data-ttu-id="422e4-146">Valore</span><span class="sxs-lookup"><span data-stu-id="422e4-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="422e4-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="422e4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="422e4-148">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="422e4-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="422e4-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="422e4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="422e4-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="422e4-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="422e4-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="422e4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="422e4-152"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="422e4-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422e4-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="422e4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422e4-154">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="422e4-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





