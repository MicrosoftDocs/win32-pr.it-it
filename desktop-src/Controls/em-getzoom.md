---
title: Messaggio di EM_GETZOOM (RichEdit. h)
description: Ottiene la percentuale di zoom corrente. Il razionamento dello zoom è sempre compreso tra 1/64 e 64. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Controlli di Windows Message EM_GETZOOM
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740295"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="37aac-106">\_Messaggio GETZOOM em</span><span class="sxs-lookup"><span data-stu-id="37aac-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="37aac-107">Ottiene la percentuale di zoom corrente per un controllo di modifica su più righe o un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="37aac-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="37aac-108">Il razionamento dello zoom è sempre compreso tra 1/64 e 64.</span><span class="sxs-lookup"><span data-stu-id="37aac-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="37aac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="37aac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37aac-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37aac-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37aac-111">Riceve il numeratore del rapporto di zoom.</span><span class="sxs-lookup"><span data-stu-id="37aac-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="37aac-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37aac-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37aac-113">Riceve il denominatore del rapporto di zoom.</span><span class="sxs-lookup"><span data-stu-id="37aac-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37aac-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37aac-114">Return value</span></span>

<span data-ttu-id="37aac-115">Il messaggio restituisce **true** se il messaggio viene elaborato, che sarà se *wParam* e *lParam* non sono **null**.</span><span class="sxs-lookup"><span data-stu-id="37aac-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37aac-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="37aac-116">Remarks</span></span>

<span data-ttu-id="37aac-117">**Modifica:** Supportato in Windows 10 1809 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37aac-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="37aac-118">Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="37aac-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="37aac-119">Per informazioni sul controllo di modifica, vedere [modificare i controlli](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="37aac-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37aac-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37aac-120">Requirements</span></span>



| <span data-ttu-id="37aac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37aac-121">Requirement</span></span> | <span data-ttu-id="37aac-122">Valore</span><span class="sxs-lookup"><span data-stu-id="37aac-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37aac-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37aac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37aac-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37aac-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37aac-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37aac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37aac-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37aac-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37aac-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="37aac-127">Redistributable</span></span><br/>          | <span data-ttu-id="37aac-128">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="37aac-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="37aac-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37aac-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="37aac-130"><dt>RichEdit. h/COMmctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37aac-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37aac-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37aac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37aac-132">**\_Zoom em**</span><span class="sxs-lookup"><span data-stu-id="37aac-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





