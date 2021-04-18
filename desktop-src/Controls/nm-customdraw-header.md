---
title: Codice di notifica di NM_CUSTOMDRAW (intestazione) (COMmctrl. h)
description: Inviato da un controllo intestazione per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Codice di notifica di NM_CUSTOMDRAW (intestazione) controlli Windows
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302792"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="73388-105">\_Codice di notifica di CUSTOMDRAW (intestazione) Nm</span><span class="sxs-lookup"><span data-stu-id="73388-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="73388-106">Inviato da un controllo intestazione per notificare alla finestra padre le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="73388-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="73388-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73388-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="73388-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="73388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73388-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73388-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73388-110">Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="73388-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="73388-111">Il membro **dwItemSpec** di questa struttura contiene l'indice dell'elemento da disegnare e il membro **lItemlParam** di questa struttura contiene l'elemento *lParam* dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="73388-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73388-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73388-112">Return value</span></span>

<span data-ttu-id="73388-113">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="73388-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="73388-114">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="73388-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="73388-115">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="73388-115">You must return one of the following values.</span></span>



| <span data-ttu-id="73388-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="73388-116">Return code</span></span>                                                                                            | <span data-ttu-id="73388-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73388-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73388-118"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="73388-119">Il controllo viene disegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="73388-119">The control will draw itself.</span></span> <span data-ttu-id="73388-120">Non invierà alcun messaggio [ \_ CUSTOMDRAW Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="73388-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="73388-121">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="73388-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="73388-122"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="73388-123">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="73388-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="73388-124">Invierà i \_ codici di notifica di CUSTOMDRAW prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="73388-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="73388-125">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="73388-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="73388-126"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="73388-127">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="73388-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="73388-128">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="73388-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="73388-129"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="73388-130">Il controllo invierà una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="73388-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="73388-131">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="73388-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="73388-132"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="73388-133">[Versioni di controllo comuni](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="73388-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="73388-134">Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="73388-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="73388-135">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="73388-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="73388-136"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="73388-137">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="73388-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="73388-138">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="73388-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="73388-139">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="73388-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="73388-140"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="73388-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="73388-141">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="73388-141">Your application drew the item manually.</span></span> <span data-ttu-id="73388-142">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="73388-142">The control will not draw the item.</span></span> <span data-ttu-id="73388-143">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="73388-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="73388-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="73388-144">Remarks</span></span>

<span data-ttu-id="73388-145">Per ulteriori informazioni, vedere [utilizzo del progetto personalizzato](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="73388-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="73388-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73388-146">Requirements</span></span>



| <span data-ttu-id="73388-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="73388-147">Requirement</span></span> | <span data-ttu-id="73388-148">Valore</span><span class="sxs-lookup"><span data-stu-id="73388-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73388-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73388-149">Minimum supported client</span></span><br/> | <span data-ttu-id="73388-150">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73388-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73388-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73388-151">Minimum supported server</span></span><br/> | <span data-ttu-id="73388-152">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73388-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73388-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73388-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="73388-154"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73388-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





