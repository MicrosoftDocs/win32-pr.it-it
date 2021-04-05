---
title: Messaggio TCM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat di TabCtrl.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- Controlli di Windows Message TCM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874402"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="ae0dd-105">\_Messaggio TCM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="ae0dd-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="ae0dd-106">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="ae0dd-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat di TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="ae0dd-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae0dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae0dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae0dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae0dd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ae0dd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ae0dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae0dd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae0dd-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae0dd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae0dd-113">Return value</span></span>

<span data-ttu-id="ae0dd-114">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="ae0dd-115">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="ae0dd-116">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae0dd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae0dd-117">Remarks</span></span>

<span data-ttu-id="ae0dd-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ae0dd-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0dd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae0dd-119">Requirements</span></span>



| <span data-ttu-id="ae0dd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae0dd-120">Requirement</span></span> | <span data-ttu-id="ae0dd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ae0dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0dd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae0dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae0dd-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae0dd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae0dd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae0dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae0dd-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae0dd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae0dd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae0dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae0dd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae0dd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae0dd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae0dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae0dd-129">**TCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ae0dd-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





