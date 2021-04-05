---
description: Un'applicazione invia il \_ messaggio WM MDINEXT a una finestra del client di interfaccia a documenti multipli (MDI) per attivare la finestra figlio precedente o successiva.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Messaggio WM_MDINEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751207"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="aa118-103">\_Messaggio MDINEXT WM</span><span class="sxs-lookup"><span data-stu-id="aa118-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="aa118-104">Un'applicazione invia il messaggio **WM \_ MDINEXT** a una finestra del client di interfaccia a documenti multipli (MDI) per attivare la finestra figlio precedente o successiva.</span><span class="sxs-lookup"><span data-stu-id="aa118-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="aa118-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa118-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa118-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa118-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa118-107">Handle per la finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="aa118-107">A handle to the MDI child window.</span></span> <span data-ttu-id="aa118-108">Il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio specificata, a seconda del valore del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="aa118-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="aa118-109">Se il parametro *wParam* è **null**, il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="aa118-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="aa118-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa118-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa118-111">Se questo parametro è zero, il sistema attiva la finestra figlio MDI successiva e posiziona la finestra figlio identificata dal parametro *wParam* dietro tutte le altre finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="aa118-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="aa118-112">Se questo parametro è diverso da zero, il sistema attiva la finestra figlio precedente, inserendola davanti alla finestra figlio identificata da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="aa118-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa118-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa118-113">Return value</span></span>

<span data-ttu-id="aa118-114">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="aa118-114">Type: **zero**</span></span>

<span data-ttu-id="aa118-115">Il valore restituito è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="aa118-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa118-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa118-116">Remarks</span></span>

<span data-ttu-id="aa118-117">Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio MDI attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.</span><span class="sxs-lookup"><span data-stu-id="aa118-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa118-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa118-118">Requirements</span></span>



| <span data-ttu-id="aa118-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa118-119">Requirement</span></span> | <span data-ttu-id="aa118-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aa118-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa118-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa118-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa118-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa118-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aa118-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa118-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa118-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa118-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa118-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa118-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa118-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa118-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa118-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa118-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa118-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="aa118-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa118-129">**\_MDIACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="aa118-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="aa118-130">**\_MDIGETACTIVE WM**</span><span class="sxs-lookup"><span data-stu-id="aa118-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="aa118-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="aa118-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aa118-132">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="aa118-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




