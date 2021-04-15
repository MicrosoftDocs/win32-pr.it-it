---
title: Codice di notifica HDN_ENDDRAG (COMmctrl. h)
description: Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi. Questo codice di notifica viene inviato come un \_ messaggio di notifica WM. Solo i controlli intestazione impostati sullo \_ stile DragDrop di HDS inviano il codice di notifica.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDDRAG
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479456"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="e6200-106">\_Codice di notifica ENDDRAG di HDN</span><span class="sxs-lookup"><span data-stu-id="e6200-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="e6200-107">Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="e6200-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="e6200-108">Questo codice di notifica viene inviato come un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e6200-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="e6200-109">Solo i controlli intestazione impostati sullo stile [**\_ DragDrop di HDS**](header-control-styles.md) inviano il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e6200-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e6200-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6200-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6200-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6200-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6200-112">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento dell'intestazione trascinato.</span><span class="sxs-lookup"><span data-stu-id="e6200-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6200-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6200-113">Return value</span></span>

<span data-ttu-id="e6200-114">Per consentire al controllo di posizionare e riordinare automaticamente l'elemento, restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="e6200-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="e6200-115">Per impedire che l'elemento venga inserito, restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="e6200-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6200-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6200-116">Remarks</span></span>

<span data-ttu-id="e6200-117">Se il proprietario sta eseguendo la gestione del trascinamento della selezione esterna (manuale), deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="e6200-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="e6200-118">Il proprietario deve quindi riordinare manualmente gli elementi di intestazione inviando [**HDM \_ SetItem**](hdm-setitem.md) o [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).</span><span class="sxs-lookup"><span data-stu-id="e6200-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6200-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6200-119">Requirements</span></span>



| <span data-ttu-id="e6200-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6200-120">Requirement</span></span> | <span data-ttu-id="e6200-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e6200-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6200-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6200-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e6200-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6200-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6200-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6200-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e6200-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6200-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6200-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6200-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6200-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6200-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





