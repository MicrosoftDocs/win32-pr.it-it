---
title: Messaggio WM_CTLCOLORSCROLLBAR (winuser. h)
description: Il \_ messaggio WM CTLCOLORSCROLLBAR viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Controlli di Windows Message WM_CTLCOLORSCROLLBAR
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964156"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="38db0-104">\_Messaggio CTLCOLORSCROLLBAR WM</span><span class="sxs-lookup"><span data-stu-id="38db0-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="38db0-105">Il messaggio **WM \_ CTLCOLORSCROLLBAR** viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato.</span><span class="sxs-lookup"><span data-stu-id="38db0-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="38db0-106">Rispondendo a questo messaggio, la finestra padre può utilizzare l'handle del contesto di visualizzazione per impostare il colore di sfondo del controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="38db0-107">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="38db0-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="38db0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38db0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38db0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38db0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38db0-110">Handle per il contesto di dispositivo per il controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38db0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38db0-112">Handle per la barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38db0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38db0-113">Return value</span></span>

<span data-ttu-id="38db0-114">Se un'applicazione elabora il messaggio, deve restituire l'handle a un pennello.</span><span class="sxs-lookup"><span data-stu-id="38db0-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="38db0-115">Il sistema utilizza il pennello per disegnare lo sfondo del controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="38db0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="38db0-116">Remarks</span></span>

<span data-ttu-id="38db0-117">Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="38db0-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="38db0-118">Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="38db0-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="38db0-119">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="38db0-120">Il messaggio **WM \_ CTLCOLORSCROLLBAR** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.</span><span class="sxs-lookup"><span data-stu-id="38db0-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="38db0-121">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="38db0-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="38db0-122">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="38db0-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="38db0-123">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="38db0-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="38db0-124">Il messaggio **WM \_ CTLCOLORSCROLLBAR** viene usato solo dai controlli della barra di scorrimento figlio.</span><span class="sxs-lookup"><span data-stu-id="38db0-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="38db0-125">Le barre di scorrimento associate a una finestra (WS \_ Scroll e WS \_ VSCROLL) non generano questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="38db0-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="38db0-126">Per personalizzare l'aspetto delle barre di scorrimento associate a una finestra, utilizzare le funzioni della barra di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="38db0-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="38db0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38db0-127">Requirements</span></span>



| <span data-ttu-id="38db0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="38db0-128">Requirement</span></span> | <span data-ttu-id="38db0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="38db0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38db0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38db0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="38db0-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38db0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38db0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38db0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="38db0-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38db0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38db0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38db0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38db0-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38db0-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38db0-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38db0-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="38db0-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="38db0-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38db0-138">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="38db0-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="38db0-139">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="38db0-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="38db0-140">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="38db0-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="38db0-141">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="38db0-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="38db0-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="38db0-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="38db0-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="38db0-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="38db0-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="38db0-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="38db0-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="38db0-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="38db0-146">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="38db0-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

