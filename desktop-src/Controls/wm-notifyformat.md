---
title: Messaggio WM_NOTIFYFORMAT (winuser. h)
description: Determina se una finestra accetta strutture ANSI o Unicode nel messaggio di \_ notifica di WM Notify. I \_ messaggi WM NOTIFYFORMAT vengono inviati da un controllo comune alla relativa finestra padre e dalla finestra padre al controllo comune.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Controlli di Windows Message WM_NOTIFYFORMAT
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964462"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="3b5d5-105">\_Messaggio NOTIFYFORMAT WM</span><span class="sxs-lookup"><span data-stu-id="3b5d5-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="3b5d5-106">Determina se una finestra accetta strutture ANSI o Unicode nel messaggio di notifica di [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="3b5d5-107">**WM \_** I messaggi NOTIFYFORMAT vengono inviati da un controllo comune alla relativa finestra padre e dalla finestra padre al controllo comune.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b5d5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b5d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b5d5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b5d5-110">Handle per la finestra che invia il messaggio **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="3b5d5-111">Se *lParam* è \_ una query NF, questo parametro è l'handle di un controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="3b5d5-112">Se *lParam* è NF \_ Requery, questo parametro è l'handle per la finestra padre di un controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b5d5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b5d5-114">Valore del comando che specifica la natura del messaggio **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="3b5d5-115">Si otterrà uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b5d5-115">This will be one of the following values:</span></span>



| <span data-ttu-id="3b5d5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b5d5-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="3b5d5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3b5d5-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="3b5d5-118"><dt>**\_query NF**</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="3b5d5-119">Il messaggio è una query per determinare se le strutture ANSI o Unicode devono essere utilizzate nei messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="3b5d5-120">Questo comando viene inviato da un controllo alla relativa finestra padre durante la creazione di un controllo e in risposta a un \_ comando NF Requery.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="3b5d5-121"><dt>**Requery NF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="3b5d5-122">Il messaggio è una richiesta di invio di un \_ modulo di query NF di questo messaggio alla finestra padre di un controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="3b5d5-123">Questo comando viene inviato dalla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-123">This command is sent from the parent window.</span></span> <span data-ttu-id="3b5d5-124">La finestra padre chiede al controllo di eseguire di nuovo la query sul tipo di strutture da usare nei messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="3b5d5-125">Se *lParam* è NF \_ Requery, il valore restituito è il risultato dell'operazione di riesecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5d5-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b5d5-126">Return value</span></span>

<span data-ttu-id="3b5d5-127">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-127">Returns one of the following values.</span></span>



| <span data-ttu-id="3b5d5-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3b5d5-128">Return code</span></span>                                                                                 | <span data-ttu-id="3b5d5-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b5d5-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b5d5-130"><dt>**NFR \_ ANSI**</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="3b5d5-131">È consigliabile usare le strutture ANSI nei messaggi [**WM \_ Notify**](wm-notify.md) inviati dal controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="3b5d5-132"><dt>**NFR \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="3b5d5-133">Le strutture Unicode devono essere usate nei messaggi [**WM \_ Notify**](wm-notify.md) inviati dal controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="3b5d5-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="3b5d5-135">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="3b5d5-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b5d5-136">Remarks</span></span>

<span data-ttu-id="3b5d5-137">Quando viene creato un controllo comune, il controllo Invia un messaggio **WM \_ NOTIFYFORMAT** alla finestra padre per determinare il tipo di strutture da usare nei messaggi [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="3b5d5-138">Se la finestra padre non gestisce questo messaggio, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) risponde in base al tipo della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="3b5d5-139">Ovvero, se la finestra padre è una finestra Unicode, **DefWindowProc** restituisce NFR \_ Unicode e se la finestra padre è una finestra ANSI, **DefWindowProc** restituisce NFR \_ ANSI.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="3b5d5-140">Se la finestra padre è una finestra di dialogo e non gestisce questo messaggio, la funzione [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) risponde in modo analogo a seconda del tipo di finestra di dialogo (Unicode o ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b5d5-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="3b5d5-141">Una finestra padre può modificare il tipo di strutture usate da un controllo comune nei messaggi di [**\_ notifica WM**](wm-notify.md) impostando *lParam* su NF per \_ ripetere la query e inviando un messaggio **WM \_ NOTIFYFORMAT** al controllo.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="3b5d5-142">Questo fa in modo che il controllo invii un \_ modulo di query NF del messaggio **WM \_ NOTIFYFORMAT** alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="3b5d5-143">Tutti i controlli comuni invieranno messaggi **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="3b5d5-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="3b5d5-144">Tuttavia, i controlli Windows standard (modifica controlli, caselle combinate, caselle di riepilogo, pulsanti, barre di scorrimento e controlli statici) non lo sono.</span><span class="sxs-lookup"><span data-stu-id="3b5d5-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5d5-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b5d5-145">Requirements</span></span>



| <span data-ttu-id="3b5d5-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5d5-146">Requirement</span></span> | <span data-ttu-id="3b5d5-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3b5d5-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5d5-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b5d5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5d5-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b5d5-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3b5d5-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b5d5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5d5-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b5d5-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3b5d5-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b5d5-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b5d5-153"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d5-153"><dt>Winuser.h</dt></span></span> </dl> |



 

