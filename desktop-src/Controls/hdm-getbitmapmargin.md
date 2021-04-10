---
title: Messaggio HDM_GETBITMAPMARGIN (COMmctrl. h)
description: Ottiene la larghezza del margine bitmap per un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetBitmapMargin dell'intestazione.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Controlli di Windows Message HDM_GETBITMAPMARGIN
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964260"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="28082-105">\_Messaggio HDM GETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="28082-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="28082-106">Ottiene la larghezza del margine bitmap per un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="28082-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="28082-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetBitmapMargin dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="28082-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="28082-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="28082-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28082-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28082-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="28082-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="28082-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="28082-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28082-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="28082-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="28082-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28082-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28082-113">Return value</span></span>

<span data-ttu-id="28082-114">Restituisce la larghezza del margine della bitmap in pixel.</span><span class="sxs-lookup"><span data-stu-id="28082-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="28082-115">Se il margine bitmap non è stato specificato in precedenza, viene restituito il valore predefinito 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE).</span><span class="sxs-lookup"><span data-stu-id="28082-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="28082-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28082-116">Requirements</span></span>



| <span data-ttu-id="28082-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28082-117">Requirement</span></span> | <span data-ttu-id="28082-118">Valore</span><span class="sxs-lookup"><span data-stu-id="28082-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28082-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28082-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28082-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28082-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28082-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28082-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28082-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28082-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28082-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28082-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28082-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28082-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28082-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28082-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28082-126">**\_SETBITMAPMARGIN HDM**</span><span class="sxs-lookup"><span data-stu-id="28082-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

