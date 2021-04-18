---
title: Messaggio WM_GETDLGCODE (winuser. h)
description: Inviato alla routine della finestra associata a un controllo.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Finestre di dialogo WM_GETDLGCODE messaggio
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302083"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="b9941-104">\_Messaggio GETDLGCODE WM</span><span class="sxs-lookup"><span data-stu-id="b9941-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="b9941-105">Inviato alla routine della finestra associata a un controllo.</span><span class="sxs-lookup"><span data-stu-id="b9941-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="b9941-106">Per impostazione predefinita, il sistema gestisce tutti gli input da tastiera al controllo; il sistema interpreta determinati tipi di input da tastiera come tasti di spostamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b9941-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="b9941-107">Per eseguire l'override di questo comportamento predefinito, il controllo può rispondere al messaggio **WM \_ GETDLGCODE** per indicare i tipi di input che desidera elaborare.</span><span class="sxs-lookup"><span data-stu-id="b9941-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="b9941-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9941-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9941-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9941-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9941-110">Tasto virtuale, premuto dall'utente, che ha richiesto a Windows di emettere la notifica.</span><span class="sxs-lookup"><span data-stu-id="b9941-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="b9941-111">Il gestore deve gestire in modo selettivo queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="b9941-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="b9941-112">Ad esempio, il gestore potrebbe accettare ed elaborare **la \_ restituzione VK** , ma delegare la **\_ Scheda VK** alla finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="b9941-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="b9941-113">Per un elenco di valori, vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="b9941-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="b9941-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9941-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9941-115">Puntatore a una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) (o **null** se il sistema sta eseguendo una query).</span><span class="sxs-lookup"><span data-stu-id="b9941-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9941-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9941-116">Return value</span></span>

<span data-ttu-id="b9941-117">Il valore restituito è uno o più dei valori seguenti, che indica il tipo di input elaborato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9941-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="b9941-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9941-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="b9941-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9941-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9941-120"><dt>**DLGC \_ PULSANTE**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="b9941-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="b9941-121">Pulsante.</span><span class="sxs-lookup"><span data-stu-id="b9941-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="b9941-122"><dt>**DLGC \_**</dt> <dt>0x0010</dt> DEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="b9941-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="b9941-123">Pulsante di push predefinito.</span><span class="sxs-lookup"><span data-stu-id="b9941-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="b9941-124"><dt>**DLGC \_**</dt> <dt>0x0008</dt> HASSETSEL</span><span class="sxs-lookup"><span data-stu-id="b9941-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="b9941-125">[**Em \_ Messaggi SETSEL**](/windows/desktop/Controls/em-setsel) .</span><span class="sxs-lookup"><span data-stu-id="b9941-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b9941-126"><dt>**DLGC \_ RADIOBUTTON**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="b9941-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="b9941-127">Pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="b9941-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b9941-128"><dt>**DLGC \_**</dt> <dt>0x0100</dt> statico</span><span class="sxs-lookup"><span data-stu-id="b9941-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="b9941-129">Controllo statico.</span><span class="sxs-lookup"><span data-stu-id="b9941-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="b9941-130"><dt>**DLGC \_**</dt> <dt>0x0020</dt> UNDEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="b9941-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="b9941-131">Pulsante di push non predefinito.</span><span class="sxs-lookup"><span data-stu-id="b9941-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="b9941-132"><dt>**DLGC \_**</dt> <dt>0x0004</dt> WANTALLKEYS</span><span class="sxs-lookup"><span data-stu-id="b9941-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="b9941-133">Tutti gli input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="b9941-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="b9941-134"><dt>**DLGC \_**</dt> <dt>0x0001</dt> WANTARROWS</span><span class="sxs-lookup"><span data-stu-id="b9941-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="b9941-135">Tasti di direzione.</span><span class="sxs-lookup"><span data-stu-id="b9941-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="b9941-136"><dt>**DLGC \_**</dt> <dt>0x0080</dt> WANTCHARS</span><span class="sxs-lookup"><span data-stu-id="b9941-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="b9941-137">[**WM \_ Messaggi CHAR**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="b9941-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="b9941-138"><dt>**DLGC \_**</dt> <dt>0x0004</dt> WANTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="b9941-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="b9941-139">Tutti gli input da tastiera (l'applicazione passa questo messaggio nella struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) al controllo).</span><span class="sxs-lookup"><span data-stu-id="b9941-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="b9941-140"><dt>**DLGC \_**</dt> <dt>0x0002</dt> WANTTAB</span><span class="sxs-lookup"><span data-stu-id="b9941-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="b9941-141">Tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="b9941-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="b9941-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9941-142">Remarks</span></span>

<span data-ttu-id="b9941-143">Sebbene la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisca sempre zero in risposta al messaggio **WM \_ GETDLGCODE** , la routine della finestra per le classi di controlli predefinite restituisce un codice appropriato per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="b9941-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="b9941-144">Il messaggio **WM \_ GETDLGCODE** e i valori restituiti sono utili solo con i controlli della finestra di dialogo definiti dall'utente o i controlli standard modificati dalla sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="b9941-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9941-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9941-145">Requirements</span></span>



| <span data-ttu-id="b9941-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9941-146">Requirement</span></span> | <span data-ttu-id="b9941-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b9941-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9941-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9941-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b9941-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9941-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b9941-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9941-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b9941-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9941-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9941-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9941-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9941-153"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9941-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9941-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9941-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9941-155">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b9941-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9941-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b9941-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b9941-157">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="b9941-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="b9941-158">**MESSAGGIO**</span><span class="sxs-lookup"><span data-stu-id="b9941-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="b9941-159">**\_carattere WM**</span><span class="sxs-lookup"><span data-stu-id="b9941-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="b9941-160">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b9941-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9941-161">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="b9941-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

