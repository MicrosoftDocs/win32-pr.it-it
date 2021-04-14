---
title: Messaggio di EM_SETEVENTMASK (RichEdit. h)
description: Imposta la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Controlli di Windows Message EM_SETEVENTMASK
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478568"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="a2ae1-105">\_Messaggio SETEVENTMASK em</span><span class="sxs-lookup"><span data-stu-id="a2ae1-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="a2ae1-106">Imposta la maschera di eventi per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="a2ae1-107">La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2ae1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2ae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ae1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2ae1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ae1-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2ae1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2ae1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ae1-112">Nuova maschera eventi per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="a2ae1-113">Per un elenco di maschere di eventi, vedere [**flag di maschera eventi del controllo Rich Edit**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a2ae1-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ae1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2ae1-114">Return value</span></span>

<span data-ttu-id="a2ae1-115">Questo messaggio restituisce la maschera eventi precedente.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ae1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2ae1-116">Remarks</span></span>

<span data-ttu-id="a2ae1-117">La maschera di eventi predefinita (prima che sia impostato) è ENM \_ None.</span><span class="sxs-lookup"><span data-stu-id="a2ae1-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ae1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2ae1-118">Requirements</span></span>



| <span data-ttu-id="a2ae1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ae1-119">Requirement</span></span> | <span data-ttu-id="a2ae1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a2ae1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ae1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2ae1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ae1-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2ae1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2ae1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2ae1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ae1-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2ae1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2ae1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2ae1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ae1-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ae1-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ae1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2ae1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2ae1-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a2ae1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a2ae1-129">**\_GETEVENTMASK em**</span><span class="sxs-lookup"><span data-stu-id="a2ae1-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="a2ae1-130">**Flag di maschera eventi controllo Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="a2ae1-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





