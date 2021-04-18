---
title: Messaggio PGM_GETBORDER (COMmctrl. h)
description: Recupera le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro pager GetBorder.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Controlli di Windows Message PGM_GETBORDER
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302051"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="d9243-105">\_Messaggio PGM GETborder</span><span class="sxs-lookup"><span data-stu-id="d9243-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="d9243-106">Recupera le dimensioni correnti del bordo per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="d9243-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="d9243-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .</span><span class="sxs-lookup"><span data-stu-id="d9243-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9243-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9243-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9243-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9243-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d9243-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9243-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d9243-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9243-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9243-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9243-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9243-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9243-113">Return value</span></span>

<span data-ttu-id="d9243-114">Restituisce un valore INT che contiene le dimensioni correnti del bordo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="d9243-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9243-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9243-115">Requirements</span></span>



| <span data-ttu-id="d9243-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9243-116">Requirement</span></span> | <span data-ttu-id="d9243-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d9243-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9243-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9243-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9243-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9243-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9243-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9243-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9243-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9243-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9243-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9243-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9243-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9243-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9243-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9243-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9243-125">**PGM ( \_ bordo)**</span><span class="sxs-lookup"><span data-stu-id="d9243-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





