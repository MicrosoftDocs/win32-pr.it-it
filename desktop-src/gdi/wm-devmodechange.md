---
description: Il \_ messaggio WM DEVMODECHANGE viene inviato a tutte le finestre di primo livello ogni volta che l'utente modifica le impostazioni della modalità dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Messaggio WM_DEVMODECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980290"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="235b1-103">\_Messaggio DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="235b1-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="235b1-104">Il messaggio **WM \_ DEVMODECHANGE** viene inviato a tutte le finestre di primo livello ogni volta che l'utente modifica le impostazioni della modalità dispositivo.</span><span class="sxs-lookup"><span data-stu-id="235b1-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="235b1-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="235b1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="235b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="235b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235b1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="235b1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="235b1-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="235b1-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="235b1-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="235b1-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="235b1-110">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="235b1-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="235b1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="235b1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="235b1-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="235b1-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="235b1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="235b1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="235b1-114">Puntatore a una stringa che specifica il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="235b1-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235b1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="235b1-115">Return value</span></span>

<span data-ttu-id="235b1-116">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="235b1-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="235b1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="235b1-117">Remarks</span></span>

<span data-ttu-id="235b1-118">Impossibile inviare questo messaggio direttamente a una finestra.</span><span class="sxs-lookup"><span data-stu-id="235b1-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="235b1-119">Per inviare il messaggio **WM \_ DEVMODECHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con il parametro *HWND* impostato su HWND \_ broadcast.</span><span class="sxs-lookup"><span data-stu-id="235b1-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="235b1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="235b1-120">Requirements</span></span>



| <span data-ttu-id="235b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="235b1-121">Requirement</span></span> | <span data-ttu-id="235b1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="235b1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="235b1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="235b1-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="235b1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="235b1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="235b1-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="235b1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="235b1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="235b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="235b1-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="235b1-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235b1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="235b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235b1-130">Panoramica dei contesti di dispositivo</span><span class="sxs-lookup"><span data-stu-id="235b1-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="235b1-131">Messaggi di contesto dispositivo</span><span class="sxs-lookup"><span data-stu-id="235b1-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
