---
title: Messaggio BCM_SETTEXTMARGIN (COMmctrl. h)
description: Il \_ messaggio BCM SETTEXTMARGIN imposta i margini per il disegno di testo in un controllo Button.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- Controlli di Windows Message BCM_SETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476660"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="e1f4d-104">\_Messaggio SETTEXTMARGIN BCM</span><span class="sxs-lookup"><span data-stu-id="e1f4d-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="e1f4d-105">Il messaggio **BCM \_ SETTEXTMARGIN** imposta i margini per il disegno di testo in un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1f4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1f4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f4d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1f4d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f4d-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e1f4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1f4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f4d-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica i margini da utilizzare per il disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f4d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1f4d-111">Return value</span></span>

<span data-ttu-id="e1f4d-112">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="e1f4d-113">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f4d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1f4d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e1f4d-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="e1f4d-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e1f4d-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e1f4d-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1f4d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1f4d-117">Requirements</span></span>



| <span data-ttu-id="e1f4d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1f4d-118">Requirement</span></span> | <span data-ttu-id="e1f4d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e1f4d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f4d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1f4d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f4d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1f4d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1f4d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1f4d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f4d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1f4d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1f4d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1f4d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1f4d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1f4d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f4d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1f4d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1f4d-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e1f4d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1f4d-128">**Pulsante \_ SetTextMargin**</span><span class="sxs-lookup"><span data-stu-id="e1f4d-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="e1f4d-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e1f4d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1f4d-130">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="e1f4d-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

