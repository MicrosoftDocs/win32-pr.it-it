---
description: Un'applicazione invia il \_ messaggio WM MDIACTIVATE a una finestra del client di interfaccia a documenti multipli (MDI) per indicare alla finestra client di attivare una finestra figlio MDI diversa.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Messaggio WM_MDIACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312375"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="32ceb-103">\_Messaggio MDIACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="32ceb-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="32ceb-104">Un'applicazione invia il messaggio **WM \_ MDIACTIVATE** a una finestra del client di interfaccia a documenti multipli (MDI) per indicare alla finestra client di attivare una finestra figlio MDI diversa.</span><span class="sxs-lookup"><span data-stu-id="32ceb-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="32ceb-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="32ceb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ceb-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ceb-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ceb-107">Handle per la finestra figlio MDI da attivare.</span><span class="sxs-lookup"><span data-stu-id="32ceb-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="32ceb-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ceb-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ceb-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="32ceb-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ceb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32ceb-110">Return value</span></span>

<span data-ttu-id="32ceb-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="32ceb-111">Type: **LRESULT**</span></span>

<span data-ttu-id="32ceb-112">Se un'applicazione invia questo messaggio a una finestra del client MDI, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="32ceb-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="32ceb-113">Una finestra figlio MDI deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="32ceb-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ceb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="32ceb-114">Remarks</span></span>

<span data-ttu-id="32ceb-115">Quando la finestra client elabora questo messaggio, invia **WM \_ MDIACTIVATE** alla finestra figlio in fase di disattivazione e alla finestra figlio attivata.</span><span class="sxs-lookup"><span data-stu-id="32ceb-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="32ceb-116">I parametri del messaggio ricevuti da una finestra figlio MDI sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32ceb-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="32ceb-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ceb-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="32ceb-118">Handle per la finestra figlio MDI da disattivare.</span><span class="sxs-lookup"><span data-stu-id="32ceb-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="32ceb-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ceb-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="32ceb-120">Handle per la finestra figlio MDI attivata.</span><span class="sxs-lookup"><span data-stu-id="32ceb-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="32ceb-121">Una finestra figlio MDI viene attivata indipendentemente dalla finestra cornice MDI.</span><span class="sxs-lookup"><span data-stu-id="32ceb-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="32ceb-122">Quando la finestra cornice diventa attiva, la finestra figlio abilitata per l'ultima volta con il messaggio **WM \_ MDIACTIVATE** riceve il messaggio [**WM \_ NCACTIVATE**](wm-ncactivate.md) per creare una cornice e una barra del titolo attive; la finestra figlio non riceve un altro messaggio **WM \_ MDIACTIVATE** .</span><span class="sxs-lookup"><span data-stu-id="32ceb-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ceb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32ceb-123">Requirements</span></span>



| <span data-ttu-id="32ceb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ceb-124">Requirement</span></span> | <span data-ttu-id="32ceb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="32ceb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ceb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32ceb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32ceb-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32ceb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32ceb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32ceb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32ceb-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32ceb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32ceb-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32ceb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ceb-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32ceb-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ceb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32ceb-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="32ceb-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="32ceb-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32ceb-134">**\_MDIGETACTIVE WM**</span><span class="sxs-lookup"><span data-stu-id="32ceb-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="32ceb-135">**\_MDINEXT WM**</span><span class="sxs-lookup"><span data-stu-id="32ceb-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="32ceb-136">**\_NCACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="32ceb-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="32ceb-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="32ceb-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32ceb-138">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="32ceb-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




