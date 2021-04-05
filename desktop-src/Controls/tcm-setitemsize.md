---
title: Messaggio TCM_SETITEMSIZE (COMmctrl. h)
description: Imposta la larghezza e l'altezza delle schede in un controllo struttura a larghezza fissa o disegnato dal proprietario. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Controlli di Windows Message TCM_SETITEMSIZE
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873277"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="9b1be-105">\_Messaggio TCM SETITEMSIZE</span><span class="sxs-lookup"><span data-stu-id="9b1be-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="9b1be-106">Imposta la larghezza e l'altezza delle schede in un controllo struttura a larghezza fissa o disegnato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="9b1be-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="9b1be-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .</span><span class="sxs-lookup"><span data-stu-id="9b1be-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b1be-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b1be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b1be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b1be-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9b1be-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9b1be-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9b1be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b1be-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b1be-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **int** che specifica la nuova larghezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="9b1be-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="9b1be-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **int** che specifica la nuova altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="9b1be-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b1be-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b1be-114">Return value</span></span>

<span data-ttu-id="9b1be-115">Restituisce la larghezza e l'altezza precedenti.</span><span class="sxs-lookup"><span data-stu-id="9b1be-115">Returns the old width and height.</span></span> <span data-ttu-id="9b1be-116">La larghezza si trova nell' [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e l'altezza si trova in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b1be-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b1be-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b1be-117">Remarks</span></span>

<span data-ttu-id="9b1be-118">Se la larghezza è impostata su un valore minore della larghezza dell'immagine impostata da [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), la larghezza della scheda viene impostata sul valore più basso maggiore della larghezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="9b1be-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b1be-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b1be-119">Requirements</span></span>



| <span data-ttu-id="9b1be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b1be-120">Requirement</span></span> | <span data-ttu-id="9b1be-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9b1be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b1be-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b1be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b1be-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b1be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b1be-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b1be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b1be-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b1be-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b1be-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b1be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b1be-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b1be-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

