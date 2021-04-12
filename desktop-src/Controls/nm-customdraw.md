---
title: Codice di notifica NM_CUSTOMDRAW (COMmctrl. h)
description: Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- Controlli di Windows per il codice di notifica NM_CUSTOMDRAW
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475155"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="1a1e0-105">\_Codice di notifica CUSTOMDRAW Nm</span><span class="sxs-lookup"><span data-stu-id="1a1e0-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="1a1e0-106">Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="1a1e0-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1e0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="1a1e0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a1e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a1e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a1e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a1e0-110">Puntatore a una struttura personalizzata correlata al disegno che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="1a1e0-111">Nell'elenco seguente vengono specificati i controlli e le relative strutture associate.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="1a1e0-112">Control</span><span class="sxs-lookup"><span data-stu-id="1a1e0-112">Control</span></span>                     | <span data-ttu-id="1a1e0-113">Struttura di progetto personalizzata</span><span class="sxs-lookup"><span data-stu-id="1a1e0-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="1a1e0-114">Rebar, TrackBar e header</span><span class="sxs-lookup"><span data-stu-id="1a1e0-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="1a1e0-115">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="1a1e0-116">Visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="1a1e0-116">List view</span></span>                   | [<span data-ttu-id="1a1e0-117">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="1a1e0-118">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="1a1e0-118">Tooltip</span></span>                     | [<span data-ttu-id="1a1e0-119">**NMTTCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="1a1e0-120">Visualizzazione struttura</span><span class="sxs-lookup"><span data-stu-id="1a1e0-120">Tree view</span></span>                   | [<span data-ttu-id="1a1e0-121">**NMTVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="1a1e0-122">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="1a1e0-122">Toolbar</span></span>                     | [<span data-ttu-id="1a1e0-123">**NMTBCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a1e0-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a1e0-124">Return value</span></span>

<span data-ttu-id="1a1e0-125">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="1a1e0-126">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="1a1e0-127">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-127">You must return one of the following values.</span></span>



| <span data-ttu-id="1a1e0-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1a1e0-128">Return code</span></span>                                                                                            | <span data-ttu-id="1a1e0-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a1e0-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a1e0-130"><dt>**\_DODEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="1a1e0-131">Il controllo viene disegnato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-131">The control will draw itself.</span></span> <span data-ttu-id="1a1e0-132">Non invierà altri codici di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) per questo ciclo di disegno.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="1a1e0-133">Questo flag non può essere usato con altri flag.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="1a1e0-134"><dt>**\_DOERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="1a1e0-135">Il controllo trarrà solo lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1a1e0-136"><dt>**\_NEWFONT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="1a1e0-137">L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="1a1e0-138">Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="1a1e0-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="1a1e0-139">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="1a1e0-140"><dt>**\_NOTIFYITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="1a1e0-141">Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="1a1e0-142">Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="1a1e0-143">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="1a1e0-144"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="1a1e0-145">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="1a1e0-146">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1a1e0-147"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="1a1e0-148">Il controllo invierà un codice di notifica [ \_ CUSTOMDRAW Nm](nm-customdraw.md) quando il ciclo di disegno per l'intero controllo è completo.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="1a1e0-149">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="1a1e0-150"><dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="1a1e0-151">L'applicazione riceverà un codice di notifica [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT \| CDDS \_ sottoelemento prima che ogni elemento secondario di visualizzazione elenco venga disegnato.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="1a1e0-152">È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente oppure restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) per l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="1a1e0-153">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="1a1e0-154"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="1a1e0-155">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-155">Your application drew the item manually.</span></span> <span data-ttu-id="1a1e0-156">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-156">The control will not draw the item.</span></span> <span data-ttu-id="1a1e0-157">Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="1a1e0-158"><dt>**\_SKIPPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="1a1e0-159">Il controllo non trarrà il rettangolo di attivazione intorno a un elemento.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="1a1e0-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a1e0-160">Remarks</span></span>

<span data-ttu-id="1a1e0-161">Attualmente, i controlli seguenti supportano la funzionalità di estrazione personalizzata: intestazione, visualizzazione elenco, Rebar, barra degli strumenti, descrizione comando, TrackBar e visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="1a1e0-162">Il progetto personalizzato è supportato anche per i controlli pulsante se si dispone di un manifesto dell'applicazione per assicurarsi che sia disponibile Comctl32.dll versione 6.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="1a1e0-163">Se questo messaggio viene gestito in una procedura di dialogo, è necessario impostare il valore restituito come parte dei dati della finestra prima di restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="1a1e0-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="1a1e0-164">Per ulteriori informazioni, vedere [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="1a1e0-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1e0-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a1e0-165">Requirements</span></span>



| <span data-ttu-id="1a1e0-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a1e0-166">Requirement</span></span> | <span data-ttu-id="1a1e0-167">Valore</span><span class="sxs-lookup"><span data-stu-id="1a1e0-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1e0-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a1e0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="1a1e0-169">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a1e0-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a1e0-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a1e0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="1a1e0-171">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a1e0-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a1e0-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a1e0-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a1e0-173"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e0-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a1e0-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a1e0-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a1e0-175">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1a1e0-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a1e0-176">Progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="1a1e0-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

