---
title: Messaggio WM_CHANGEUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM CHANGEUISTATE per indicare che lo stato dell'interfaccia utente deve essere modificato.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- Menu del messaggio WM_CHANGEUISTATE e altre risorse
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743583"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="751ad-104">\_Messaggio CHANGEUISTATE WM</span><span class="sxs-lookup"><span data-stu-id="751ad-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="751ad-105">Un'applicazione invia il messaggio **WM \_ CHANGEUISTATE** per indicare che lo stato dell'interfaccia utente deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="751ad-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="751ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="751ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="751ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="751ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="751ad-108">La parola di ordine inferiore specifica l'azione da intraprendere.</span><span class="sxs-lookup"><span data-stu-id="751ad-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="751ad-109">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="751ad-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="751ad-110">Valore</span><span class="sxs-lookup"><span data-stu-id="751ad-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="751ad-111">Significato</span><span class="sxs-lookup"><span data-stu-id="751ad-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="751ad-112"><dt>**Interfacce utente \_ Cancella**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="751ad-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="751ad-113">I flag di stato dell'interfaccia utente specificati dalla parola di ordine superiore devono essere cancellati.</span><span class="sxs-lookup"><span data-stu-id="751ad-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="751ad-114"><dt>**Interfacce utente \_ Inizializza**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="751ad-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="751ad-115">I flag di stato dell'interfaccia utente specificati dalla parola di ordine superiore devono essere modificati in base all'ultimo evento di input.</span><span class="sxs-lookup"><span data-stu-id="751ad-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="751ad-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="751ad-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="751ad-117"><dt>**Interfacce utente \_ SET**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="751ad-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="751ad-118">È necessario impostare i flag di stato dell'interfaccia utente specificati dalla parola più avanzata.</span><span class="sxs-lookup"><span data-stu-id="751ad-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="751ad-119">La parola più ordinata specifica quali elementi di stato dell'interfaccia utente sono interessati o lo stile del controllo.</span><span class="sxs-lookup"><span data-stu-id="751ad-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="751ad-120">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="751ad-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="751ad-121">Valore</span><span class="sxs-lookup"><span data-stu-id="751ad-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="751ad-122">Significato</span><span class="sxs-lookup"><span data-stu-id="751ad-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="751ad-123"><dt>**UISF \_**</dt> <dt>0x4</dt> attivo</span><span class="sxs-lookup"><span data-stu-id="751ad-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="751ad-124">Un controllo deve essere disegnato nello stile usato per i controlli attivi.</span><span class="sxs-lookup"><span data-stu-id="751ad-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="751ad-125"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="751ad-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="751ad-126">Gli acceleratori tastiera sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="751ad-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="751ad-127"><dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus</span><span class="sxs-lookup"><span data-stu-id="751ad-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="751ad-128">Gli indicatori di stato attivo sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="751ad-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="751ad-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="751ad-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="751ad-130">Questo parametro non viene utilizzato e deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="751ad-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="751ad-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="751ad-131">Remarks</span></span>

<span data-ttu-id="751ad-132">Una finestra deve inviare questo messaggio a se stesso o al relativo padre quando deve modificare gli elementi di stato dell'interfaccia utente di tutte le finestre nella stessa gerarchia.</span><span class="sxs-lookup"><span data-stu-id="751ad-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="751ad-133">La routine della finestra deve consentire a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) di elaborare questo messaggio in modo che l'intero albero della finestra abbia uno stato coerente dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="751ad-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="751ad-134">Quando la finestra di primo livello riceve il messaggio **WM \_ CHANGEUISTATE** , invia un messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con gli stessi parametri a tutte le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="751ad-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="751ad-135">Quando il sistema elabora il messaggio **WM \_ UPDATEUISTATE** , apporta la modifica nello stato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="751ad-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="751ad-136">Se la parola più bassa di *wParam* è l'inizializzazione di interfacce utente \_ , il sistema invierà il messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con lo stato dell'interfaccia utente in base all'ultimo evento di input.</span><span class="sxs-lookup"><span data-stu-id="751ad-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="751ad-137">Se, ad esempio, l'ultimo input proviene dal mouse, il sistema nasconderà i segnali da tastiera. Se l'ultimo input proviene dalla tastiera, il sistema visualizzerà i suggerimenti da tastiera. Se lo stato risultante dall'elaborazione di **WM \_ CHANGEUISTATE** è uguale a quello precedente, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non invia questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="751ad-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="751ad-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="751ad-138">Requirements</span></span>



| <span data-ttu-id="751ad-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="751ad-139">Requirement</span></span> | <span data-ttu-id="751ad-140">Valore</span><span class="sxs-lookup"><span data-stu-id="751ad-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="751ad-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="751ad-141">Minimum supported client</span></span><br/> | <span data-ttu-id="751ad-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="751ad-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="751ad-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="751ad-143">Minimum supported server</span></span><br/> | <span data-ttu-id="751ad-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="751ad-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="751ad-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="751ad-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="751ad-146"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="751ad-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751ad-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="751ad-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="751ad-148">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="751ad-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="751ad-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="751ad-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="751ad-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="751ad-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="751ad-151">**\_QUERYUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="751ad-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="751ad-152">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="751ad-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="751ad-153">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="751ad-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

