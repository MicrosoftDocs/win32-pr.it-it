---
title: Messaggio PSM_SHOWWIZBUTTONS (Prsht. h)
description: Consente di visualizzare o nascondere i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Controlli di Windows Message PSM_SHOWWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301181"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="484b4-105">\_Messaggio SHOWWIZBUTTONS di PSM</span><span class="sxs-lookup"><span data-stu-id="484b4-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="484b4-106">Consente di visualizzare o nascondere i pulsanti in una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="484b4-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="484b4-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="484b4-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="484b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="484b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="484b4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="484b4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="484b4-110">Uno o più dei valori seguenti che specificano i pulsanti della finestra delle proprietà da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="484b4-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="484b4-111">Se il valore di un pulsante è incluso sia in questo parametro che in *lParam*, viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="484b4-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="484b4-112">Valore</span><span class="sxs-lookup"><span data-stu-id="484b4-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="484b4-113">Significato</span><span class="sxs-lookup"><span data-stu-id="484b4-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="484b4-114"><dt>**PSWIZB \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="484b4-115">Pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="484b4-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="484b4-116"><dt>**\_annullamento PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="484b4-117">Pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="484b4-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="484b4-118"><dt>**\_DISABLEDFINISH PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="484b4-119">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="484b4-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="484b4-120"><dt>**\_fine PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="484b4-121">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="484b4-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="484b4-122"><dt>**PSWIZB \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="484b4-123">Pulsante **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="484b4-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="484b4-124"><dt>**PSWIZB \_ Show**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="484b4-125">Impostare solo questo flag (definito come zero) per nascondere tutti i pulsanti specificati in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="484b4-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="484b4-126"><dt>**\_ripristino PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="484b4-127">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="484b4-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="484b4-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="484b4-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="484b4-129">Uno o più degli stessi valori utilizzati in *wParam*, che specificano quali pulsanti sono interessati da questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="484b4-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="484b4-130">Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, il pulsante è nascosto.</span><span class="sxs-lookup"><span data-stu-id="484b4-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="484b4-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="484b4-131">Return value</span></span>

<span data-ttu-id="484b4-132">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="484b4-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="484b4-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="484b4-133">Remarks</span></span>

<span data-ttu-id="484b4-134">Le procedure guidate visualizzano tre o quattro pulsanti sotto ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="484b4-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="484b4-135">Questo messaggio viene usato per specificare quali pulsanti sono visibili.</span><span class="sxs-lookup"><span data-stu-id="484b4-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="484b4-136">Le procedure guidate di solito visualizzano **indietro**, **Annulla** e un pulsante **Avanti** o **fine** .</span><span class="sxs-lookup"><span data-stu-id="484b4-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="484b4-137">Il pulsante **Annulla** è sempre visibile.</span><span class="sxs-lookup"><span data-stu-id="484b4-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="484b4-138">In genere, **impostare \_ PSWIZB Finish** o **PSWIZB \_ DISABLEDFINISH** per sostituire il pulsante **Avanti** con il pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="484b4-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="484b4-139">Per visualizzare contemporaneamente i pulsanti **Avanti** e **fine** , impostare il flag **PSH \_ WIZARDHASFINISH** nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) quando si crea la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="484b4-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="484b4-140">Ogni pagina visualizzerà quindi tutti i quattro pulsanti: **indietro**, **Avanti**, **Annulla** e **fine**.</span><span class="sxs-lookup"><span data-stu-id="484b4-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="484b4-141">Se si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) per inviare questo messaggio, verrà pubblicato.</span><span class="sxs-lookup"><span data-stu-id="484b4-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="484b4-142">In qualsiasi altro momento, è possibile usare [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per inviare **PSM \_ SHOWWIZBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="484b4-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="484b4-143">Se il gestore di notifiche utilizza [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) per inviare un messaggio **PSM \_ SHOWWIZBUTTONS** , non eseguire alcuna operazione che influirà sullo stato attivo della finestra fino a quando il gestore non viene restituito.</span><span class="sxs-lookup"><span data-stu-id="484b4-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="484b4-144">Se, ad esempio, si chiama [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediatamente dopo aver usato **PostMessage** per inviare **PSM \_ SHOWWIZBUTTONS**, la finestra di messaggio riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="484b4-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="484b4-145">Poiché i messaggi inviati non vengono recapitati fino a quando non raggiungono l'intestazione della coda di messaggi, il messaggio **PSM \_ SHOWWIZBUTTONS** non verrà recapitato fino al termine della procedura guidata per la finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="484b4-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="484b4-146">Di conseguenza, la finestra delle proprietà non sarà in grado di impostare correttamente lo stato attivo per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="484b4-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="484b4-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="484b4-147">Requirements</span></span>



| <span data-ttu-id="484b4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="484b4-148">Requirement</span></span> | <span data-ttu-id="484b4-149">Valore</span><span class="sxs-lookup"><span data-stu-id="484b4-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="484b4-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="484b4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="484b4-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="484b4-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="484b4-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="484b4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="484b4-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="484b4-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="484b4-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="484b4-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="484b4-155"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="484b4-155"><dt>Prsht.h</dt></span></span> </dl> |



 

