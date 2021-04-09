---
title: Messaggio TCM_DESELECTALL (COMmctrl. h)
description: Reimposta gli elementi in un controllo struttura a schede, cancellando tutti i set impostati sullo \_ stato TCIS ButtonPressed. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Controlli di Windows Message TCM_DESELECTALL
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121150"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="178d6-105">\_Messaggio TCM DESELECTALL</span><span class="sxs-lookup"><span data-stu-id="178d6-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="178d6-106">Reimposta gli elementi in un controllo struttura a schede, cancellando tutti i set impostati sullo stato [**TCIS \_ ButtonPressed**](tab-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="178d6-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="178d6-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .</span><span class="sxs-lookup"><span data-stu-id="178d6-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="178d6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="178d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="178d6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="178d6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="178d6-110">Flag che specifica l'ambito della deselezione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="178d6-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="178d6-111">Se questo parametro è impostato su **false**, tutti gli elementi della scheda verranno reimpostati.</span><span class="sxs-lookup"><span data-stu-id="178d6-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="178d6-112">Se è impostato su **true**, tutti gli elementi della scheda eccetto quello attualmente selezionato verranno reimpostati.</span><span class="sxs-lookup"><span data-stu-id="178d6-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="178d6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="178d6-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="178d6-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="178d6-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="178d6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="178d6-115">Return value</span></span>

<span data-ttu-id="178d6-116">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="178d6-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="178d6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="178d6-117">Remarks</span></span>

<span data-ttu-id="178d6-118">Questo messaggio è significativo solo se è stato impostato il flag di stile dei [**\_ pulsanti TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="178d6-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="178d6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="178d6-119">Requirements</span></span>



| <span data-ttu-id="178d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="178d6-120">Requirement</span></span> | <span data-ttu-id="178d6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="178d6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="178d6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="178d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="178d6-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="178d6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="178d6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="178d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="178d6-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="178d6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="178d6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="178d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="178d6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="178d6-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





