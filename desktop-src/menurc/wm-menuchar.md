---
title: Messaggio WM_MENUCHAR (winuser. h)
description: Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o tasto di scelta rapida. Questo messaggio viene inviato alla finestra che possiede il menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- Menu del messaggio WM_MENUCHAR e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743831"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="90dae-105">\_Messaggio MENUCHAR WM</span><span class="sxs-lookup"><span data-stu-id="90dae-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="90dae-106">Inviato quando un menu è attivo e l'utente preme un tasto che non corrisponde ad alcun tasto di scelta rapida o tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="90dae-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="90dae-107">Questo messaggio viene inviato alla finestra che possiede il menu.</span><span class="sxs-lookup"><span data-stu-id="90dae-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="90dae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90dae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90dae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90dae-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90dae-110">La parola di ordine inferiore specifica il codice carattere che corrisponde alla chiave che l'utente ha premuto.</span><span class="sxs-lookup"><span data-stu-id="90dae-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="90dae-111">La parola di ordine superiore specifica il tipo di menu attivo.</span><span class="sxs-lookup"><span data-stu-id="90dae-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="90dae-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="90dae-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="90dae-113">Valore</span><span class="sxs-lookup"><span data-stu-id="90dae-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="90dae-114">Significato</span><span class="sxs-lookup"><span data-stu-id="90dae-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="90dae-115"><dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="90dae-116">Menu A discesa, sottomenu o menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="90dae-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="90dae-117"><dt>**MF \_**</dt> <dt>0x00002000L</dt> SYSMENU</span><span class="sxs-lookup"><span data-stu-id="90dae-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="90dae-118">Menu finestra.</span><span class="sxs-lookup"><span data-stu-id="90dae-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="90dae-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90dae-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90dae-120">Handle per il menu attivo.</span><span class="sxs-lookup"><span data-stu-id="90dae-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90dae-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90dae-121">Return value</span></span>

<span data-ttu-id="90dae-122">Un'applicazione che elabora questo messaggio deve restituire uno dei valori seguenti nella parola più ordinata del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="90dae-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="90dae-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="90dae-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="90dae-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90dae-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90dae-125">Multipagina <dt>**\_ Chiudi**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="90dae-126">Informa il sistema che dovrebbe chiudere il menu attivo.</span><span class="sxs-lookup"><span data-stu-id="90dae-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="90dae-127">Multipagina <dt>**\_ ESECUZIONE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="90dae-128">Informa il sistema che deve scegliere l'elemento specificato nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="90dae-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="90dae-129">La finestra proprietaria riceve un messaggio di [**\_ comando WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="90dae-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="90dae-130">Multipagina <dt>**\_ Ignora**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="90dae-131">Informa il sistema che deve eliminare il carattere premuto dall'utente e creare un breve beep sull'altoparlante del sistema.</span><span class="sxs-lookup"><span data-stu-id="90dae-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="90dae-132">Multipagina <dt>**\_ SELEZIONARE**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="90dae-133">Informa il sistema che deve selezionare l'elemento specificato nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="90dae-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="90dae-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="90dae-134">Remarks</span></span>

<span data-ttu-id="90dae-135">La parola di basso livello viene ignorata se la parola più significativa contiene 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="90dae-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="90dae-136">Un'applicazione deve elaborare questo messaggio quando viene usato un acceleratore per selezionare una voce di menu che visualizza una bitmap.</span><span class="sxs-lookup"><span data-stu-id="90dae-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="90dae-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90dae-137">Requirements</span></span>



| <span data-ttu-id="90dae-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="90dae-138">Requirement</span></span> | <span data-ttu-id="90dae-139">Valore</span><span class="sxs-lookup"><span data-stu-id="90dae-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dae-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90dae-140">Minimum supported client</span></span><br/> | <span data-ttu-id="90dae-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90dae-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90dae-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90dae-142">Minimum supported server</span></span><br/> | <span data-ttu-id="90dae-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90dae-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90dae-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90dae-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dae-145"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90dae-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90dae-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90dae-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="90dae-147">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="90dae-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="90dae-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90dae-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="90dae-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90dae-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="90dae-150">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="90dae-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90dae-151">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="90dae-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

