---
title: Messaggio WM_CTLCOLORBTN (winuser. h)
description: Il \_ messaggio WM CTLCOLORBTN viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo del pulsante e i colori di sfondo. Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora questo messaggio.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Controlli di Windows Message WM_CTLCOLORBTN
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963749"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="93e52-106">\_Messaggio CTLCOLORBTN WM</span><span class="sxs-lookup"><span data-stu-id="93e52-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="93e52-107">Il messaggio **WM \_ CTLCOLORBTN** viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante.</span><span class="sxs-lookup"><span data-stu-id="93e52-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="93e52-108">La finestra padre può modificare il testo del pulsante e i colori di sfondo.</span><span class="sxs-lookup"><span data-stu-id="93e52-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="93e52-109">Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="93e52-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="93e52-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="93e52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e52-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93e52-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e52-112">**HDC** che specifica l'handle per il contesto di visualizzazione per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="93e52-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="93e52-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93e52-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e52-114">**HWND** che specifica l'handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="93e52-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e52-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93e52-115">Return value</span></span>

<span data-ttu-id="93e52-116">Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello.</span><span class="sxs-lookup"><span data-stu-id="93e52-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="93e52-117">Il sistema utilizza il pennello per disegnare lo sfondo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="93e52-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e52-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="93e52-118">Remarks</span></span>

<span data-ttu-id="93e52-119">Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="93e52-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="93e52-120">Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.</span><span class="sxs-lookup"><span data-stu-id="93e52-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="93e52-121">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="93e52-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="93e52-122">[**I pulsanti con lo stile \_ BS**](button-styles.md)Button, [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) non utilizzano il pennello restituito.</span><span class="sxs-lookup"><span data-stu-id="93e52-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="93e52-123">I pulsanti con questi stili vengono sempre disegnati con i colori di sistema predefiniti.</span><span class="sxs-lookup"><span data-stu-id="93e52-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="93e52-124">Il disegno dei pulsanti di push richiede diversi pennelli: faccia, evidenziazione e ombreggiatura, ma il messaggio **WM \_ CTLCOLORBTN** consente la restituzione di un solo pennello.</span><span class="sxs-lookup"><span data-stu-id="93e52-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="93e52-125">Per fornire un aspetto personalizzato per i pulsanti di push, utilizzare un pulsante creato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="93e52-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="93e52-126">Per ulteriori informazioni, vedere [creazione di controlli Owner-Drawn](user-controls-intro.md).</span><span class="sxs-lookup"><span data-stu-id="93e52-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="93e52-127">Il messaggio **WM \_ CTLCOLORBTN** non viene mai inviato tra i thread.</span><span class="sxs-lookup"><span data-stu-id="93e52-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="93e52-128">Viene inviato solo all'interno di un thread.</span><span class="sxs-lookup"><span data-stu-id="93e52-128">It is sent only within one thread.</span></span>

<span data-ttu-id="93e52-129">Il colore del testo di una casella di controllo o di un pulsante di opzione si applica alla casella o al pulsante, al segno di spunta e al testo.</span><span class="sxs-lookup"><span data-stu-id="93e52-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="93e52-130">Il rettangolo di attivazione per questi pulsanti rimane il colore predefinito del sistema (in genere nero).</span><span class="sxs-lookup"><span data-stu-id="93e52-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="93e52-131">Il colore del testo di una casella di gruppo si applica al testo ma non alla riga che definisce la casella.</span><span class="sxs-lookup"><span data-stu-id="93e52-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="93e52-132">Il colore del testo di un pulsante di push si applica solo al relativo rettangolo di attivazione; non influisce sul colore del testo.</span><span class="sxs-lookup"><span data-stu-id="93e52-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="93e52-133">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="93e52-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="93e52-134">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="93e52-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="93e52-135">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="93e52-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e52-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93e52-136">Requirements</span></span>



| <span data-ttu-id="93e52-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e52-137">Requirement</span></span> | <span data-ttu-id="93e52-138">Valore</span><span class="sxs-lookup"><span data-stu-id="93e52-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e52-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93e52-139">Minimum supported client</span></span><br/> | <span data-ttu-id="93e52-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93e52-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93e52-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93e52-141">Minimum supported server</span></span><br/> | <span data-ttu-id="93e52-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93e52-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93e52-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93e52-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e52-144"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e52-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e52-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93e52-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="93e52-146">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="93e52-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="93e52-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="93e52-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="93e52-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="93e52-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

