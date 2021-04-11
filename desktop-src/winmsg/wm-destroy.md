---
description: Inviato quando una finestra viene distrutta. Viene inviata alla routine della finestra che viene distrutta dopo la rimozione della finestra dallo schermo.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Messaggio WM_DESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232464"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="5946d-104">\_Messaggio WM Destroy</span><span class="sxs-lookup"><span data-stu-id="5946d-104">WM\_DESTROY message</span></span>

<span data-ttu-id="5946d-105">Inviato quando una finestra viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="5946d-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="5946d-106">Viene inviata alla routine della finestra che viene distrutta dopo la rimozione della finestra dallo schermo.</span><span class="sxs-lookup"><span data-stu-id="5946d-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="5946d-107">Questo messaggio viene inviato prima alla finestra distrutta e quindi alle finestre figlio (se presenti) distrutte.</span><span class="sxs-lookup"><span data-stu-id="5946d-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="5946d-108">Durante l'elaborazione del messaggio, è possibile presupporre che tutte le finestre figlio esistano ancora.</span><span class="sxs-lookup"><span data-stu-id="5946d-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="5946d-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5946d-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="5946d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5946d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5946d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5946d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5946d-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5946d-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5946d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5946d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5946d-114">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5946d-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5946d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5946d-115">Return value</span></span>

<span data-ttu-id="5946d-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5946d-116">Type: **LRESULT**</span></span>

<span data-ttu-id="5946d-117">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5946d-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5946d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5946d-118">Remarks</span></span>

<span data-ttu-id="5946d-119">Se la finestra distrutta fa parte della catena del visualizzatore degli Appunti (impostata chiamando la funzione [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la finestra deve rimuovere se stessa dalla catena elaborando la funzione [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) prima di restituire il messaggio **WM \_ Destroy** .</span><span class="sxs-lookup"><span data-stu-id="5946d-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5946d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5946d-120">Requirements</span></span>



| <span data-ttu-id="5946d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5946d-121">Requirement</span></span> | <span data-ttu-id="5946d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5946d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5946d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5946d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5946d-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5946d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5946d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5946d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5946d-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5946d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5946d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5946d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5946d-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5946d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5946d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5946d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5946d-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5946d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5946d-131">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="5946d-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="5946d-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="5946d-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="5946d-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="5946d-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="5946d-134">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="5946d-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="5946d-135">**\_chiusura WM**</span><span class="sxs-lookup"><span data-stu-id="5946d-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="5946d-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5946d-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5946d-137">Windows</span><span class="sxs-lookup"><span data-stu-id="5946d-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
