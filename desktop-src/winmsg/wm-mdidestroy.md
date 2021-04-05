---
description: Un'applicazione invia il \_ messaggio WM MDIDESTROY a una finestra del client di interfaccia a documenti multipli (MDI) per chiudere una finestra figlio MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Messaggio WM_MDIDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751210"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="6c1ea-103">\_Messaggio MDIDESTROY WM</span><span class="sxs-lookup"><span data-stu-id="6c1ea-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="6c1ea-104">Un'applicazione invia il messaggio **WM \_ MDIDESTROY** a una finestra del client di interfaccia a documenti multipli (MDI) per chiudere una finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="6c1ea-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c1ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1ea-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c1ea-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1ea-107">Handle per la finestra figlio MDI da chiudere.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="6c1ea-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c1ea-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1ea-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1ea-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c1ea-110">Return value</span></span>

<span data-ttu-id="6c1ea-111">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="6c1ea-111">Type: **zero**</span></span>

<span data-ttu-id="6c1ea-112">Questo messaggio restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1ea-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c1ea-113">Remarks</span></span>

<span data-ttu-id="6c1ea-114">Questo messaggio rimuove il titolo della finestra figlio MDI dalla finestra cornice MDI e disattiva la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="6c1ea-115">Per chiudere tutte le finestre figlio MDI, un'applicazione deve utilizzare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="6c1ea-116">Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio e la finestra figlio MDI attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.</span><span class="sxs-lookup"><span data-stu-id="6c1ea-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1ea-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c1ea-117">Requirements</span></span>



| <span data-ttu-id="6c1ea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c1ea-118">Requirement</span></span> | <span data-ttu-id="6c1ea-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6c1ea-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1ea-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c1ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1ea-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c1ea-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c1ea-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c1ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1ea-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c1ea-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c1ea-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c1ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1ea-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c1ea-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c1ea-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c1ea-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c1ea-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6c1ea-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c1ea-128">**\_MDICREATE WM**</span><span class="sxs-lookup"><span data-stu-id="6c1ea-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="6c1ea-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6c1ea-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c1ea-130">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="6c1ea-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




