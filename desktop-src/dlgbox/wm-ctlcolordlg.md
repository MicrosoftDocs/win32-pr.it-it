---
title: Messaggio WM_CTLCOLORDLG (winuser. h)
description: Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo. Rispondendo a questo messaggio, la finestra di dialogo può impostare il testo e i colori di sfondo usando l'handle del contesto del dispositivo di visualizzazione specificato.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Finestre di dialogo WM_CTLCOLORDLG messaggio
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740154"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="4b201-105">\_Messaggio CTLCOLORDLG WM</span><span class="sxs-lookup"><span data-stu-id="4b201-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="4b201-106">Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b201-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="4b201-107">Rispondendo a questo messaggio, la finestra di dialogo può impostare il testo e i colori di sfondo usando l'handle del contesto del dispositivo di visualizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="4b201-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="4b201-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b201-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b201-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b201-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b201-110">Handle per il contesto di dispositivo per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b201-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4b201-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b201-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b201-112">Handle per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b201-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b201-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b201-113">Return value</span></span>

<span data-ttu-id="4b201-114">Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello.</span><span class="sxs-lookup"><span data-stu-id="4b201-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="4b201-115">Il sistema utilizza il pennello per disegnare lo sfondo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b201-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b201-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b201-116">Remarks</span></span>

<span data-ttu-id="4b201-117">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b201-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="4b201-118">Il sistema non elimina automaticamente il pennello restituito.</span><span class="sxs-lookup"><span data-stu-id="4b201-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="4b201-119">È responsabilità dell'applicazione eliminare il pennello quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="4b201-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="4b201-120">Il messaggio **WM \_ CTLCOLORDLG** non viene mai inviato tra i thread.</span><span class="sxs-lookup"><span data-stu-id="4b201-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="4b201-121">Viene inviato solo all'interno di un thread.</span><span class="sxs-lookup"><span data-stu-id="4b201-121">It is sent only within one thread.</span></span>

<span data-ttu-id="4b201-122">Si noti che il messaggio **WM \_ CTLCOLORDLG** viene inviato alla finestra di dialogo; tutti gli altri \**WM \_ CTLCOLOR \** _ messaggi vengono inviati al proprietario del controllo.</span><span class="sxs-lookup"><span data-stu-id="4b201-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="4b201-123">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un _ *int \_ ptr*\* e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="4b201-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="4b201-124">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="4b201-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="4b201-125">Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4b201-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b201-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b201-126">Requirements</span></span>



| <span data-ttu-id="4b201-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b201-127">Requirement</span></span> | <span data-ttu-id="4b201-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4b201-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b201-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b201-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4b201-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b201-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4b201-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b201-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4b201-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b201-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b201-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b201-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b201-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b201-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b201-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b201-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b201-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4b201-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b201-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="4b201-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4b201-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="4b201-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="4b201-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4b201-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b201-140">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="4b201-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="4b201-141">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4b201-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4b201-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="4b201-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4b201-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="4b201-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

