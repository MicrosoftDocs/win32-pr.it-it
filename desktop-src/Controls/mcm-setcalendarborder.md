---
title: Messaggio MCM_SETCALENDARBORDER (COMmctrl. h)
description: Imposta la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Controlli di Windows Message MCM_SETCALENDARBORDER
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476625"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="043a8-105">\_Messaggio SETCALENDARBORDER MCM</span><span class="sxs-lookup"><span data-stu-id="043a8-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="043a8-106">Imposta la dimensione, in pixel, del bordo.</span><span class="sxs-lookup"><span data-stu-id="043a8-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="043a8-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .</span><span class="sxs-lookup"><span data-stu-id="043a8-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="043a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="043a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="043a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="043a8-110">Se **true**, la dimensione del bordo è impostata sul numero di pixel specificato da *lParam* .</span><span class="sxs-lookup"><span data-stu-id="043a8-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="043a8-111">Se **false**, le dimensioni del bordo vengono reimpostate sul valore predefinito specificato dal tema oppure su zero se i temi non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="043a8-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="043a8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="043a8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="043a8-113">Numero di pixel della dimensione del bordo.</span><span class="sxs-lookup"><span data-stu-id="043a8-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="043a8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="043a8-114">Return value</span></span>

<span data-ttu-id="043a8-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="043a8-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="043a8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="043a8-116">Requirements</span></span>



| <span data-ttu-id="043a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="043a8-117">Requirement</span></span> | <span data-ttu-id="043a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="043a8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="043a8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="043a8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="043a8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="043a8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="043a8-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="043a8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="043a8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="043a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="043a8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="043a8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





