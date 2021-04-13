---
title: Messaggio MCM_GETCALENDARBORDER (COMmctrl. h)
description: Ottiene la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCurrentView.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- Controlli di Windows Message MCM_GETCALENDARBORDER
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518292"
---
# <a name="mcm_getcalendarborder-message"></a><span data-ttu-id="31c91-105">\_Messaggio GETCALENDARBORDER MCM</span><span class="sxs-lookup"><span data-stu-id="31c91-105">MCM\_GETCALENDARBORDER message</span></span>

<span data-ttu-id="31c91-106">Ottiene la dimensione, in pixel, del bordo.</span><span class="sxs-lookup"><span data-stu-id="31c91-106">Gets the size of the border, in pixels.</span></span> <span data-ttu-id="31c91-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="31c91-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="31c91-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="31c91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31c91-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31c91-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31c91-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="31c91-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31c91-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31c91-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31c91-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c91-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31c91-113">Return value</span></span>

<span data-ttu-id="31c91-114">Dimensioni del bordo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="31c91-114">Border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c91-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31c91-115">Requirements</span></span>



| <span data-ttu-id="31c91-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c91-116">Requirement</span></span> | <span data-ttu-id="31c91-117">Valore</span><span class="sxs-lookup"><span data-stu-id="31c91-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31c91-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31c91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31c91-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31c91-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31c91-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31c91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31c91-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31c91-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31c91-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31c91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c91-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c91-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





