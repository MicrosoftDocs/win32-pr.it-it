---
title: Messaggio TCM_HIGHLIGHTITEM (COMmctrl. h)
description: Imposta lo stato di evidenziazione di un elemento di scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Controlli di Windows Message TCM_HIGHLIGHTITEM
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874401"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="e6863-105">\_Messaggio TCM HIGHLIGHTITEM</span><span class="sxs-lookup"><span data-stu-id="e6863-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="e6863-106">Imposta lo stato di evidenziazione di un elemento di scheda.</span><span class="sxs-lookup"><span data-stu-id="e6863-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="e6863-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .</span><span class="sxs-lookup"><span data-stu-id="e6863-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6863-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6863-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6863-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6863-110">Valore **int** che specifica l'indice in base zero di un elemento di controllo Tab.</span><span class="sxs-lookup"><span data-stu-id="e6863-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="e6863-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6863-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6863-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **bool** che specifica lo stato di evidenziazione da impostare.</span><span class="sxs-lookup"><span data-stu-id="e6863-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="e6863-113">Se questo valore è **true**, la scheda è evidenziata; Se **false**, la scheda è impostata sullo stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="e6863-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="e6863-114">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6863-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6863-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6863-115">Return value</span></span>

<span data-ttu-id="e6863-116">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e6863-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6863-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6863-117">Remarks</span></span>

<span data-ttu-id="e6863-118">In Comctl32.dll versione 6,0, questo messaggio non ha alcun effetto visibile quando un tema è attivo.</span><span class="sxs-lookup"><span data-stu-id="e6863-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6863-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6863-119">Requirements</span></span>



| <span data-ttu-id="e6863-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6863-120">Requirement</span></span> | <span data-ttu-id="e6863-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e6863-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6863-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6863-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e6863-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6863-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6863-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6863-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e6863-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6863-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6863-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6863-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6863-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6863-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

