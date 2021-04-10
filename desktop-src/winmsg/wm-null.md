---
description: Non esegue alcuna operazione. Un'applicazione invia il \_ messaggio WM null se desidera pubblicare un messaggio che verrà ignorato dalla finestra del destinatario.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Messaggio WM_NULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231547"
---
# <a name="wm_null-message"></a><span data-ttu-id="9506b-104">\_Messaggio WM null</span><span class="sxs-lookup"><span data-stu-id="9506b-104">WM\_NULL message</span></span>

<span data-ttu-id="9506b-105">Non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="9506b-105">Performs no operation.</span></span> <span data-ttu-id="9506b-106">Un'applicazione invia il messaggio **WM \_ null** se desidera pubblicare un messaggio che verrà ignorato dalla finestra del destinatario.</span><span class="sxs-lookup"><span data-stu-id="9506b-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="9506b-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9506b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="9506b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9506b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9506b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9506b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9506b-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="9506b-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9506b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9506b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9506b-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="9506b-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9506b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9506b-113">Return value</span></span>

<span data-ttu-id="9506b-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9506b-114">Type: **LRESULT**</span></span>

<span data-ttu-id="9506b-115">Un'applicazione restituisce zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9506b-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9506b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9506b-116">Remarks</span></span>

<span data-ttu-id="9506b-117">Ad esempio, se un'applicazione ha installato un hook di **WH \_ GetMessage** e vuole impedire l'elaborazione di un messaggio, la funzione di callback [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) può modificare il numero del messaggio in **WM \_ null** , in modo che il destinatario lo ignorerà.</span><span class="sxs-lookup"><span data-stu-id="9506b-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="9506b-118">Un altro esempio è che un'applicazione può verificare se una finestra sta rispondendo ai messaggi inviando il messaggio **WM \_ null** con la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="9506b-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9506b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9506b-119">Requirements</span></span>



| <span data-ttu-id="9506b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9506b-120">Requirement</span></span> | <span data-ttu-id="9506b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9506b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9506b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9506b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9506b-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9506b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9506b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9506b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9506b-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9506b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9506b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9506b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9506b-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9506b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9506b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9506b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9506b-129">Panoramica di Windows</span><span class="sxs-lookup"><span data-stu-id="9506b-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
