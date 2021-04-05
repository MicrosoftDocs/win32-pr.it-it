---
title: Messaggio EM_GETMARGINS (winuser. h)
description: Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Controlli di Windows Message EM_GETMARGINS
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740298"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="cb5c2-104">\_Messaggio GETmargins em</span><span class="sxs-lookup"><span data-stu-id="cb5c2-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="cb5c2-105">Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb5c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb5c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb5c2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb5c2-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb5c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb5c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb5c2-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5c2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb5c2-111">Return value</span></span>

<span data-ttu-id="cb5c2-112">Restituisce la larghezza del margine sinistro in LOWORD e la larghezza del margine destro in HIWORD.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5c2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb5c2-113">Remarks</span></span>

<span data-ttu-id="cb5c2-114">**Modifica avanzata:** Il **messaggio \_ GetMargins em** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cb5c2-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb5c2-115">Requirements</span></span>



| <span data-ttu-id="cb5c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5c2-116">Requirement</span></span> | <span data-ttu-id="cb5c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cb5c2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5c2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb5c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5c2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb5c2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb5c2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb5c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5c2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb5c2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb5c2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb5c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb5c2-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5c2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb5c2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb5c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5c2-125">**\_margini em**</span><span class="sxs-lookup"><span data-stu-id="cb5c2-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





