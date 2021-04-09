---
title: Messaggio di EM_GETEVENTMASK (RichEdit. h)
description: Recupera la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Controlli di Windows Message EM_GETEVENTMASK
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964581"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="d61c1-105">\_Messaggio GETEVENTMASK em</span><span class="sxs-lookup"><span data-stu-id="d61c1-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="d61c1-106">Recupera la maschera di eventi per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d61c1-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="d61c1-107">La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="d61c1-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d61c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d61c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d61c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d61c1-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d61c1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d61c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d61c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d61c1-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d61c1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d61c1-113">Return value</span></span>

<span data-ttu-id="d61c1-114">Questo messaggio restituisce la maschera eventi per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d61c1-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d61c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d61c1-115">Requirements</span></span>



| <span data-ttu-id="d61c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d61c1-116">Requirement</span></span> | <span data-ttu-id="d61c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d61c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d61c1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d61c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d61c1-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d61c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d61c1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d61c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d61c1-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d61c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d61c1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d61c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61c1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d61c1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d61c1-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="d61c1-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d61c1-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d61c1-126">**\_SETEVENTMASK em**</span><span class="sxs-lookup"><span data-stu-id="d61c1-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="d61c1-127">**Flag di maschera eventi controllo Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="d61c1-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





