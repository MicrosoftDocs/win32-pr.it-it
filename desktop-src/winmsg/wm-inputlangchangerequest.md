---
description: Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione del pannello di controllo della tastiera) o dall'indicatore sulla barra delle applicazioni del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Messaggio WM_INPUTLANGCHANGEREQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312378"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="ff798-103">\_Messaggio INPUTLANGCHANGEREQUEST WM</span><span class="sxs-lookup"><span data-stu-id="ff798-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="ff798-104">Inviato alla finestra con lo stato attivo quando l'utente sceglie una nuova lingua di input, con il tasto di scelta rapida (specificato nell'applicazione del pannello di controllo della tastiera) o dall'indicatore sulla barra delle applicazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff798-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="ff798-105">Un'applicazione può accettare la modifica passando il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rifiutare la modifica (e impedirne l'esecuzione) restituendo immediatamente.</span><span class="sxs-lookup"><span data-stu-id="ff798-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="ff798-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ff798-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="ff798-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff798-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff798-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff798-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff798-109">Nuove impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="ff798-109">The new input locale.</span></span> <span data-ttu-id="ff798-110">Questo parametro può essere una combinazione dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff798-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="ff798-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ff798-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="ff798-112">Significato</span><span class="sxs-lookup"><span data-stu-id="ff798-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="ff798-113"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> indietro</span><span class="sxs-lookup"><span data-stu-id="ff798-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="ff798-114">È stato usato un tasto di scelta per scegliere le impostazioni locali di input precedenti nell'elenco installato delle impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="ff798-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="ff798-115">Questo flag non può essere usato con il \_ flag di avanzamento INPUTLANGCHANGE.</span><span class="sxs-lookup"><span data-stu-id="ff798-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="ff798-116"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0X0002</dt> di avanzamento</span><span class="sxs-lookup"><span data-stu-id="ff798-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="ff798-117">È stato usato un tasto di scelta per scegliere le impostazioni locali di input successive nell'elenco installato delle impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="ff798-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="ff798-118">Questo flag non può essere usato con il \_ flag INPUTLANGCHANGE indietro.</span><span class="sxs-lookup"><span data-stu-id="ff798-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="ff798-119"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0001</dt> SYSCHARSET</span><span class="sxs-lookup"><span data-stu-id="ff798-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ff798-120">Il nuovo layout della tastiera delle impostazioni locali di input può essere utilizzato con il set di caratteri di sistema.</span><span class="sxs-lookup"><span data-stu-id="ff798-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="ff798-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff798-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff798-122">Identificatore delle impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="ff798-122">The input locale identifier.</span></span> <span data-ttu-id="ff798-123">Per altre informazioni, vedere [lingue, impostazioni locali e layout di tastiera](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="ff798-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff798-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff798-124">Return value</span></span>

<span data-ttu-id="ff798-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff798-125">Type: **LRESULT**</span></span>

<span data-ttu-id="ff798-126">Questo messaggio viene pubblicato, non inviato, all'applicazione, quindi il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ff798-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="ff798-127">Per accettare la modifica, l'applicazione deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ff798-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="ff798-128">Per rifiutare la modifica, l'applicazione deve restituire zero senza chiamare **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="ff798-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff798-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff798-129">Remarks</span></span>

<span data-ttu-id="ff798-130">Quando la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) riceve il messaggio **WM \_ INPUTLANGCHANGEREQUEST** , attiva le nuove impostazioni locali di input e invia una notifica all'applicazione della modifica inviando il messaggio [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) .</span><span class="sxs-lookup"><span data-stu-id="ff798-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="ff798-131">L'indicatore della lingua è presente sulla barra delle applicazioni solo se è stato installato più di un layout di tastiera e se è stato abilitato l'indicatore utilizzando l'applicazione del pannello di controllo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ff798-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff798-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff798-132">Requirements</span></span>



| <span data-ttu-id="ff798-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff798-133">Requirement</span></span> | <span data-ttu-id="ff798-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ff798-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff798-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff798-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ff798-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff798-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff798-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff798-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ff798-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff798-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff798-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff798-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff798-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff798-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff798-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff798-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff798-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ff798-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff798-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ff798-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ff798-144">**\_INPUTLANGCHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="ff798-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="ff798-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ff798-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff798-146">Windows</span><span class="sxs-lookup"><span data-stu-id="ff798-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 
