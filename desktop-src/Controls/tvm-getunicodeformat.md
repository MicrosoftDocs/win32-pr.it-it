---
title: Messaggio TVM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat di TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- Controlli di Windows Message TVM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048103"
---
# <a name="tvm_getunicodeformat-message"></a><span data-ttu-id="e4de6-105">\_Messaggio GETUNICODEFORMAT TVM</span><span class="sxs-lookup"><span data-stu-id="e4de6-105">TVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="e4de6-106">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="e4de6-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="e4de6-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="e4de6-107">You can send this message explicitly or use the [**TreeView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4de6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4de6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4de6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4de6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e4de6-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e4de6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e4de6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4de6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e4de6-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e4de6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4de6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4de6-113">Return value</span></span>

<span data-ttu-id="e4de6-114">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="e4de6-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="e4de6-115">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4de6-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="e4de6-116">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="e4de6-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4de6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4de6-117">Remarks</span></span>

<span data-ttu-id="e4de6-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="e4de6-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4de6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4de6-119">Requirements</span></span>



| <span data-ttu-id="e4de6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4de6-120">Requirement</span></span> | <span data-ttu-id="e4de6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4de6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4de6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4de6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4de6-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4de6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4de6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4de6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4de6-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4de6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4de6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4de6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4de6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4de6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4de6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4de6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4de6-129">**\_SETUNICODEFORMAT TVM**</span><span class="sxs-lookup"><span data-stu-id="e4de6-129">**TVM\_SETUNICODEFORMAT**</span></span>](tvm-setunicodeformat.md)
</dt> </dl>

 

 





