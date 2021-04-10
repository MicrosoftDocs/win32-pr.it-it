---
title: Messaggio PSM_SETHEADERSUBTITLE (Prsht. h)
description: Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHeaderSubTitle di PropSheet.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Controlli di Windows Message PSM_SETHEADERSUBTITLE
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964159"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="ec1ea-105">\_Messaggio SETHEADERSUBTITLE di PSM</span><span class="sxs-lookup"><span data-stu-id="ec1ea-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="ec1ea-106">Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="ec1ea-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="ec1ea-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderSubTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .</span><span class="sxs-lookup"><span data-stu-id="ec1ea-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec1ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec1ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec1ea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec1ea-110">Indice in base zero della pagina della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="ec1ea-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="ec1ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec1ea-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec1ea-112">Nuovo sottotitolo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ec1ea-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec1ea-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec1ea-113">Return value</span></span>

<span data-ttu-id="ec1ea-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ec1ea-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1ea-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec1ea-115">Remarks</span></span>

<span data-ttu-id="ec1ea-116">Se si specifica la pagina corrente, verrà ridisegnata immediatamente per visualizzare il nuovo sottotitolo.</span><span class="sxs-lookup"><span data-stu-id="ec1ea-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="ec1ea-117">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="ec1ea-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec1ea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec1ea-118">Requirements</span></span>



| <span data-ttu-id="ec1ea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec1ea-119">Requirement</span></span> | <span data-ttu-id="ec1ea-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ec1ea-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1ea-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec1ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1ea-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec1ea-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec1ea-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec1ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1ea-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec1ea-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec1ea-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec1ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec1ea-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec1ea-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec1ea-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ec1ea-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec1ea-128">**PSM \_ SETHEADERSUBTITLEW** (Unicode) e **PSM \_ SETHEADERSUBTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec1ea-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec1ea-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec1ea-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec1ea-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ec1ea-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ec1ea-131">**HWNDTOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="ec1ea-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="ec1ea-132">**IDTOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="ec1ea-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="ec1ea-133">**PAGETOINDEX di PSM \_**</span><span class="sxs-lookup"><span data-stu-id="ec1ea-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





