---
title: Messaggio PSM_INSERTPAGE (Prsht. h)
description: Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Controlli di Windows Message PSM_INSERTPAGE
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301937"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="7d9af-106">\_Messaggio INSERTPAGE di PSM</span><span class="sxs-lookup"><span data-stu-id="7d9af-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="7d9af-107">Inserisce una nuova pagina in una finestra delle proprietà esistente.</span><span class="sxs-lookup"><span data-stu-id="7d9af-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="7d9af-108">La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata.</span><span class="sxs-lookup"><span data-stu-id="7d9af-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="7d9af-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .</span><span class="sxs-lookup"><span data-stu-id="7d9af-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d9af-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d9af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d9af-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d9af-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d9af-112">Posizione in cui deve essere inserita la pagina.</span><span class="sxs-lookup"><span data-stu-id="7d9af-112">Where the page is to be inserted.</span></span> <span data-ttu-id="7d9af-113">Impostare questo parametro su **null** per impostare la nuova pagina come prima pagina.</span><span class="sxs-lookup"><span data-stu-id="7d9af-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="7d9af-114">Per specificare dove deve essere inserita la nuova pagina, è possibile passare un indice o un handle HPROPSHEETPAGE della pagina esistente.</span><span class="sxs-lookup"><span data-stu-id="7d9af-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="7d9af-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7d9af-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="7d9af-116">Significato</span><span class="sxs-lookup"><span data-stu-id="7d9af-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d9af-117"><dt></dt><dt>Indice</dt> di</span><span class="sxs-lookup"><span data-stu-id="7d9af-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="7d9af-118">Se il parametro *wParam* è minore di MAXUSHORT (il valore integer short senza segno più grande), il *wParam* specifica l'indice in base zero per la nuova pagina.</span><span class="sxs-lookup"><span data-stu-id="7d9af-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="7d9af-119">Ad esempio, per rendere la pagina inserita la terza pagina nella finestra delle proprietà, impostare *wParam* su 2.</span><span class="sxs-lookup"><span data-stu-id="7d9af-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="7d9af-120">Per impostarla come prima pagina, impostare *wParam* su 0.</span><span class="sxs-lookup"><span data-stu-id="7d9af-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="7d9af-121">Se *wParam* ha un valore maggiore del numero di pagine e minore di MAXUSHORT, la pagina verrà accodata.</span><span class="sxs-lookup"><span data-stu-id="7d9af-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="7d9af-122"><dt></dt><dt>hpageInsertAfter</dt></span><span class="sxs-lookup"><span data-stu-id="7d9af-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="7d9af-123">Se si imposta il parametro *wParam* su un handle HPROPSHEETPAGE della pagina esistente, la nuova pagina verrà inserita dopo questa.</span><span class="sxs-lookup"><span data-stu-id="7d9af-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="7d9af-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d9af-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d9af-125">Handle per la pagina da inserire.</span><span class="sxs-lookup"><span data-stu-id="7d9af-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="7d9af-126">La pagina deve prima essere creata da una chiamata alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="7d9af-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d9af-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d9af-127">Return value</span></span>

<span data-ttu-id="7d9af-128">Restituisce un valore diverso da zero se la pagina è stata inserita correttamente oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7d9af-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d9af-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d9af-129">Remarks</span></span>

<span data-ttu-id="7d9af-130">Le pagine dopo il punto di inserimento vengono spostate verso destra per adattarsi alla nuova pagina.</span><span class="sxs-lookup"><span data-stu-id="7d9af-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="7d9af-131">La finestra delle proprietà non viene ridimensionata per adattarsi alla nuova pagina.</span><span class="sxs-lookup"><span data-stu-id="7d9af-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="7d9af-132">Non rendere la nuova pagina più grande della pagina più grande della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d9af-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="7d9af-133">Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d9af-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="7d9af-134">Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="7d9af-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="7d9af-135">Di conseguenza, non usare il messaggio PSM \_ INSERTPAGE nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.</span><span class="sxs-lookup"><span data-stu-id="7d9af-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="7d9af-136">\_applica PSN</span><span class="sxs-lookup"><span data-stu-id="7d9af-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="7d9af-137">\_KILLACTIVE PSN</span><span class="sxs-lookup"><span data-stu-id="7d9af-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="7d9af-138">ripristino di PSN \_</span><span class="sxs-lookup"><span data-stu-id="7d9af-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="7d9af-139">seactive PSN \_</span><span class="sxs-lookup"><span data-stu-id="7d9af-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="7d9af-140">**eliminazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="7d9af-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="7d9af-141">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="7d9af-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="7d9af-142">Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato.</span><span class="sxs-lookup"><span data-stu-id="7d9af-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="7d9af-143">L'applicazione non riceverà il messaggio finché il gestore della finestra delle proprietà non avrà terminato le attività.</span><span class="sxs-lookup"><span data-stu-id="7d9af-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="7d9af-144">È quindi possibile modificare l'elenco di pagine.</span><span class="sxs-lookup"><span data-stu-id="7d9af-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="7d9af-145">Anche le notifiche seguenti sono interessate dalla modifica della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d9af-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="7d9af-146">\_WIZBACK PSN</span><span class="sxs-lookup"><span data-stu-id="7d9af-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="7d9af-147">\_WIZNEXT PSN</span><span class="sxs-lookup"><span data-stu-id="7d9af-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="7d9af-148">È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, a condizione che venga restituito (tramite DWL \_ MSGRESULT) un valore diverso da zero per specificare la nuova pagina desiderata.</span><span class="sxs-lookup"><span data-stu-id="7d9af-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="7d9af-149">Si noti, tuttavia, che se si inserisce una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), [PSN \_ KILLACTIVE](psn-killactive.md) potrebbe essere inviato alla pagina errata.</span><span class="sxs-lookup"><span data-stu-id="7d9af-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="7d9af-150">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="7d9af-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d9af-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d9af-151">Requirements</span></span>



| <span data-ttu-id="7d9af-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9af-152">Requirement</span></span> | <span data-ttu-id="7d9af-153">Valore</span><span class="sxs-lookup"><span data-stu-id="7d9af-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9af-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d9af-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7d9af-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d9af-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d9af-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d9af-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7d9af-157">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d9af-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7d9af-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d9af-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d9af-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d9af-159"><dt>Prsht.h</dt></span></span> </dl> |



 

