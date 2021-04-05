---
title: Messaggio EM_SETRECT (winuser. h)
description: Imposta il rettangolo di formattazione di un controllo di modifica su più righe.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Controlli di Windows Message EM_SETRECT
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
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048301"
---
# <a name="em_setrect-message"></a><span data-ttu-id="4046b-104">\_Messaggio serect em</span><span class="sxs-lookup"><span data-stu-id="4046b-104">EM\_SETRECT message</span></span>

<span data-ttu-id="4046b-105">Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4046b-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="4046b-106">Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo.</span><span class="sxs-lookup"><span data-stu-id="4046b-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="4046b-107">Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4046b-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="4046b-108">Questo messaggio viene elaborato solo dai controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4046b-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="4046b-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4046b-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4046b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4046b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4046b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4046b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4046b-112">**Rich Edit 2,0 e versioni successive:** Indica se *lParam* specifica le coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="4046b-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="4046b-113">Un valore pari a zero indica le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="4046b-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="4046b-114">Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4046b-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="4046b-115">Gli offset possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="4046b-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="4046b-116">**Modificare i controlli e rich edit 1,0:** Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4046b-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4046b-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4046b-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4046b-118">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="4046b-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="4046b-119">Se questo parametro è **null**, il rettangolo di formattazione viene impostato sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4046b-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4046b-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4046b-120">Return value</span></span>

<span data-ttu-id="4046b-121">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4046b-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4046b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4046b-122">Remarks</span></span>

<span data-ttu-id="4046b-123">L'impostazione di *lParam* su **null** non produce alcun effetto se viene installato un dispositivo touch o se viene inviato **em \_ serect** da un thread con un hook installato (vedere [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="4046b-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="4046b-124">In questi casi, *lParam* deve contenere un puntatore valido a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4046b-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="4046b-125">Il **messaggio \_ serect em** causa il ridisegnato del testo del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4046b-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="4046b-126">Per modificare le dimensioni del rettangolo di formattazione senza ridisegnare il testo, usare il [**messaggio \_ SETRECTNP em**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="4046b-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="4046b-127">Quando un controllo di modifica viene creato per la prima volta, il rettangolo di formattazione viene impostato su una dimensione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4046b-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="4046b-128">È possibile utilizzare il **messaggio \_ serect em** per rendere il rettangolo di formattazione più grande o più piccolo della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4046b-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="4046b-129">Se il controllo di modifica non dispone di una barra di scorrimento orizzontale e il rettangolo di formattazione è impostato su un valore maggiore rispetto alla finestra di controllo di modifica, le righe di testo che superano la larghezza della finestra di controllo di modifica, ma inferiori rispetto alla larghezza del rettangolo di formattazione, vengono ritagliate invece di essere sottoposte a incapsulamento.</span><span class="sxs-lookup"><span data-stu-id="4046b-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="4046b-130">Se il controllo di modifica contiene un bordo, il rettangolo di formattazione viene ridotto in base alle dimensioni del bordo.</span><span class="sxs-lookup"><span data-stu-id="4046b-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="4046b-131">Se si sta modificando il rettangolo restituito da un messaggio [**\_ GetRect em**](em-getrect.md) , è necessario rimuovere le dimensioni del bordo prima di utilizzare il rettangolo con il messaggio **em \_ serect** .</span><span class="sxs-lookup"><span data-stu-id="4046b-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="4046b-132">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4046b-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4046b-133">Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo.</span><span class="sxs-lookup"><span data-stu-id="4046b-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="4046b-134">Quando l'utente fa clic sulla barra di selezione, viene selezionata la riga corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4046b-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="4046b-135">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4046b-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4046b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4046b-136">Requirements</span></span>



| <span data-ttu-id="4046b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4046b-137">Requirement</span></span> | <span data-ttu-id="4046b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="4046b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4046b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4046b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4046b-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4046b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4046b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4046b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4046b-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4046b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4046b-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4046b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4046b-144"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4046b-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4046b-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4046b-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="4046b-146">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4046b-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4046b-147">**GetRect EM \_**</span><span class="sxs-lookup"><span data-stu-id="4046b-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="4046b-148">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="4046b-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="4046b-149">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4046b-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4046b-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4046b-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

