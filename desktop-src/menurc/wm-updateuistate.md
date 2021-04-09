---
title: Messaggio WM_UPDATEUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM UPDATEUISTATE per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- Menu del messaggio WM_UPDATEUISTATE e altre risorse
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121619"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="4f967-104">\_Messaggio UPDATEUISTATE WM</span><span class="sxs-lookup"><span data-stu-id="4f967-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="4f967-105">Un'applicazione invia il messaggio **WM \_ UPDATEUISTATE** per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="4f967-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="4f967-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f967-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f967-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f967-108">La parola di ordine inferiore specifica l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4f967-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="4f967-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f967-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4f967-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4f967-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="4f967-111">Significato</span><span class="sxs-lookup"><span data-stu-id="4f967-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="4f967-112"><dt>**Interfacce utente \_ Cancella**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f967-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="4f967-113">L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa deve essere nascosto.</span><span class="sxs-lookup"><span data-stu-id="4f967-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="4f967-114"><dt>**Interfacce utente \_ Inizializza**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4f967-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="4f967-115">L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa deve essere modificato in base all'ultimo evento di input.</span><span class="sxs-lookup"><span data-stu-id="4f967-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="4f967-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4f967-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="4f967-117"><dt>**Interfacce utente \_ SET**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f967-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="4f967-118">L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa dovrebbe essere visibile.</span><span class="sxs-lookup"><span data-stu-id="4f967-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="4f967-119">La parola più ordinata specifica quali elementi di stato dell'interfaccia utente sono interessati o lo stile del controllo.</span><span class="sxs-lookup"><span data-stu-id="4f967-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="4f967-120">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f967-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4f967-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4f967-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="4f967-122">Significato</span><span class="sxs-lookup"><span data-stu-id="4f967-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="4f967-123"><dt>**UISF \_**</dt> <dt>0x4</dt> attivo</span><span class="sxs-lookup"><span data-stu-id="4f967-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="4f967-124">Un controllo deve essere disegnato nello stile usato per i controlli attivi.</span><span class="sxs-lookup"><span data-stu-id="4f967-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="4f967-125"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="4f967-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="4f967-126">Tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4f967-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="4f967-127"><dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus</span><span class="sxs-lookup"><span data-stu-id="4f967-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="4f967-128">Indicatori di stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4f967-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="4f967-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f967-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f967-130">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4f967-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f967-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f967-131">Remarks</span></span>

<span data-ttu-id="4f967-132">Una finestra deve inviare questo messaggio per modificare lo stato dell'interfaccia utente di tutte le relative finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="4f967-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="4f967-133">A differenza del messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , che è una notifica, quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora il messaggio **WM \_ UPDATEUISTATE** modifica lo stato dell'interfaccia utente e propaga le modifiche a tutte le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="4f967-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="4f967-134">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aggiorna lo stato dell'interfaccia utente in base al valore *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4f967-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="4f967-135">Se lo stato dell'interfaccia utente viene modificato, la funzione Invia il messaggio a tutte le finestre figlio immediate.</span><span class="sxs-lookup"><span data-stu-id="4f967-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="4f967-136">**DefWindowProc** invia anche questo messaggio quando riceve un messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) che comunica al sistema che la finestra figlio intende modificare lo stato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4f967-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f967-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f967-137">Requirements</span></span>



| <span data-ttu-id="4f967-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f967-138">Requirement</span></span> | <span data-ttu-id="4f967-139">Valore</span><span class="sxs-lookup"><span data-stu-id="4f967-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f967-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f967-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4f967-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f967-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4f967-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f967-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4f967-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f967-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f967-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f967-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f967-145"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f967-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f967-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f967-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f967-147">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4f967-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4f967-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="4f967-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4f967-149">**\_CHANGEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="4f967-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="4f967-150">**\_QUERYUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="4f967-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="4f967-151">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4f967-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4f967-152">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="4f967-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

