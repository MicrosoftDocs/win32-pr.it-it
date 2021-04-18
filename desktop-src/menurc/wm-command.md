---
title: Messaggio WM_COMMAND (winuser. h)
description: Inviato quando l'utente seleziona un elemento di comando da un menu, quando un controllo Invia un messaggio di notifica alla relativa finestra padre o quando viene convertita una sequenza di tasti di scelta rapida.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- Menu del messaggio WM_COMMAND e altre risorse
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330436"
---
# <a name="wm_command-message"></a><span data-ttu-id="e9d85-104">\_Messaggio di comando WM</span><span class="sxs-lookup"><span data-stu-id="e9d85-104">WM\_COMMAND message</span></span>

<span data-ttu-id="e9d85-105">Inviato quando l'utente seleziona un elemento di comando da un menu, quando un controllo Invia un messaggio di notifica alla relativa finestra padre o quando viene convertita una sequenza di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e9d85-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="e9d85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9d85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9d85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d85-108">Per una descrizione di questo parametro, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e9d85-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e9d85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9d85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d85-110">Per una descrizione di questo parametro, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e9d85-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d85-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9d85-111">Return value</span></span>

<span data-ttu-id="e9d85-112">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e9d85-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="e9d85-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="e9d85-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="e9d85-114">Esempio tratto da [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="e9d85-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="e9d85-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9d85-115">Remarks</span></span>

<span data-ttu-id="e9d85-116">L'uso dei parametri *wParam* e *lParam* è riepilogato qui.</span><span class="sxs-lookup"><span data-stu-id="e9d85-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="e9d85-117">Origine messaggio</span><span class="sxs-lookup"><span data-stu-id="e9d85-117">Message Source</span></span> | <span data-ttu-id="e9d85-118">wParam (parola alta)</span><span class="sxs-lookup"><span data-stu-id="e9d85-118">wParam (high word)</span></span>                | <span data-ttu-id="e9d85-119">wParam (parola bassa)</span><span class="sxs-lookup"><span data-stu-id="e9d85-119">wParam (low word)</span></span>                | <span data-ttu-id="e9d85-120">lParam</span><span class="sxs-lookup"><span data-stu-id="e9d85-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="e9d85-121">Menu</span><span class="sxs-lookup"><span data-stu-id="e9d85-121">Menu</span></span>           | <span data-ttu-id="e9d85-122">0</span><span class="sxs-lookup"><span data-stu-id="e9d85-122">0</span></span>                                 | <span data-ttu-id="e9d85-123">Identificatore menu (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="e9d85-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="e9d85-124">0</span><span class="sxs-lookup"><span data-stu-id="e9d85-124">0</span></span>                            |
| <span data-ttu-id="e9d85-125">Acceleratore</span><span class="sxs-lookup"><span data-stu-id="e9d85-125">Accelerator</span></span>    | <span data-ttu-id="e9d85-126">1</span><span class="sxs-lookup"><span data-stu-id="e9d85-126">1</span></span>                                 | <span data-ttu-id="e9d85-127">Identificatore acceleratore (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="e9d85-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="e9d85-128">0</span><span class="sxs-lookup"><span data-stu-id="e9d85-128">0</span></span>                            |
| <span data-ttu-id="e9d85-129">Control</span><span class="sxs-lookup"><span data-stu-id="e9d85-129">Control</span></span>        | <span data-ttu-id="e9d85-130">Codice di notifica definito dal controllo</span><span class="sxs-lookup"><span data-stu-id="e9d85-130">Control-defined notification code</span></span> | <span data-ttu-id="e9d85-131">Identificatore di controllo</span><span class="sxs-lookup"><span data-stu-id="e9d85-131">Control identifier</span></span>               | <span data-ttu-id="e9d85-132">Handle per la finestra di controllo</span><span class="sxs-lookup"><span data-stu-id="e9d85-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="e9d85-133">Menu</span><span class="sxs-lookup"><span data-stu-id="e9d85-133">Menus</span></span>

<span data-ttu-id="e9d85-134">Se un'applicazione Abilita un separatore di menu, il sistema invia un messaggio di **\_ comando WM** con la parola bassa del parametro *wParam* impostato su zero quando l'utente seleziona il separatore.</span><span class="sxs-lookup"><span data-stu-id="e9d85-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="e9d85-135">Se un menu viene definito con un valore [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) di **MNS \_ NOTIFYBYPOS**, viene inviato [**WM \_ MENUCOMMAND**](wm-menucommand.md) anziché il **\_ comando WM**.</span><span class="sxs-lookup"><span data-stu-id="e9d85-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="e9d85-136">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e9d85-136">Accelerators</span></span>

<span data-ttu-id="e9d85-137">Le sequenze di tasti dell'acceleratore che selezionano gli elementi dal menu finestra vengono convertite in messaggi [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d85-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="e9d85-138">Se si verifica una sequenza di tasti di scelta rapida che corrisponde a una voce di menu quando la finestra proprietaria del menu è ridotta a icona, non viene inviato alcun messaggio di **\_ comando WM** .</span><span class="sxs-lookup"><span data-stu-id="e9d85-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="e9d85-139">Tuttavia, se si verifica una sequenza di tasti di scelta rapida che non corrisponde ad alcuno degli elementi nel menu della finestra o nel menu finestra, viene inviato un messaggio di **\_ comando WM** , anche se la finestra è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="e9d85-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d85-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9d85-140">Requirements</span></span>



| <span data-ttu-id="e9d85-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9d85-141">Requirement</span></span> | <span data-ttu-id="e9d85-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e9d85-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d85-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9d85-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d85-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9d85-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9d85-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9d85-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d85-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9d85-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9d85-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9d85-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9d85-148"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d85-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d85-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9d85-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9d85-150">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e9d85-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="e9d85-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9d85-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e9d85-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9d85-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e9d85-153">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e9d85-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9d85-154">Menu</span><span class="sxs-lookup"><span data-stu-id="e9d85-154">Menus</span></span>](menus.md)
</dt> </dl>

 

