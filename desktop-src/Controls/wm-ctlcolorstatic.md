---
title: Messaggio WM_CTLCOLORSTATIC (winuser. h)
description: Un controllo statico o un controllo di modifica che è di sola lettura o disabilitato invia il \_ messaggio CTLCOLORSTATIC WM alla relativa finestra padre quando il controllo sta per essere disegnato.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Controlli di Windows Message WM_CTLCOLORSTATIC
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741367"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="4e15f-104">\_Messaggio CTLCOLORSTATIC WM</span><span class="sxs-lookup"><span data-stu-id="4e15f-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="4e15f-105">Un controllo statico o un controllo di modifica che è di sola lettura o disabilitato invia il **messaggio \_ CTLCOLORSTATIC WM** alla relativa finestra padre quando il controllo sta per essere disegnato.</span><span class="sxs-lookup"><span data-stu-id="4e15f-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="4e15f-106">Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare i colori di primo piano e di sfondo del testo del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="4e15f-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="4e15f-107">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e15f-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4e15f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e15f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e15f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e15f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e15f-110">Handle per il contesto di dispositivo per la finestra del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="4e15f-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="4e15f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e15f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e15f-112">Handle per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="4e15f-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e15f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e15f-113">Return value</span></span>

<span data-ttu-id="4e15f-114">Se un'applicazione elabora il messaggio, il valore restituito è un handle per un pennello utilizzato dal sistema per disegnare lo sfondo del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="4e15f-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e15f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e15f-115">Remarks</span></span>

<span data-ttu-id="4e15f-116">Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="4e15f-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="4e15f-117">Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="4e15f-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="4e15f-118">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="4e15f-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="4e15f-119">È possibile impostare il colore di sfondo del testo di un controllo di modifica disabilitato, ma non è possibile impostare il colore di primo piano del testo.</span><span class="sxs-lookup"><span data-stu-id="4e15f-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="4e15f-120">Il sistema usa sempre il colore \_ GRAYTEXT.</span><span class="sxs-lookup"><span data-stu-id="4e15f-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="4e15f-121">I controlli di modifica che non sono di sola lettura o disabilitati non inviano il messaggio **WM \_ CTLCOLORSTATIC** , bensì inviano il messaggio [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="4e15f-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="4e15f-122">Il messaggio **WM \_ CTLCOLORSTATIC** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.</span><span class="sxs-lookup"><span data-stu-id="4e15f-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="4e15f-123">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="4e15f-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="4e15f-124">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="4e15f-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="4e15f-125">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4e15f-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="4e15f-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="4e15f-126">Examples</span></span>

<span data-ttu-id="4e15f-127">Nell'esempio C++ riportato di seguito viene illustrato come impostare i colori di primo piano e di sfondo del testo di un controllo statico in risposta al messaggio **WM \_ CTLCOLORSTATIC** .</span><span class="sxs-lookup"><span data-stu-id="4e15f-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="4e15f-128">La `hbrBkgnd` variabile è una variabile **HBRUSH** statica inizializzata su null e archivia il pennello di sfondo tra le chiamate a **WM \_ CTLCOLORSTATIC**.</span><span class="sxs-lookup"><span data-stu-id="4e15f-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="4e15f-129">Il pennello deve essere eliminato da una chiamata alla funzione [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) quando non è più necessario, in genere quando la finestra di dialogo associata viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="4e15f-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="4e15f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e15f-130">Requirements</span></span>



| <span data-ttu-id="4e15f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e15f-131">Requirement</span></span> | <span data-ttu-id="4e15f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4e15f-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e15f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e15f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4e15f-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e15f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e15f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e15f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4e15f-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e15f-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e15f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e15f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e15f-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e15f-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e15f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e15f-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e15f-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4e15f-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e15f-141">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="4e15f-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="4e15f-142">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="4e15f-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="4e15f-143">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="4e15f-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="4e15f-144">**\_CTLCOLORSCROLLBAR WM**</span><span class="sxs-lookup"><span data-stu-id="4e15f-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="4e15f-145">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4e15f-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4e15f-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="4e15f-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4e15f-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="4e15f-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4e15f-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="4e15f-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="4e15f-149">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="4e15f-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

