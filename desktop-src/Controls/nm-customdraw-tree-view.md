---
title: Codice di notifica di NM_CUSTOMDRAW (visualizzazione albero) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (visualizzazione albero) controlli di Windows per il codice di notifica
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873317"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="2a1f1-105">\_Codice di notifica di CUSTOMDRAW Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="2a1f1-106">Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="2a1f1-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1f1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2a1f1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a1f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a1f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a1f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a1f1-110">Puntatore a una struttura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) che contiene e riceve informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="2a1f1-111">Il membro **dwItemSpec** del membro **NMCD** di questa struttura contiene l'handle dell'elemento da disegnare.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="2a1f1-112">Il membro **lItemlParam** del membro **NMCD** di questa struttura contiene il *lParam* dell'elemento da disegnare.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a1f1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a1f1-113">Return value</span></span>

<span data-ttu-id="2a1f1-114">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="2a1f1-115">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="2a1f1-116">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-116">You must return one of the following values.</span></span>



| <span data-ttu-id="2a1f1-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2a1f1-117">Return code</span></span>                                                                                            | <span data-ttu-id="2a1f1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a1f1-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a1f1-119"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="2a1f1-120">Il controllo disegna se stesso.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-120">The control draws itself.</span></span> <span data-ttu-id="2a1f1-121">Non invia alcun codice [ \_ CUSTOMDRAW Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="2a1f1-122">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="2a1f1-123"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="2a1f1-124">Il controllo Invia una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="2a1f1-125">Invia i codici di notifica di [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) prima e dopo il disegno di elementi.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="2a1f1-126">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="2a1f1-127"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="2a1f1-128">Il controllo Invia una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="2a1f1-129"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="2a1f1-130">Il controllo Invia una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="2a1f1-131">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="2a1f1-132"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="2a1f1-133">Versione 4,71.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="2a1f1-134">Il controllo Invia una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="2a1f1-135">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="2a1f1-136"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="2a1f1-137">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="2a1f1-138">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="2a1f1-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="2a1f1-139">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="2a1f1-140"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="2a1f1-141">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-141">Your application drew the item manually.</span></span> <span data-ttu-id="2a1f1-142">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-142">The control will not draw the item.</span></span> <span data-ttu-id="2a1f1-143">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="2a1f1-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a1f1-144">Remarks</span></span>

[<span data-ttu-id="2a1f1-145">Versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="2a1f1-146">Se si modifica il tipo di carattere restituendo [**CDRF \_ NEWFONT**](cdrf-constants.md), il controllo di visualizzazione albero potrebbe visualizzare il testo ritagliato.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="2a1f1-147">Questo comportamento è necessario per garantire la compatibilità con le versioni precedenti dei controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="2a1f1-148">Se si desidera modificare il tipo di carattere di un controllo di visualizzazione albero, è possibile ottenere risultati migliori se si invia un messaggio della [**\_ versione CCM**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1f1-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a1f1-149">Requirements</span></span>



| <span data-ttu-id="2a1f1-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1f1-150">Requirement</span></span> | <span data-ttu-id="2a1f1-151">Valore</span><span class="sxs-lookup"><span data-stu-id="2a1f1-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1f1-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a1f1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1f1-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a1f1-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a1f1-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a1f1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1f1-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a1f1-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a1f1-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a1f1-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a1f1-157"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a1f1-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a1f1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1f1-159">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="2a1f1-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





