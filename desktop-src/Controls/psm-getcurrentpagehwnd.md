---
title: Messaggio PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Controlli di Windows Message PSM_GETCURRENTPAGEHWND
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302200"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="19c14-105">\_Messaggio GETCURRENTPAGEHWND di PSM</span><span class="sxs-lookup"><span data-stu-id="19c14-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="19c14-106">Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="19c14-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="19c14-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .</span><span class="sxs-lookup"><span data-stu-id="19c14-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19c14-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19c14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c14-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19c14-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19c14-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="19c14-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19c14-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19c14-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19c14-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="19c14-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c14-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19c14-113">Return value</span></span>

<span data-ttu-id="19c14-114">Restituisce un handle per la finestra della pagina della finestra delle proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="19c14-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c14-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="19c14-115">Remarks</span></span>

<span data-ttu-id="19c14-116">Usare il messaggio **PSM \_ GETCURRENTPAGEHWND** con le finestre delle proprietà non modali per determinare quando eliminare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="19c14-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="19c14-117">Quando l'utente fa clic sul pulsante **OK** o **Annulla** , **PSM \_ GETCURRENTPAGEHWND** restituisce **null** ed è quindi possibile usare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="19c14-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="19c14-118">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="19c14-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19c14-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19c14-119">Requirements</span></span>



| <span data-ttu-id="19c14-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c14-120">Requirement</span></span> | <span data-ttu-id="19c14-121">Valore</span><span class="sxs-lookup"><span data-stu-id="19c14-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19c14-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c14-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19c14-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19c14-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19c14-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c14-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19c14-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19c14-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19c14-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19c14-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c14-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c14-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c14-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19c14-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c14-129">**PropertySheet**</span><span class="sxs-lookup"><span data-stu-id="19c14-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

