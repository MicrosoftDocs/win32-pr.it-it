---
title: Messaggio di EM_SETZOOM (RichEdit. h)
description: Imposta il rapporto di zoom. Il rapporto deve essere un valore compreso tra 1/64 e 64. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Controlli di Windows Message EM_SETZOOM
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874030"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="d4e0a-106">\_Messaggio di ridimensionamento em</span><span class="sxs-lookup"><span data-stu-id="d4e0a-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="d4e0a-107">Imposta la percentuale di zoom per un controllo di modifica su più righe o un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="d4e0a-108">Il rapporto deve essere un valore compreso tra 1/64 e 64.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="d4e0a-109">Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0a-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="d4e0a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4e0a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e0a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4e0a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e0a-112">Numeratore del rapporto di zoom.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="d4e0a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4e0a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e0a-114">Denominatore del rapporto di zoom.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="d4e0a-115">Questi parametri possono avere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="d4e0a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4e0a-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="d4e0a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="d4e0a-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="d4e0a-118"><dt>**Entrambi 0**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e0a-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="d4e0a-119">Disattiva lo zoom usando il messaggio di **Zoom \_ em** . è possibile che si verifichi ancora lo zoom usando [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent).</span><span class="sxs-lookup"><span data-stu-id="d4e0a-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="d4e0a-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e0a-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="d4e0a-121">Consente di ingrandire la visualizzazione del numeratore/denominatore della percentuale di zoom</span><span class="sxs-lookup"><span data-stu-id="d4e0a-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e0a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4e0a-122">Return value</span></span>

<span data-ttu-id="d4e0a-123">Se viene accettata la nuova impostazione di zoom, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="d4e0a-124">Se la nuova impostazione di zoom non viene accettata, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4e0a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4e0a-125">Remarks</span></span>

<span data-ttu-id="d4e0a-126">**Modifica:** Supportato in Windows 10 1809 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d4e0a-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="d4e0a-127">Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0a-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="d4e0a-128">Per informazioni sul controllo di modifica, vedere [modificare i controlli](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d4e0a-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e0a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4e0a-129">Requirements</span></span>



| <span data-ttu-id="d4e0a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e0a-130">Requirement</span></span> | <span data-ttu-id="d4e0a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d4e0a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e0a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4e0a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4e0a-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4e0a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4e0a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4e0a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4e0a-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4e0a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4e0a-136">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d4e0a-136">Redistributable</span></span><br/>          | <span data-ttu-id="d4e0a-137">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="d4e0a-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="d4e0a-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4e0a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4e0a-139"><dt>RichEdit. h/COMmctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e0a-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e0a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4e0a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e0a-141">**EM \_ GETzoom**</span><span class="sxs-lookup"><span data-stu-id="d4e0a-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





