---
title: Messaggio WM_SETHOTKEY (winuser. h)
description: Inviato a una finestra per associare un tasto di scelta con la finestra. Quando l'utente preme il tasto di scelta, il sistema attiva la finestra.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Input della tastiera e del mouse WM_SETHOTKEY messaggio
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761513"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="ee675-105">\_Messaggio di SEHOTKEY WM</span><span class="sxs-lookup"><span data-stu-id="ee675-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="ee675-106">Inviato a una finestra per associare un tasto di scelta con la finestra.</span><span class="sxs-lookup"><span data-stu-id="ee675-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="ee675-107">Quando l'utente preme il tasto di scelta, il sistema attiva la finestra.</span><span class="sxs-lookup"><span data-stu-id="ee675-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="ee675-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee675-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee675-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee675-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee675-110">La parola di ordine inferiore specifica il codice della chiave virtuale da associare alla finestra.</span><span class="sxs-lookup"><span data-stu-id="ee675-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="ee675-111">La parola più significativa può essere uno o più dei seguenti valori di CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="ee675-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="ee675-112">L'impostazione di *wParam* su **null** rimuove il tasto di scelta associato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="ee675-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="ee675-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ee675-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="ee675-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ee675-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="ee675-115"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="ee675-116">ALT (tasto)</span><span class="sxs-lookup"><span data-stu-id="ee675-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="ee675-117"><dt>**HOTKEYF \_**</dt> <dt>0x02</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="ee675-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="ee675-118">Tasto CTRL</span><span class="sxs-lookup"><span data-stu-id="ee675-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="ee675-119"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> EXT</span><span class="sxs-lookup"><span data-stu-id="ee675-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="ee675-120">Chiave estesa</span><span class="sxs-lookup"><span data-stu-id="ee675-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="ee675-121"><dt>**HOTKEYF \_ MAIUSC**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="ee675-122">Tasto MAIUSC</span><span class="sxs-lookup"><span data-stu-id="ee675-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="ee675-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee675-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee675-124">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="ee675-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee675-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee675-125">Return value</span></span>

<span data-ttu-id="ee675-126">Il valore restituito è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee675-126">The return value is one of the following.</span></span>



| <span data-ttu-id="ee675-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee675-127">Return value</span></span>                                                                  | <span data-ttu-id="ee675-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee675-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee675-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="ee675-130">La funzione ha esito negativo. il tasto di scelta non è valido.</span><span class="sxs-lookup"><span data-stu-id="ee675-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="ee675-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="ee675-132">La funzione ha esito negativo. la finestra non è valida.</span><span class="sxs-lookup"><span data-stu-id="ee675-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="ee675-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="ee675-134">La funzione ha esito positivo e nessun'altra finestra ha lo stesso tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="ee675-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="ee675-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="ee675-136">La funzione ha esito positivo, ma un'altra finestra ha già lo stesso tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="ee675-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee675-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee675-137">Remarks</span></span>

<span data-ttu-id="ee675-138">Impossibile associare un tasto di scelta a una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="ee675-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="ee675-139">**VK \_** Il carattere di escape, **\_ lo spazio VK** e la **\_ Scheda VK** sono tasti di scelta rapida non validi.</span><span class="sxs-lookup"><span data-stu-id="ee675-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="ee675-140">Quando l'utente preme il tasto di scelta, il sistema genera un [**messaggio \_ WM SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) con *wParam* uguale a **SC \_ HotKey** e *lParam* uguale all'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee675-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="ee675-141">Se questo messaggio viene passato a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), il sistema visualizzerà l'ultimo popup attivo della finestra (se esistente) o la finestra stessa (se non è presente alcuna finestra popup) in primo piano.</span><span class="sxs-lookup"><span data-stu-id="ee675-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="ee675-142">Una finestra può avere solo un tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="ee675-142">A window can only have one hot key.</span></span> <span data-ttu-id="ee675-143">Se alla finestra è già associato un tasto di scelta, il nuovo tasto di scelta sostituisce quello precedente.</span><span class="sxs-lookup"><span data-stu-id="ee675-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="ee675-144">Se più di una finestra ha lo stesso tasto di scelta, la finestra attivata dal tasto di scelta è casuale.</span><span class="sxs-lookup"><span data-stu-id="ee675-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="ee675-145">Questi tasti di scelta rapida non sono correlati ai tasti di scelta rapida impostati da [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span><span class="sxs-lookup"><span data-stu-id="ee675-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee675-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee675-146">Requirements</span></span>



| <span data-ttu-id="ee675-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee675-147">Requirement</span></span> | <span data-ttu-id="ee675-148">Valore</span><span class="sxs-lookup"><span data-stu-id="ee675-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee675-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee675-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ee675-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee675-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ee675-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee675-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ee675-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee675-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee675-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee675-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee675-154"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee675-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee675-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee675-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee675-156">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ee675-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee675-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="ee675-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="ee675-158">**WM \_ GEThotkey**</span><span class="sxs-lookup"><span data-stu-id="ee675-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="ee675-159">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="ee675-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="ee675-160">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ee675-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee675-161">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="ee675-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

