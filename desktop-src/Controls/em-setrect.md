---
title: EM_SETRECT messaggio (Winuser.h)
description: 'EM_SETRECT messaggio: imposta il rettangolo di formattazione di un controllo di modifica su più righe.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT messaggio Controlli Windows
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085969"
---
# <a name="em_setrect-message"></a><span data-ttu-id="4bd72-104">Messaggio \_ EM SETRECT</span><span class="sxs-lookup"><span data-stu-id="4bd72-104">EM\_SETRECT message</span></span>

<span data-ttu-id="4bd72-105">Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4bd72-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="4bd72-106">Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo.</span><span class="sxs-lookup"><span data-stu-id="4bd72-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="4bd72-107">Il rettangolo di limitazione è indipendente dalle dimensioni della finestra del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4bd72-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="4bd72-108">Questo messaggio viene elaborato solo dai controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4bd72-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="4bd72-109">È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4bd72-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bd72-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bd72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd72-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bd72-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd72-112">**Rich Edit 2.0 e versioni successive:** Indica se *lParam specifica* coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="4bd72-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="4bd72-113">Il valore zero indica le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="4bd72-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="4bd72-114">Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4bd72-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="4bd72-115">Gli offset possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="4bd72-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="4bd72-116">**Controlli di modifica e Rich Edit 1.0:** Questo parametro non viene usato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4bd72-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4bd72-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bd72-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd72-118">Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="4bd72-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="4bd72-119">Se questo parametro è **NULL,** il rettangolo di formattazione viene impostato su valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4bd72-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd72-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bd72-120">Return value</span></span>

<span data-ttu-id="4bd72-121">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4bd72-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd72-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bd72-122">Remarks</span></span>

<span data-ttu-id="4bd72-123">L'impostazione di *lParam* su **NULL** non ha alcun effetto se è installato un dispositivo touch o se **EM \_ SETRECT** viene inviato da un thread in cui è installato un hook (vedere [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="4bd72-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="4bd72-124">In questi casi, *lParam* deve contenere un puntatore valido a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4bd72-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="4bd72-125">Il **messaggio EM \_ SETRECT** fa sì che il testo del controllo di modifica venga ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="4bd72-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="4bd72-126">Per modificare le dimensioni del rettangolo di formattazione senza ridisegnare il testo, usare il [**messaggio EM \_ SETRECTNP.**](em-setrectnp.md)</span><span class="sxs-lookup"><span data-stu-id="4bd72-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="4bd72-127">Quando viene creato un controllo di modifica per la prima volta, il rettangolo di formattazione viene impostato su una dimensione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4bd72-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="4bd72-128">È possibile usare il **messaggio EM \_ SETRECT per** rendere il rettangolo di formattazione più grande o più piccolo della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4bd72-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="4bd72-129">Se il controllo di modifica non dispone di una barra di scorrimento orizzontale e il rettangolo di formattazione è impostato in modo da essere più grande della finestra del controllo di modifica, le righe di testo che superano la larghezza della finestra del controllo di modifica (ma inferiori alla larghezza del rettangolo di formattazione) vengono ritagliate anziché a capo.</span><span class="sxs-lookup"><span data-stu-id="4bd72-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="4bd72-130">Se il controllo di modifica contiene un bordo, il rettangolo di formattazione viene ridotto delle dimensioni del bordo.</span><span class="sxs-lookup"><span data-stu-id="4bd72-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="4bd72-131">Se si modifica il rettangolo restituito da un messaggio [**EM \_ GETRECT,**](em-getrect.md) è necessario rimuovere le dimensioni del bordo prima di usare il rettangolo con il **messaggio EM \_ SETRECT.**</span><span class="sxs-lookup"><span data-stu-id="4bd72-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="4bd72-132">**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4bd72-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4bd72-133">Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo.</span><span class="sxs-lookup"><span data-stu-id="4bd72-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="4bd72-134">Quando l'utente fa clic sulla barra di selezione, viene selezionata la riga corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4bd72-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="4bd72-135">Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="4bd72-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd72-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bd72-136">Requirements</span></span>



| <span data-ttu-id="4bd72-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd72-137">Requirement</span></span> | <span data-ttu-id="4bd72-138">Valore</span><span class="sxs-lookup"><span data-stu-id="4bd72-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd72-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bd72-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd72-140">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bd72-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4bd72-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bd72-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd72-142">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bd72-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4bd72-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bd72-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd72-144"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bd72-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd72-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bd72-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="4bd72-146">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4bd72-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4bd72-147">**EM \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="4bd72-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="4bd72-148">**EM \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="4bd72-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="4bd72-149">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4bd72-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4bd72-150">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4bd72-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

