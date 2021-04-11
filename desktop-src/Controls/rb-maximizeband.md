---
title: Messaggio RB_MAXIMIZEBAND (COMmctrl. h)
description: Ridimensiona una banda in un controllo Rebar alla dimensione ideale o più grande.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Controlli di Windows Message RB_MAXIMIZEBAND
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874153"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="e5b8e-104">\_Messaggio MAXIMIZEBAND RB</span><span class="sxs-lookup"><span data-stu-id="e5b8e-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="e5b8e-105">Ridimensiona una banda in un controllo Rebar alla dimensione ideale o più grande.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5b8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5b8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b8e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5b8e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b8e-108">Indice in base zero della banda da ingrandire.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="e5b8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5b8e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b8e-110">Indica se la larghezza ideale della banda deve essere utilizzata quando la banda è ingrandita.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="e5b8e-111">Se questo valore è diverso da zero, verrà utilizzata la larghezza ideale.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="e5b8e-112">Se questo valore è zero, la banda verrà resa il più possibile grande.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b8e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5b8e-113">Return value</span></span>

<span data-ttu-id="e5b8e-114">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e5b8e-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b8e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5b8e-115">Requirements</span></span>



| <span data-ttu-id="e5b8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b8e-116">Requirement</span></span> | <span data-ttu-id="e5b8e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b8e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b8e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b8e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b8e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5b8e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5b8e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b8e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b8e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5b8e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5b8e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5b8e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b8e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b8e-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b8e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5b8e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5b8e-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e5b8e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5b8e-126">**RB \_ SETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="e5b8e-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





