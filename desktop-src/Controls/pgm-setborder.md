---
title: Messaggio PGM_SETBORDER (COMmctrl. h)
description: Imposta la dimensione corrente del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro pager di pager \_ .
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Controlli di Windows Message PGM_SETBORDER
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048260"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="b04b5-105">\_Messaggio di DEBORDO PGM</span><span class="sxs-lookup"><span data-stu-id="b04b5-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="b04b5-106">Imposta la dimensione corrente del bordo per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="b04b5-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="b04b5-107">È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro pager di pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .</span><span class="sxs-lookup"><span data-stu-id="b04b5-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b04b5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b04b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b04b5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b04b5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b04b5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b04b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b04b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b04b5-112">Nuove dimensioni del bordo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b04b5-112">New size of the border, in pixels.</span></span> <span data-ttu-id="b04b5-113">Il valore non deve essere maggiore del pulsante cercapersone o minore di zero.</span><span class="sxs-lookup"><span data-stu-id="b04b5-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="b04b5-114">Se *lParam* è troppo grande, il bordo verrà disegnato con le stesse dimensioni del pulsante.</span><span class="sxs-lookup"><span data-stu-id="b04b5-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="b04b5-115">Se *lParam* è negativo, la dimensione del bordo verrà impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="b04b5-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04b5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b04b5-116">Return value</span></span>

<span data-ttu-id="b04b5-117">Restituisce un valore INT che contiene le dimensioni del bordo precedenti, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b04b5-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b04b5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b04b5-118">Requirements</span></span>



| <span data-ttu-id="b04b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04b5-119">Requirement</span></span> | <span data-ttu-id="b04b5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b04b5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b04b5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b04b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b04b5-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b04b5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b04b5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b04b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b04b5-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b04b5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b04b5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b04b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04b5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04b5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





