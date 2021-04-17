---
title: Messaggio WM_CTLCOLOREDIT (winuser. h)
description: Un controllo di modifica che non è di sola lettura o disabilitato invia il \_ messaggio WM CTLCOLOREDIT alla relativa finestra padre quando il controllo sta per essere disegnato.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Controlli di Windows Message WM_CTLCOLOREDIT
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475112"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="c066a-104">\_Messaggio CTLCOLOREDIT WM</span><span class="sxs-lookup"><span data-stu-id="c066a-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="c066a-105">Un controllo di modifica che non è di sola lettura o disabilitato invia il messaggio **WM \_ CTLCOLOREDIT** alla relativa finestra padre quando il controllo sta per essere disegnato.</span><span class="sxs-lookup"><span data-stu-id="c066a-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="c066a-106">Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare il testo e i colori di sfondo del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c066a-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c066a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c066a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c066a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c066a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c066a-109">Handle per il contesto di dispositivo per la finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c066a-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="c066a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c066a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c066a-111">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c066a-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c066a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c066a-112">Return value</span></span>

<span data-ttu-id="c066a-113">Se un'applicazione elabora il messaggio, deve restituire l'handle di un pennello.</span><span class="sxs-lookup"><span data-stu-id="c066a-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="c066a-114">Il sistema utilizza il pennello per disegnare lo sfondo del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c066a-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c066a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c066a-115">Remarks</span></span>

<span data-ttu-id="c066a-116">Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="c066a-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="c066a-117">Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="c066a-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="c066a-118">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c066a-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="c066a-119">I controlli di modifica di sola lettura o disabilitato non inviano il messaggio **WM \_ CTLCOLOREDIT** , bensì inviano il messaggio [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .</span><span class="sxs-lookup"><span data-stu-id="c066a-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="c066a-120">Il messaggio **WM \_ CTLCOLOREDIT** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.</span><span class="sxs-lookup"><span data-stu-id="c066a-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="c066a-121">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="c066a-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="c066a-122">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="c066a-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="c066a-123">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c066a-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="c066a-124">**Modifica avanzata:** Questo messaggio non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c066a-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="c066a-125">Per impostare il colore di sfondo per un controllo Rich Edit, utilizzare il messaggio [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c066a-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c066a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c066a-126">Requirements</span></span>



| <span data-ttu-id="c066a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c066a-127">Requirement</span></span> | <span data-ttu-id="c066a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c066a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c066a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c066a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c066a-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c066a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c066a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c066a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c066a-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c066a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c066a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c066a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c066a-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c066a-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c066a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c066a-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c066a-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c066a-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c066a-137">**\_SETBKGNDCOLOR em**</span><span class="sxs-lookup"><span data-stu-id="c066a-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="c066a-138">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="c066a-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="c066a-139">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c066a-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c066a-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c066a-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c066a-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="c066a-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="c066a-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="c066a-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

