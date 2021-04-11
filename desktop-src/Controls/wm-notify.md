---
title: Messaggio WM_NOTIFY (winuser. h)
description: Inviato da un controllo comune alla relativa finestra padre quando si verifica un evento oppure il controllo richiede alcune informazioni.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Controlli di Windows Message WM_NOTIFY
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964463"
---
# <a name="wm_notify-message"></a><span data-ttu-id="2528f-104">\_Messaggio di notifica WM</span><span class="sxs-lookup"><span data-stu-id="2528f-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="2528f-105">Inviato da un controllo comune alla relativa finestra padre quando si verifica un evento oppure il controllo richiede alcune informazioni.</span><span class="sxs-lookup"><span data-stu-id="2528f-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="2528f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2528f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2528f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2528f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2528f-108">Identificatore del controllo comune che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2528f-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="2528f-109">Questo identificatore non è necessariamente univoco.</span><span class="sxs-lookup"><span data-stu-id="2528f-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="2528f-110">Per identificare il controllo, un'applicazione deve usare il membro **hwndFrom** o **IdFrom** della struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , passata come parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2528f-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="2528f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2528f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2528f-112">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene il codice di notifica e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="2528f-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="2528f-113">Per alcuni messaggi di notifica, questo parametro punta a una struttura più ampia con la struttura **NMHDR** come primo membro.</span><span class="sxs-lookup"><span data-stu-id="2528f-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2528f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2528f-114">Return value</span></span>

<span data-ttu-id="2528f-115">Il valore restituito viene ignorato tranne che per i messaggi di notifica che specificano in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2528f-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2528f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2528f-116">Remarks</span></span>

<span data-ttu-id="2528f-117">La destinazione del messaggio deve essere **HWND** dell'elemento padre del controllo.</span><span class="sxs-lookup"><span data-stu-id="2528f-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="2528f-118">Questo valore può essere ottenuto tramite [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), come illustrato nell'esempio seguente, dove *m \_ controlHwnd* è l' **HWND** del controllo stesso.</span><span class="sxs-lookup"><span data-stu-id="2528f-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="2528f-119">Le applicazioni gestiscono il messaggio nella procedura della finestra padre, come illustrato nell'esempio seguente, che gestisce il messaggio di notifica inviato dal controllo personalizzato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="2528f-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="2528f-120">Alcune notifiche, principalmente quelle che sono state nell'API per molto tempo, vengono inviate come messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2528f-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="2528f-121">Per ulteriori informazioni, vedere [Control Messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2528f-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="2528f-122">Se il gestore di messaggi si trova in una routine della finestra di dialogo, è necessario utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT per impostare un valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2528f-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="2528f-123">Per i sistemi Windows Vista e versioni successive, non è possibile inviare il messaggio di **\_ notifica WM** tra i processi.</span><span class="sxs-lookup"><span data-stu-id="2528f-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="2528f-124">Molte notifiche sono disponibili nei formati ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="2528f-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="2528f-125">La finestra che invia il messaggio di **\_ notifica WM** usa il messaggio [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) per determinare il formato da usare.</span><span class="sxs-lookup"><span data-stu-id="2528f-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="2528f-126">Per ulteriori informazioni, vedere **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="2528f-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="2528f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2528f-127">Requirements</span></span>



| <span data-ttu-id="2528f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2528f-128">Requirement</span></span> | <span data-ttu-id="2528f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2528f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2528f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2528f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2528f-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2528f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2528f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2528f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2528f-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2528f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2528f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2528f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2528f-135"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2528f-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2528f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2528f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2528f-137">**\_NOTIFYFORMAT WM**</span><span class="sxs-lookup"><span data-stu-id="2528f-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

