---
description: Un'applicazione invia il \_ messaggio WM MDICREATE a una finestra del client di interfaccia a documenti multipli (MDI) per creare una finestra figlio MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Messaggio WM_MDICREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314863"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="46819-103">\_Messaggio MDICREATE WM</span><span class="sxs-lookup"><span data-stu-id="46819-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="46819-104">Un'applicazione invia il messaggio **WM \_ MDICREATE** a una finestra del client di interfaccia a documenti multipli (MDI) per creare una finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="46819-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="46819-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="46819-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46819-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46819-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46819-107">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="46819-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="46819-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46819-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46819-109">Puntatore a una struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) contenente le informazioni utilizzate dal sistema per creare la finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="46819-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46819-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46819-110">Return value</span></span>

<span data-ttu-id="46819-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="46819-111">Type: **HWND**</span></span>

<span data-ttu-id="46819-112">Se il messaggio ha esito positivo, il valore restituito è l'handle per la nuova finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="46819-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="46819-113">Se il messaggio ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="46819-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46819-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="46819-114">Remarks</span></span>

<span data-ttu-id="46819-115">La finestra figlio MDI viene creata con i bit di [**stile della finestra**](window-styles.md) **WS \_ child**, **WS \_ CLIPSIBLINGS**, WS **\_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** e **WS \_ MAXIMIZEBOX**, più altri bit di stile specificati nella struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="46819-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="46819-116">Il sistema aggiunge il titolo della nuova finestra figlio al menu finestra della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="46819-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="46819-117">Un'applicazione deve usare questo messaggio per creare tutte le finestre figlio della finestra client.</span><span class="sxs-lookup"><span data-stu-id="46819-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="46819-118">Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.</span><span class="sxs-lookup"><span data-stu-id="46819-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="46819-119">Quando viene creata una finestra figlio MDI, il sistema invia il messaggio [**WM \_ create**](wm-create.md) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="46819-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="46819-120">Il parametro *lParam* del messaggio **WM \_ create** contiene un puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="46819-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="46819-121">Il membro *lpCreateParams* di questa struttura contiene un puntatore alla struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passata con il messaggio **WM \_ MDICREATE** che ha creato la finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="46819-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="46819-122">Un'applicazione non deve inviare un secondo messaggio **WM \_ MDICREATE** mentre un messaggio **WM \_ MDICREATE** è ancora in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="46819-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="46819-123">Ad esempio, non deve inviare un messaggio **WM \_ MDICREATE** mentre una finestra figlio MDI sta elaborando il relativo messaggio **WM \_ MDICREATE** .</span><span class="sxs-lookup"><span data-stu-id="46819-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="46819-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46819-124">Requirements</span></span>



| <span data-ttu-id="46819-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="46819-125">Requirement</span></span> | <span data-ttu-id="46819-126">Valore</span><span class="sxs-lookup"><span data-stu-id="46819-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46819-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46819-127">Minimum supported client</span></span><br/> | <span data-ttu-id="46819-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46819-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46819-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46819-129">Minimum supported server</span></span><br/> | <span data-ttu-id="46819-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46819-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46819-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46819-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="46819-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46819-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46819-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46819-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="46819-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="46819-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46819-135">**CreateMDIWindow**</span><span class="sxs-lookup"><span data-stu-id="46819-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="46819-136">**STRUTTURA CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="46819-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="46819-137">**MDICREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="46819-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="46819-138">**creazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="46819-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="46819-139">**\_MDIDESTROY WM**</span><span class="sxs-lookup"><span data-stu-id="46819-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="46819-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="46819-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46819-141">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="46819-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
