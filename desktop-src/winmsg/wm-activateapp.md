---
description: Inviato quando una finestra appartenente a un'applicazione diversa da quella della finestra attiva sta per essere attivata. Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Messaggio WM_ACTIVATEAPP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314880"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="1d85a-104">\_Messaggio ACTIVATEAPP WM</span><span class="sxs-lookup"><span data-stu-id="1d85a-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="1d85a-105">Inviato quando una finestra appartenente a un'applicazione diversa da quella della finestra attiva sta per essere attivata.</span><span class="sxs-lookup"><span data-stu-id="1d85a-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="1d85a-106">Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.</span><span class="sxs-lookup"><span data-stu-id="1d85a-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="1d85a-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d85a-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="1d85a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d85a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d85a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d85a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d85a-110">Indica se la finestra viene attivata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="1d85a-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="1d85a-111">Questo parametro è **true** se è in corso l'attivazione della finestra; è **false** se la finestra è in fase di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="1d85a-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="1d85a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d85a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d85a-113">Identificatore del thread.</span><span class="sxs-lookup"><span data-stu-id="1d85a-113">The thread identifier.</span></span> <span data-ttu-id="1d85a-114">Se il parametro *wParam* è **true**, *lParam* è l'identificatore del thread a cui appartiene la finestra da disattivare.</span><span class="sxs-lookup"><span data-stu-id="1d85a-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="1d85a-115">Se *wParam* è **false**, *lParam* è l'identificatore del thread a cui appartiene la finestra attivata.</span><span class="sxs-lookup"><span data-stu-id="1d85a-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d85a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d85a-116">Return value</span></span>

<span data-ttu-id="1d85a-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1d85a-117">Type: **LRESULT**</span></span>

<span data-ttu-id="1d85a-118">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="1d85a-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d85a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d85a-119">Requirements</span></span>



| <span data-ttu-id="1d85a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d85a-120">Requirement</span></span> | <span data-ttu-id="1d85a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1d85a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d85a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d85a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d85a-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d85a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1d85a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d85a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d85a-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d85a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d85a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d85a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d85a-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d85a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d85a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d85a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d85a-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1d85a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d85a-130">**\_attivazione WM**</span><span class="sxs-lookup"><span data-stu-id="1d85a-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="1d85a-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1d85a-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d85a-132">Windows</span><span class="sxs-lookup"><span data-stu-id="1d85a-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
