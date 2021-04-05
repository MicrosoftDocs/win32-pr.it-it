---
title: Messaggio PSM_REMOVEPAGE (Prsht. h)
description: Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Controlli di Windows Message PSM_REMOVEPAGE
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874253"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="7ec8d-105">\_Messaggio REMOVEPAGE di PSM</span><span class="sxs-lookup"><span data-stu-id="7ec8d-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="7ec8d-106">Rimuove una pagina da una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="7ec8d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .</span><span class="sxs-lookup"><span data-stu-id="7ec8d-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ec8d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ec8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ec8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec8d-110">Indice in base zero della pagina da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="7ec8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ec8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec8d-112">Handle HPROPSHEETPAGE della pagina da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec8d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ec8d-113">Return value</span></span>

<span data-ttu-id="7ec8d-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec8d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ec8d-115">Remarks</span></span>

<span data-ttu-id="7ec8d-116">Un'applicazione può specificare l'indice o l'handle o entrambi.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="7ec8d-117">Se vengono specificati entrambi, *lParam* avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="7ec8d-118">L'invio di **PSM \_ REMOVEPAGE** Elimina la pagina della finestra delle proprietà da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="7ec8d-119">Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="7ec8d-120">Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="7ec8d-121">Di conseguenza, non usare il messaggio **PSM \_ REMOVEPAGE** nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="7ec8d-122">\_applica PSN</span><span class="sxs-lookup"><span data-stu-id="7ec8d-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="7ec8d-123">\_KILLACTIVE PSN</span><span class="sxs-lookup"><span data-stu-id="7ec8d-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="7ec8d-124">ripristino di PSN \_</span><span class="sxs-lookup"><span data-stu-id="7ec8d-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="7ec8d-125">seactive PSN \_</span><span class="sxs-lookup"><span data-stu-id="7ec8d-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="7ec8d-126">**eliminazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="7ec8d-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="7ec8d-127">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="7ec8d-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="7ec8d-128">Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="7ec8d-129">L'applicazione non riceverà il messaggio finché il gestore della finestra delle proprietà non avrà terminato le attività.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="7ec8d-130">È quindi possibile modificare l'elenco di pagine.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="7ec8d-131">Anche le notifiche seguenti sono interessate dalla modifica della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="7ec8d-132">\_WIZBACK PSN</span><span class="sxs-lookup"><span data-stu-id="7ec8d-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="7ec8d-133">\_WIZNEXT PSN</span><span class="sxs-lookup"><span data-stu-id="7ec8d-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="7ec8d-134">È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, a condizione che venga restituito (tramite DWL \_ MSGRESULT) un valore diverso da zero per specificare la nuova pagina desiderata.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="7ec8d-135">Si noti, tuttavia, che se si rimuove una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), [PSN \_ KILLACTIVE](psn-killactive.md) potrebbe essere inviato alla pagina errata.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec8d-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ec8d-136">Requirements</span></span>



| <span data-ttu-id="7ec8d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec8d-137">Requirement</span></span> | <span data-ttu-id="7ec8d-138">Valore</span><span class="sxs-lookup"><span data-stu-id="7ec8d-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec8d-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ec8d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec8d-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ec8d-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7ec8d-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ec8d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec8d-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ec8d-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7ec8d-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ec8d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec8d-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec8d-144"><dt>Prsht.h</dt></span></span> </dl> |



 

