---
description: Inviato per annullare determinate modalità, ad esempio l'acquisizione del mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Messaggio WM_CANCELMODE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314874"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="8f878-103">\_Messaggio CANCELMODE WM</span><span class="sxs-lookup"><span data-stu-id="8f878-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="8f878-104">Inviato per annullare determinate modalità, ad esempio l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="8f878-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="8f878-105">Ad esempio, il sistema invia questo messaggio alla finestra attiva quando viene visualizzata una finestra di dialogo o una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="8f878-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="8f878-106">Alcune funzioni inviano inoltre questo messaggio in modo esplicito alla finestra specificata, indipendentemente dal fatto che sia la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="8f878-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="8f878-107">Ad esempio, la funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) Invia questo messaggio quando si disabilita la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="8f878-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="8f878-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f878-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="8f878-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f878-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f878-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f878-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f878-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="8f878-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f878-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f878-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f878-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="8f878-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f878-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f878-114">Return value</span></span>

<span data-ttu-id="8f878-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8f878-115">Type: **LRESULT**</span></span>

<span data-ttu-id="8f878-116">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="8f878-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f878-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f878-117">Remarks</span></span>

<span data-ttu-id="8f878-118">Quando viene inviato il messaggio **WM \_ CANCELMODE** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Annulla l'elaborazione interna dell'input della barra di scorrimento standard, Annulla l'elaborazione interna dei menu e rilascia l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="8f878-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f878-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f878-119">Requirements</span></span>



| <span data-ttu-id="8f878-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f878-120">Requirement</span></span> | <span data-ttu-id="8f878-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8f878-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f878-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f878-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f878-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f878-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8f878-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f878-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f878-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f878-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f878-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f878-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f878-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f878-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f878-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f878-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f878-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8f878-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f878-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8f878-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8f878-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="8f878-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="8f878-132">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="8f878-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="8f878-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8f878-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f878-134">Windows</span><span class="sxs-lookup"><span data-stu-id="8f878-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
