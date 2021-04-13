---
title: Messaggio WM_NEXTDLGCTL (winuser. h)
description: Inviato a una procedura della finestra di dialogo per impostare lo stato attivo su un altro controllo nella finestra di dialogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Finestre di dialogo WM_NEXTDLGCTL messaggio
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518345"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="27996-104">\_Messaggio NEXTDLGCTL WM</span><span class="sxs-lookup"><span data-stu-id="27996-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="27996-105">Inviato a una procedura della finestra di dialogo per impostare lo stato attivo su un altro controllo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="27996-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="27996-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27996-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27996-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27996-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27996-108">Se *lParam* è **true**, questo parametro identifica il controllo che riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="27996-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="27996-109">Se *lParam* è **false**, questo parametro indica se il controllo successivo o precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="27996-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="27996-110">Se *wParam* è zero, il controllo successivo riceve lo stato attivo; in caso contrario, il controllo precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="27996-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="27996-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27996-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27996-112">La parola più bassa indica il modo in cui il sistema usa *wParam*.</span><span class="sxs-lookup"><span data-stu-id="27996-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="27996-113">Se la parola di ordine inferiore è **true**, *wParam* è un handle associato al controllo che riceve lo stato attivo; in caso contrario, *wParam* è un flag che indica se il controllo successivo o precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="27996-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27996-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27996-114">Return value</span></span>

<span data-ttu-id="27996-115">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="27996-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="27996-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="27996-116">Remarks</span></span>

<span data-ttu-id="27996-117">Questo messaggio esegue ulteriori operazioni di gestione della finestra di dialogo oltre a quelle eseguite dalla funzione di [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** aggiorna il bordo predefinito del pulsante, imposta l'identificatore di controllo predefinito e seleziona automaticamente il testo di un controllo di modifica (se la finestra di destinazione è un controllo di modifica).</span><span class="sxs-lookup"><span data-stu-id="27996-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="27996-118">Non utilizzare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per inviare un messaggio **WM \_ NEXTDLGCTL** se l'applicazione elaborerà simultaneamente altri messaggi che impostano lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="27996-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="27996-119">Usare invece la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="27996-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="27996-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27996-120">Requirements</span></span>



| <span data-ttu-id="27996-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="27996-121">Requirement</span></span> | <span data-ttu-id="27996-122">Valore</span><span class="sxs-lookup"><span data-stu-id="27996-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27996-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27996-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27996-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27996-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="27996-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27996-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27996-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27996-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27996-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27996-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="27996-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27996-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27996-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27996-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="27996-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="27996-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="27996-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="27996-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="27996-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="27996-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="27996-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="27996-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="27996-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="27996-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="27996-135">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="27996-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

