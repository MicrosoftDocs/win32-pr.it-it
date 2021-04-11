---
title: Messaggio HDM_GETUNICODEFORMAT (COMmctrl. h)
description: Ottiene il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat dell'intestazione.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- Controlli di Windows Message HDM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119830"
---
# <a name="hdm_getunicodeformat-message"></a><span data-ttu-id="3ac00-105">\_Messaggio HDM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="3ac00-105">HDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="3ac00-106">Ottiene il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="3ac00-106">Gets the Unicode character format flag for the control.</span></span> <span data-ttu-id="3ac00-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="3ac00-107">You can send this message explicitly or use the [**Header\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ac00-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ac00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac00-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ac00-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ac00-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3ac00-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ac00-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ac00-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3ac00-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3ac00-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac00-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ac00-113">Return value</span></span>

<span data-ttu-id="3ac00-114">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="3ac00-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="3ac00-115">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ac00-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="3ac00-116">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="3ac00-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac00-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ac00-117">Remarks</span></span>

<span data-ttu-id="3ac00-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac00-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac00-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ac00-119">Requirements</span></span>



| <span data-ttu-id="3ac00-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac00-120">Requirement</span></span> | <span data-ttu-id="3ac00-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3ac00-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac00-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ac00-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac00-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ac00-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ac00-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ac00-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac00-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ac00-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ac00-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ac00-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac00-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac00-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac00-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ac00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac00-129">**\_SETUNICODEFORMAT HDM**</span><span class="sxs-lookup"><span data-stu-id="3ac00-129">**HDM\_SETUNICODEFORMAT**</span></span>](hdm-setunicodeformat.md)
</dt> </dl>

 

 





