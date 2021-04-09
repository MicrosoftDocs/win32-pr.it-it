---
title: Messaggio TCM_SETTOOLTIPS (COMmctrl. h)
description: Assegna un controllo ToolTip a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl di descrizione comando.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Controlli di Windows Message TCM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739871"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="23993-105">\_Messaggio TCM SEtooltips</span><span class="sxs-lookup"><span data-stu-id="23993-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="23993-106">Assegna un controllo ToolTip a un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="23993-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="23993-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl di \_ Descrizione comando**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="23993-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="23993-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23993-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23993-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23993-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23993-110">Handle per il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="23993-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="23993-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23993-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23993-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23993-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23993-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23993-113">Return value</span></span>

<span data-ttu-id="23993-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="23993-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23993-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="23993-115">Remarks</span></span>

<span data-ttu-id="23993-116">È possibile recuperare il controllo ToolTip associato a un controllo struttura a schede usando il messaggio [**TCM \_ GetToolTips**](tcm-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="23993-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="23993-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23993-117">Requirements</span></span>



| <span data-ttu-id="23993-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="23993-118">Requirement</span></span> | <span data-ttu-id="23993-119">Valore</span><span class="sxs-lookup"><span data-stu-id="23993-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23993-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23993-120">Minimum supported client</span></span><br/> | <span data-ttu-id="23993-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23993-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23993-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23993-122">Minimum supported server</span></span><br/> | <span data-ttu-id="23993-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23993-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23993-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23993-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="23993-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23993-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





