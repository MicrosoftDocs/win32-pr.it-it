---
title: Messaggio EM_CANUNDO (winuser. h)
description: Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Controlli di Windows Message EM_CANUNDO
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120319"
---
# <a name="em_canundo-message"></a><span data-ttu-id="1a663-105">\_Messaggio CANUNDO em</span><span class="sxs-lookup"><span data-stu-id="1a663-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="1a663-106">Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="1a663-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="1a663-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1a663-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a663-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a663-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a663-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a663-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a663-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1a663-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a663-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a663-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a663-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1a663-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a663-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a663-113">Return value</span></span>

<span data-ttu-id="1a663-114">Se sono presenti azioni nella coda di annullamento del controllo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1a663-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="1a663-115">Se la coda di annullamento è vuota, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1a663-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a663-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a663-116">Remarks</span></span>

<span data-ttu-id="1a663-117">Se la coda di annullamento non è vuota, è possibile inviare il messaggio di [**\_ annullamento em**](em-undo.md) al controllo per annullare l'operazione più recente.</span><span class="sxs-lookup"><span data-stu-id="1a663-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="1a663-118">**Modificare i controlli e rich edit 1,0:** La coda di annullamento contiene solo l'operazione più recente.</span><span class="sxs-lookup"><span data-stu-id="1a663-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="1a663-119">**Rich Edit 2,0 e versioni successive:** La coda di annullamento può contenere più operazioni.</span><span class="sxs-lookup"><span data-stu-id="1a663-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="1a663-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1a663-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1a663-121">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1a663-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a663-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a663-122">Requirements</span></span>



| <span data-ttu-id="1a663-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a663-123">Requirement</span></span> | <span data-ttu-id="1a663-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1a663-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a663-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a663-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a663-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a663-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a663-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a663-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a663-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a663-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a663-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a663-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a663-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a663-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a663-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a663-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a663-132">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="1a663-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





