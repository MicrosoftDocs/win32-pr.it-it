---
title: Messaggio PSM_SETHEADERTITLE (Prsht. h)
description: Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHeaderTitle di PropSheet.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Controlli di Windows Message PSM_SETHEADERTITLE
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301017"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="2e5d2-105">\_Messaggio SETHEADERTITLE di PSM</span><span class="sxs-lookup"><span data-stu-id="2e5d2-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="2e5d2-106">Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="2e5d2-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="2e5d2-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .</span><span class="sxs-lookup"><span data-stu-id="2e5d2-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e5d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e5d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5d2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e5d2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5d2-110">Indice in base zero della pagina della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="2e5d2-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="2e5d2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e5d2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5d2-112">Nuovo sottotitolo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="2e5d2-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e5d2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e5d2-113">Return value</span></span>

<span data-ttu-id="2e5d2-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2e5d2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e5d2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e5d2-115">Remarks</span></span>

<span data-ttu-id="2e5d2-116">Se si specifica la pagina corrente, verrà ridisegnata immediatamente per visualizzare il nuovo titolo.</span><span class="sxs-lookup"><span data-stu-id="2e5d2-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5d2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e5d2-117">Requirements</span></span>



| <span data-ttu-id="2e5d2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5d2-118">Requirement</span></span> | <span data-ttu-id="2e5d2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2e5d2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5d2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e5d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5d2-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e5d2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e5d2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e5d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5d2-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e5d2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e5d2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e5d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5d2-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5d2-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="2e5d2-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2e5d2-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2e5d2-127">**PSM \_ SETHEADERTITLEW** (Unicode) e **PSM \_ SETHEADERTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2e5d2-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2e5d2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e5d2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e5d2-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2e5d2-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e5d2-130">**HWNDTOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="2e5d2-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="2e5d2-131">**IDTOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="2e5d2-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="2e5d2-132">**PAGETOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="2e5d2-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





