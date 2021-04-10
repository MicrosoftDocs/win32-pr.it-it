---
title: Messaggio TCM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip associato a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Controlli di Windows Message TCM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121142"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="925b2-105">\_Messaggio TCM GETtooltips</span><span class="sxs-lookup"><span data-stu-id="925b2-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="925b2-106">Recupera l'handle per il controllo ToolTip associato a un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="925b2-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="925b2-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="925b2-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="925b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="925b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="925b2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="925b2-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="925b2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="925b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="925b2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="925b2-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="925b2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="925b2-113">Return value</span></span>

<span data-ttu-id="925b2-114">Restituisce l'handle per il controllo ToolTip se ha esito positivo o **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="925b2-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="925b2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="925b2-115">Remarks</span></span>

<span data-ttu-id="925b2-116">Un controllo struttura a schede crea un controllo ToolTip se dispone dello stile [**\_ Descrizione comando TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="925b2-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="925b2-117">È anche possibile assegnare un controllo ToolTip a un controllo struttura a schede usando il messaggio [**TCM \_ setooltips**](tcm-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="925b2-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="925b2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="925b2-118">Requirements</span></span>



| <span data-ttu-id="925b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="925b2-119">Requirement</span></span> | <span data-ttu-id="925b2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="925b2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="925b2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="925b2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="925b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="925b2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="925b2-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="925b2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="925b2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="925b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="925b2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="925b2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





