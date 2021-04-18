---
title: Messaggio TCM_ADJUSTRECT (COMmctrl. h)
description: Calcola l'area di visualizzazione di un controllo scheda in base a un rettangolo della finestra oppure calcola il rettangolo della finestra che corrisponderebbe a un'area di visualizzazione specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Controlli di Windows Message TCM_ADJUSTRECT
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302368"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="3fd90-105">\_Messaggio TCM ADJUSTRECT</span><span class="sxs-lookup"><span data-stu-id="3fd90-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="3fd90-106">Calcola l'area di visualizzazione di un controllo scheda in base a un rettangolo della finestra oppure calcola il rettangolo della finestra che corrisponderebbe a un'area di visualizzazione specificata.</span><span class="sxs-lookup"><span data-stu-id="3fd90-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="3fd90-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="3fd90-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fd90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fd90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd90-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fd90-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd90-110">Operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3fd90-110">Operation to perform.</span></span> <span data-ttu-id="3fd90-111">Se questo parametro è **true**, *lParam* specifica un rettangolo di visualizzazione e riceve il rettangolo della finestra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3fd90-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="3fd90-112">Se questo parametro è **false**, *lParam* specifica un rettangolo della finestra e riceve l'area di visualizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3fd90-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="3fd90-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fd90-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd90-114">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo specificato e riceve il rettangolo calcolato.</span><span class="sxs-lookup"><span data-stu-id="3fd90-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd90-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fd90-115">Return value</span></span>

<span data-ttu-id="3fd90-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3fd90-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd90-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd90-117">Remarks</span></span>

<span data-ttu-id="3fd90-118">Questo messaggio si applica solo ai controlli struttura a schede presenti nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="3fd90-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="3fd90-119">Non si applica ai controlli struttura a schede che si trovano sui lati o in basso.</span><span class="sxs-lookup"><span data-stu-id="3fd90-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd90-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd90-120">Requirements</span></span>



| <span data-ttu-id="3fd90-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd90-121">Requirement</span></span> | <span data-ttu-id="3fd90-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd90-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd90-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd90-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd90-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fd90-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd90-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd90-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fd90-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fd90-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd90-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd90-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

