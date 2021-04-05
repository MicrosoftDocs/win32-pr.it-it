---
title: Messaggio di EM_PASTESPECIAL (RichEdit. h)
description: Incolla un formato degli Appunti specifico in un controllo Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Controlli di Windows Message EM_PASTESPECIAL
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874045"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="d556e-104">\_Messaggio PASTESPECIAL em</span><span class="sxs-lookup"><span data-stu-id="d556e-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="d556e-105">Incolla un formato degli Appunti specifico in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d556e-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d556e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d556e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d556e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d556e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d556e-108">Specifica i [formati degli Appunti](/windows/desktop/dataxchg/clipboard-formats).</span><span class="sxs-lookup"><span data-stu-id="d556e-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="d556e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d556e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d556e-110">Puntatore a una struttura [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) o **null**.</span><span class="sxs-lookup"><span data-stu-id="d556e-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="d556e-111">Se un oggetto viene incollato, la struttura **REPASTESPECIAL** viene compilata con l'aspetto di visualizzazione desiderato.</span><span class="sxs-lookup"><span data-stu-id="d556e-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="d556e-112">Se *lParam* è **null** o il membro **dwAspect** è zero, l'aspetto di visualizzazione usato sarà il contenuto del descrittore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d556e-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d556e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d556e-113">Return value</span></span>

<span data-ttu-id="d556e-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d556e-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d556e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d556e-115">Requirements</span></span>



| <span data-ttu-id="d556e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d556e-116">Requirement</span></span> | <span data-ttu-id="d556e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d556e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d556e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d556e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d556e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d556e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d556e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d556e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d556e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d556e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d556e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d556e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d556e-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d556e-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d556e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d556e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d556e-125">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="d556e-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

