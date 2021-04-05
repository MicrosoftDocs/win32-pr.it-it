---
title: Codice di notifica HDN_BEGINDRAG (COMmctrl. h)
description: Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno degli elementi. Questo codice di notifica viene inviato solo da controlli intestazione impostati sullo \_ stile DragDrop di HDS. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINDRAG
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048296"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="8164e-106">\_Codice di notifica BEGINDRAG di HDN</span><span class="sxs-lookup"><span data-stu-id="8164e-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="8164e-107">Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="8164e-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="8164e-108">Questo codice di notifica viene inviato solo da controlli intestazione impostati sullo stile [**\_ DragDrop di HDS**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8164e-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="8164e-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8164e-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8164e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8164e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8164e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8164e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8164e-112">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento dell'intestazione trascinato.</span><span class="sxs-lookup"><span data-stu-id="8164e-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8164e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8164e-113">Return value</span></span>

<span data-ttu-id="8164e-114">Per consentire al controllo intestazione di gestire automaticamente le operazioni di trascinamento della selezione, restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="8164e-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="8164e-115">Se il proprietario del controllo esegue manualmente il riordinamento con trascinamento della selezione, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="8164e-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8164e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8164e-116">Remarks</span></span>

<span data-ttu-id="8164e-117">Per impostazione predefinita, il controllo dell'intestazione gestisce automaticamente il riordinamento con trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="8164e-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="8164e-118">Restituisce **true** per indicare che la gestione esterna (manuale) del trascinamento della selezione consente al proprietario del controllo di fornire servizi personalizzati come parte del processo di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="8164e-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="8164e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8164e-119">Requirements</span></span>



| <span data-ttu-id="8164e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8164e-120">Requirement</span></span> | <span data-ttu-id="8164e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8164e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8164e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8164e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8164e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8164e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8164e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8164e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8164e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8164e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8164e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8164e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8164e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8164e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





