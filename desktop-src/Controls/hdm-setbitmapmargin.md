---
title: Messaggio HDM_SETBITMAPMARGIN (COMmctrl. h)
description: Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetBitmapMargin dell'intestazione.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Controlli di Windows Message HDM_SETBITMAPMARGIN
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874269"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="c02fb-105">\_Messaggio HDM SETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="c02fb-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="c02fb-106">Imposta la larghezza del margine, espressa in pixel, di una bitmap in un controllo intestazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c02fb-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="c02fb-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetBitmapMargin dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="c02fb-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c02fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c02fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c02fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c02fb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c02fb-110">Larghezza, espressa in pixel, del margine che racchiude una bitmap all'interno di un controllo intestazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c02fb-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="c02fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c02fb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c02fb-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c02fb-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c02fb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c02fb-113">Return value</span></span>

<span data-ttu-id="c02fb-114">Restituisce la larghezza, in pixel, del margine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c02fb-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="c02fb-115">Se il margine bitmap non è stato specificato in precedenza, viene restituito il valore predefinito 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*).</span><span class="sxs-lookup"><span data-stu-id="c02fb-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c02fb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c02fb-116">Requirements</span></span>



| <span data-ttu-id="c02fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c02fb-117">Requirement</span></span> | <span data-ttu-id="c02fb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c02fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c02fb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c02fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c02fb-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c02fb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c02fb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c02fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c02fb-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c02fb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c02fb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c02fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02fb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02fb-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02fb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c02fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02fb-126">**\_GETBITMAPMARGIN HDM**</span><span class="sxs-lookup"><span data-stu-id="c02fb-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

