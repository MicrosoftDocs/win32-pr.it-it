---
description: Un'applicazione invia il \_ messaggio WM MDISETMENU a una finestra del client di interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu finestra della finestra cornice o entrambi.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Messaggio WM_MDISETMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312373"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="d35e1-103">\_Messaggio MDISETMENU WM</span><span class="sxs-lookup"><span data-stu-id="d35e1-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="d35e1-104">Un'applicazione invia il messaggio **WM \_ MDISETMENU** a una finestra del client di interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu finestra della finestra cornice o entrambi.</span><span class="sxs-lookup"><span data-stu-id="d35e1-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="d35e1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d35e1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d35e1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d35e1-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d35e1-107">Handle per il nuovo menu della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="d35e1-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="d35e1-108">Se questo parametro è **null**, il menu della finestra cornice non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="d35e1-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="d35e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d35e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d35e1-110">Handle per il menu nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="d35e1-110">A handle to the new window menu.</span></span> <span data-ttu-id="d35e1-111">Se questo parametro è **null**, il menu finestra non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="d35e1-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d35e1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d35e1-112">Return value</span></span>

<span data-ttu-id="d35e1-113">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="d35e1-113">Type: **HMENU**</span></span>

<span data-ttu-id="d35e1-114">Se il messaggio ha esito positivo, il valore restituito è l'handle per il vecchio menu della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="d35e1-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="d35e1-115">Se il messaggio ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="d35e1-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d35e1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d35e1-116">Remarks</span></span>

<span data-ttu-id="d35e1-117">Dopo l'invio di questo messaggio, un'applicazione deve chiamare la funzione [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="d35e1-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="d35e1-118">Se questo messaggio sostituisce il menu finestra, le voci di menu finestra figlio MDI vengono rimosse dal menu finestra precedente e aggiunte al menu nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="d35e1-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="d35e1-119">Se una finestra figlio MDI viene ingrandita e questo messaggio sostituisce il menu della finestra cornice MDI, l'icona del menu finestra e l'icona di ripristino vengono rimossi dal menu della finestra cornice precedente e aggiunti al menu nuova finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="d35e1-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35e1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d35e1-120">Requirements</span></span>



| <span data-ttu-id="d35e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35e1-121">Requirement</span></span> | <span data-ttu-id="d35e1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d35e1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35e1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35e1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d35e1-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d35e1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d35e1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35e1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d35e1-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d35e1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d35e1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d35e1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35e1-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d35e1-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35e1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d35e1-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d35e1-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d35e1-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d35e1-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="d35e1-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="d35e1-132">**\_MDIREFRESHMENU WM**</span><span class="sxs-lookup"><span data-stu-id="d35e1-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="d35e1-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d35e1-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d35e1-134">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="d35e1-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
