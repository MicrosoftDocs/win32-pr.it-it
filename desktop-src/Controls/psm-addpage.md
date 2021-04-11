---
title: Messaggio PSM_ADDPAGE (Prsht. h)
description: Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro PropSheet di AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Controlli di Windows Message PSM_ADDPAGE
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874258"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="9df72-105">\_Messaggio ADDPAGE di PSM</span><span class="sxs-lookup"><span data-stu-id="9df72-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="9df72-106">Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente.</span><span class="sxs-lookup"><span data-stu-id="9df72-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="9df72-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet di \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .</span><span class="sxs-lookup"><span data-stu-id="9df72-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9df72-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9df72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9df72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df72-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9df72-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9df72-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9df72-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df72-112">Handle per la pagina da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9df72-112">Handle to the page to add.</span></span> <span data-ttu-id="9df72-113">La pagina deve essere stata creata da una chiamata precedente alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="9df72-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df72-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9df72-114">Return value</span></span>

<span data-ttu-id="9df72-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9df72-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df72-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9df72-116">Remarks</span></span>

<span data-ttu-id="9df72-117">La nuova pagina non deve essere maggiore della pagina più grande attualmente nella finestra delle proprietà perché la finestra delle proprietà non viene ridimensionata per adattarsi alla nuova pagina.</span><span class="sxs-lookup"><span data-stu-id="9df72-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="9df72-118">Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9df72-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="9df72-119">Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="9df72-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="9df72-120">Di conseguenza, non è consigliabile usare il \_ messaggio ADDPAGE di PSM nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.</span><span class="sxs-lookup"><span data-stu-id="9df72-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="9df72-121">\_applica PSN</span><span class="sxs-lookup"><span data-stu-id="9df72-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="9df72-122">\_KILLACTIVE PSN</span><span class="sxs-lookup"><span data-stu-id="9df72-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="9df72-123">ripristino di PSN \_</span><span class="sxs-lookup"><span data-stu-id="9df72-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="9df72-124">seactive PSN \_</span><span class="sxs-lookup"><span data-stu-id="9df72-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="9df72-125">**eliminazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="9df72-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="9df72-126">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="9df72-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="9df72-127">Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato.</span><span class="sxs-lookup"><span data-stu-id="9df72-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="9df72-128">L'applicazione non riceverà il messaggio finché il gestore della finestra delle proprietà non avrà terminato le attività.</span><span class="sxs-lookup"><span data-stu-id="9df72-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="9df72-129">È quindi possibile modificare l'elenco di pagine.</span><span class="sxs-lookup"><span data-stu-id="9df72-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df72-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9df72-130">Requirements</span></span>



| <span data-ttu-id="9df72-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df72-131">Requirement</span></span> | <span data-ttu-id="9df72-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9df72-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9df72-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df72-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9df72-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9df72-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9df72-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df72-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9df72-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9df72-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9df72-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9df72-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df72-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df72-138"><dt>Prsht.h</dt></span></span> </dl> |



 

