---
title: Messaggio MCM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat di MonthCal.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- Controlli di Windows Message MCM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743575"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="5f32e-105">\_Messaggio GETUNICODEFORMAT MCM</span><span class="sxs-lookup"><span data-stu-id="5f32e-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="5f32e-106">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="5f32e-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="5f32e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat di MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="5f32e-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f32e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f32e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f32e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f32e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f32e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5f32e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f32e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f32e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f32e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5f32e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f32e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f32e-113">Return value</span></span>

<span data-ttu-id="5f32e-114">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="5f32e-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="5f32e-115">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f32e-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="5f32e-116">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="5f32e-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f32e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f32e-117">Remarks</span></span>

<span data-ttu-id="5f32e-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="5f32e-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f32e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f32e-119">Requirements</span></span>



| <span data-ttu-id="5f32e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f32e-120">Requirement</span></span> | <span data-ttu-id="5f32e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5f32e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f32e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f32e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f32e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f32e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f32e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f32e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f32e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f32e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f32e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f32e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f32e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f32e-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f32e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f32e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f32e-129">**\_SETUNICODEFORMAT MCM**</span><span class="sxs-lookup"><span data-stu-id="5f32e-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





