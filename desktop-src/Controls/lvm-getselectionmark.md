---
title: Messaggio LVM_GETSELECTIONMARK (COMmctrl. h)
description: Recupera il contrassegno di selezione da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetSelectionMark di ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Controlli di Windows Message LVM_GETSELECTIONMARK
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302294"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="755e2-105">\_Messaggio GETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="755e2-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="755e2-106">Recupera il contrassegno di selezione da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="755e2-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="755e2-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetSelectionMark di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="755e2-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="755e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="755e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="755e2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="755e2-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="755e2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="755e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="755e2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="755e2-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="755e2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="755e2-113">Return value</span></span>

<span data-ttu-id="755e2-114">Restituisce il contrassegno di selezione in base zero oppure-1 se non è presente alcun contrassegno di selezione.</span><span class="sxs-lookup"><span data-stu-id="755e2-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="755e2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="755e2-115">Remarks</span></span>

<span data-ttu-id="755e2-116">Il *contrassegno di selezione* è l'indice dell'elemento da cui inizia una selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="755e2-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="755e2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="755e2-117">Requirements</span></span>



| <span data-ttu-id="755e2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="755e2-118">Requirement</span></span> | <span data-ttu-id="755e2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="755e2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="755e2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="755e2-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="755e2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="755e2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="755e2-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="755e2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="755e2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="755e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="755e2-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="755e2-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755e2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="755e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755e2-127">**\_SETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="755e2-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





