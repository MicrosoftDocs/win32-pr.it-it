---
title: Messaggio PSM_SETWIZBUTTONS (Prsht. h)
description: Abilita o Disabilita i pulsanti indietro, avanti e fine in una procedura guidata. È anche possibile usare la \_ macro PropSheet SetWizButtons per inviare il messaggio.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Controlli di Windows Message PSM_SETWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120114"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="7440b-105">\_Messaggio SETWIZBUTTONS di PSM</span><span class="sxs-lookup"><span data-stu-id="7440b-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="7440b-106">Abilita o Disabilita i pulsanti **indietro**, **Avanti** e **fine** in una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="7440b-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="7440b-107">È anche possibile usare la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7440b-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="7440b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7440b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7440b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7440b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7440b-110">Impostare questo parametro su PSWIZBF \_ ELEVATIONREQUIRED per visualizzare l'icona con privilegi elevati nei pulsanti specificati in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7440b-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="7440b-111">L'icona con privilegi elevati (o l'icona dello scudo UAC) indica che la richiesta di elevazione dei privilegi verrà usata per richiedere l'approvazione o le credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7440b-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="7440b-112">Per ulteriori informazioni, vedere [progettazione di applicazioni UAC per Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7440b-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="7440b-113">La visualizzazione dell'icona dello scudo del controllo dell'account utente è supportata solo in AeroWizards (PSH \_ AEROWIZARD).</span><span class="sxs-lookup"><span data-stu-id="7440b-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="7440b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7440b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7440b-115">Valore che specifica quali pulsanti della finestra delle proprietà sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="7440b-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="7440b-116">È possibile combinare uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="7440b-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="7440b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7440b-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="7440b-118">Significato</span><span class="sxs-lookup"><span data-stu-id="7440b-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="7440b-119"><dt>**PSWIZB \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="7440b-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="7440b-120">Abilita il pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="7440b-120">Enables the **Back** button.</span></span> <span data-ttu-id="7440b-121">Se questo flag non è impostato, il pulsante **indietro** viene visualizzato come disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7440b-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="7440b-122"><dt>**\_DISABLEDFINISH PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="7440b-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="7440b-123">Visualizza un pulsante **fine** disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7440b-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="7440b-124"><dt>**\_fine PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="7440b-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="7440b-125">Visualizza un pulsante **fine** abilitato.</span><span class="sxs-lookup"><span data-stu-id="7440b-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="7440b-126"><dt>**PSWIZB \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="7440b-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="7440b-127">Abilita il pulsante **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="7440b-127">Enables the **Next** button.</span></span> <span data-ttu-id="7440b-128">Se questo flag non è impostato, il pulsante **Avanti** viene visualizzato come disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7440b-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7440b-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7440b-129">Return value</span></span>

<span data-ttu-id="7440b-130">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7440b-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7440b-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="7440b-131">Remarks</span></span>

<span data-ttu-id="7440b-132">Se il gestore di notifiche utilizza [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) per inviare un messaggio **PSM \_ SETWIZBUTTONS** , non eseguire alcuna operazione che influirà sullo stato attivo della finestra fino a quando il gestore non viene restituito.</span><span class="sxs-lookup"><span data-stu-id="7440b-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="7440b-133">Se, ad esempio, si chiama [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediatamente dopo aver usato **PostMessage** per inviare **PSM \_ SETWIZBUTTONS**, la finestra di messaggio riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="7440b-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="7440b-134">Poiché i messaggi inviati non vengono recapitati fino a quando non raggiungono l'intestazione della coda di messaggi, il messaggio **PSM \_ SETWIZBUTTONS** non verrà recapitato fino al termine della procedura guidata per la finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="7440b-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="7440b-135">Di conseguenza, la finestra delle proprietà non sarà in grado di impostare correttamente lo stato attivo per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="7440b-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="7440b-136">Se si invia il \_ messaggio SETWIZBUTTONS di PSM durante la gestione della [notifica \_ seattiva PSN](psn-setactive.md) , usare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) anziché la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="7440b-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="7440b-137">In caso contrario, i pulsanti non vengono aggiornati correttamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7440b-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="7440b-138">Se si usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per inviare questo messaggio, verrà pubblicato.</span><span class="sxs-lookup"><span data-stu-id="7440b-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="7440b-139">In qualsiasi altro momento, è possibile usare **SendMessage** per inviare **PSM \_ SETWIZBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="7440b-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="7440b-140">Le procedure guidate visualizzano tre o quattro pulsanti sotto ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="7440b-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="7440b-141">Questo messaggio viene usato per specificare quali pulsanti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="7440b-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="7440b-142">Le procedure guidate di solito visualizzano **indietro**, **Annulla** e un pulsante **Avanti** o **fine** .</span><span class="sxs-lookup"><span data-stu-id="7440b-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="7440b-143">In genere è possibile abilitare solo il pulsante **Avanti** per la pagina iniziale, **Avanti** e **indietro** per le pagine interne, quindi **tornare** alla pagina di completamento e **terminarla** .</span><span class="sxs-lookup"><span data-stu-id="7440b-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="7440b-144">Il pulsante **Annulla** è sempre abilitato.</span><span class="sxs-lookup"><span data-stu-id="7440b-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="7440b-145">In genere, \_ l'impostazione di PSWIZB Finish o PSWIZB \_ DISABLEDFINISH sostituisce il pulsante **Avanti** con il pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="7440b-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="7440b-146">Per visualizzare contemporaneamente i pulsanti **Avanti** e **fine** , impostare il \_ flag PSH WIZARDHASFINISH nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) della procedura guidata quando si crea la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="7440b-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="7440b-147">Ogni pagina visualizzerà quindi tutti e quattro i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="7440b-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="7440b-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7440b-148">Requirements</span></span>



| <span data-ttu-id="7440b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="7440b-149">Requirement</span></span> | <span data-ttu-id="7440b-150">Valore</span><span class="sxs-lookup"><span data-stu-id="7440b-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7440b-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7440b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7440b-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7440b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7440b-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7440b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7440b-154">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7440b-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7440b-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7440b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="7440b-156"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7440b-156"><dt>Prsht.h</dt></span></span> </dl> |



 

