---
title: Messaggio WM_MENUSELECT (winuser. h)
description: Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- Menu del messaggio WM_MENUSELECT e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302727"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="fefa1-104">\_Messaggio MENUSELECT WM</span><span class="sxs-lookup"><span data-stu-id="fefa1-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="fefa1-105">Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="fefa1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fefa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefa1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fefa1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fefa1-108">La parola di ordine inferiore specifica la voce di menu o l'indice del sottomenu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="fefa1-109">Se l'elemento selezionato è un elemento di comando, questo parametro contiene l'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="fefa1-110">Se l'elemento selezionato apre un menu a discesa o un sottomenu, questo parametro contiene l'indice del menu a discesa o del sottomenu nel menu principale e il parametro *lParam* contiene l'handle per il menu principale (selezionato); usare la funzione [**getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) per ottenere l'handle di menu nel menu a discesa o nel sottomenu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="fefa1-111">La parola più ordinata specifica uno o più flag di menu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="fefa1-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fefa1-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="fefa1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="fefa1-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="fefa1-114">Significato</span><span class="sxs-lookup"><span data-stu-id="fefa1-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="fefa1-115"><dt>**MF \_ BITMAP**</dt> <dt>0x00000004L</dt></span><span class="sxs-lookup"><span data-stu-id="fefa1-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="fefa1-116">Elemento consente di visualizzare una bitmap.</span><span class="sxs-lookup"><span data-stu-id="fefa1-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="fefa1-117"><dt>**MF \_**</dt> <dt>0x00000008L</dt> selezionata</span><span class="sxs-lookup"><span data-stu-id="fefa1-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="fefa1-118">L'elemento è selezionato.</span><span class="sxs-lookup"><span data-stu-id="fefa1-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="fefa1-119"><dt>**MF \_ 0x00000002L DISABILITAto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fefa1-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="fefa1-120">La voce è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fefa1-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="fefa1-121"><dt>**MF \_**</dt> <dt>0x00000001L</dt> grigio</span><span class="sxs-lookup"><span data-stu-id="fefa1-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="fefa1-122">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="fefa1-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="fefa1-123"><dt>**MF \_**</dt> <dt>0x00000080L</dt> HILITE</span><span class="sxs-lookup"><span data-stu-id="fefa1-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="fefa1-124">L'elemento è evidenziato.</span><span class="sxs-lookup"><span data-stu-id="fefa1-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="fefa1-125"><dt>**MF \_**</dt> <dt>0x00008000L</dt> MOUSESELECT</span><span class="sxs-lookup"><span data-stu-id="fefa1-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="fefa1-126">L'elemento viene selezionato con il mouse.</span><span class="sxs-lookup"><span data-stu-id="fefa1-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="fefa1-127"><dt>**MF \_**</dt> <dt>0x00000100L</dt> OWNERDRAW</span><span class="sxs-lookup"><span data-stu-id="fefa1-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="fefa1-128">Item è un elemento creato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="fefa1-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="fefa1-129"><dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="fefa1-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="fefa1-130">Elemento consente di aprire un menu a discesa o un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="fefa1-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="fefa1-131"><dt>**MF \_**</dt> <dt>0x00002000L</dt> SYSMENU</span><span class="sxs-lookup"><span data-stu-id="fefa1-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="fefa1-132">L'elemento è contenuto nel menu finestra.</span><span class="sxs-lookup"><span data-stu-id="fefa1-132">Item is contained in the window menu.</span></span> <span data-ttu-id="fefa1-133">Il parametro *lParam* contiene un handle per il menu associato al messaggio.</span><span class="sxs-lookup"><span data-stu-id="fefa1-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fefa1-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fefa1-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fefa1-135">Handle per il menu su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="fefa1-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefa1-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fefa1-136">Return value</span></span>

<span data-ttu-id="fefa1-137">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="fefa1-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fefa1-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="fefa1-138">Remarks</span></span>

<span data-ttu-id="fefa1-139">Se la parola più ordinata di *wParam* contiene 0xFFFF e il parametro *lParam* contiene **null**, il menu è stato chiuso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fefa1-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="fefa1-140">Non usare il valore 1 per la parola più ordinata di *wParam*, perché questo valore è specificato come (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span><span class="sxs-lookup"><span data-stu-id="fefa1-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="fefa1-141">Se il valore è 0xFFFF, verrebbe interpretato come 0x0000FFFF, non 1, a causa del cast a **uint**.</span><span class="sxs-lookup"><span data-stu-id="fefa1-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fefa1-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fefa1-142">Requirements</span></span>



| <span data-ttu-id="fefa1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fefa1-143">Requirement</span></span> | <span data-ttu-id="fefa1-144">Valore</span><span class="sxs-lookup"><span data-stu-id="fefa1-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fefa1-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fefa1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fefa1-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fefa1-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fefa1-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fefa1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fefa1-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fefa1-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fefa1-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fefa1-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fefa1-150"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fefa1-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefa1-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fefa1-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="fefa1-152">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fefa1-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fefa1-153">**Getsottomenù**</span><span class="sxs-lookup"><span data-stu-id="fefa1-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="fefa1-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fefa1-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fefa1-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fefa1-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fefa1-156">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fefa1-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fefa1-157">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="fefa1-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

