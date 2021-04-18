---
title: Messaggio BCM_SETSPLITINFO (COMmctrl. h)
description: Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetSplitInfo macro.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Controlli di Windows Message BCM_SETSPLITINFO
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301706"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="e90f4-105">\_Messaggio SETSPLITINFO BCM</span><span class="sxs-lookup"><span data-stu-id="e90f4-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="e90f4-106">Imposta le informazioni per un controllo pulsante di divisione.</span><span class="sxs-lookup"><span data-stu-id="e90f4-106">Sets information for a split button control.</span></span> <span data-ttu-id="e90f4-107">Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span><span class="sxs-lookup"><span data-stu-id="e90f4-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e90f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e90f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e90f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e90f4-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e90f4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e90f4-111">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e90f4-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90f4-112">Puntatore a una struttura [**\_ SPLITINFO Button**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) che contiene informazioni sul pulsante di suddivisione.</span><span class="sxs-lookup"><span data-stu-id="e90f4-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90f4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e90f4-113">Return value</span></span>

<span data-ttu-id="e90f4-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e90f4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e90f4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e90f4-115">Remarks</span></span>

<span data-ttu-id="e90f4-116">Utilizzare questo messaggio solo con gli stili del pulsante [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e90f4-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90f4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90f4-117">Requirements</span></span>



| <span data-ttu-id="e90f4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90f4-118">Requirement</span></span> | <span data-ttu-id="e90f4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e90f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e90f4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e90f4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e90f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e90f4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e90f4-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e90f4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e90f4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90f4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90f4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90f4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e90f4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e90f4-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e90f4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e90f4-128">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="e90f4-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="e90f4-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e90f4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e90f4-130">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="e90f4-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





