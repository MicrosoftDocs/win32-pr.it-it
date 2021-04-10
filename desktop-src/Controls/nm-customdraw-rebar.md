---
title: Codice di notifica di NM_CUSTOMDRAW (Rebar) (COMmctrl. h)
description: Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- NM_CUSTOMDRAW (Rebar) il codice di notifica controlli Windows
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121734"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="db9d8-105">\_Codice di notifica CUSTOMDRAW (Rebar) Nm</span><span class="sxs-lookup"><span data-stu-id="db9d8-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="db9d8-106">Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="db9d8-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="db9d8-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="db9d8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="db9d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db9d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db9d8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db9d8-110">Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="db9d8-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="db9d8-111">Il membro **dwItemSpec** della struttura contiene l'identificatore della banda da disegnare.</span><span class="sxs-lookup"><span data-stu-id="db9d8-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="db9d8-112">Il membro **lItemlParam** della struttura contiene il *lParam* della banda da disegnare.</span><span class="sxs-lookup"><span data-stu-id="db9d8-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9d8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db9d8-113">Return value</span></span>

<span data-ttu-id="db9d8-114">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="db9d8-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="db9d8-115">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="db9d8-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="db9d8-116">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="db9d8-116">You must return one of the following values.</span></span>



| <span data-ttu-id="db9d8-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="db9d8-117">Return code</span></span>                                                                                            | <span data-ttu-id="db9d8-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db9d8-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db9d8-119"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="db9d8-120">Il controllo viene disegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="db9d8-120">The control will draw itself.</span></span> <span data-ttu-id="db9d8-121">Non invierà altre notifiche [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="db9d8-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="db9d8-122">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="db9d8-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="db9d8-123"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="db9d8-124">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="db9d8-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="db9d8-125">Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="db9d8-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="db9d8-126">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="db9d8-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="db9d8-127"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="db9d8-128">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="db9d8-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="db9d8-129">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="db9d8-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="db9d8-130"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="db9d8-131">Il controllo invierà una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="db9d8-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="db9d8-132">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="db9d8-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="db9d8-133"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="db9d8-134">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="db9d8-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="db9d8-135">Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="db9d8-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="db9d8-136">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="db9d8-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="db9d8-137"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="db9d8-138">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="db9d8-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="db9d8-139">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="db9d8-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="db9d8-140">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="db9d8-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="db9d8-141"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="db9d8-142">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="db9d8-142">The application drew the item manually.</span></span> <span data-ttu-id="db9d8-143">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="db9d8-143">The control will not draw the item.</span></span> <span data-ttu-id="db9d8-144">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="db9d8-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="db9d8-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db9d8-145">Requirements</span></span>



| <span data-ttu-id="db9d8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9d8-146">Requirement</span></span> | <span data-ttu-id="db9d8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="db9d8-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db9d8-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9d8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="db9d8-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db9d8-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db9d8-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9d8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="db9d8-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db9d8-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db9d8-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db9d8-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9d8-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9d8-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db9d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9d8-155">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="db9d8-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





