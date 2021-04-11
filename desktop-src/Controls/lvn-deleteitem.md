---
title: Codice di notifica LVN_DELETEITEM (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- Controlli di Windows per il codice di notifica LVN_DELETEITEM
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121766"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="53c50-105">\_Codice di notifica DeleteItem di LVN</span><span class="sxs-lookup"><span data-stu-id="53c50-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="53c50-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento sta per essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="53c50-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="53c50-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="53c50-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="53c50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53c50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c50-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53c50-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53c50-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="53c50-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="53c50-111">Il membro **iItem** identifica l'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="53c50-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="53c50-112">Se il controllo non ha lo stile **\_ OWNERDATA di LVS** , il *lParam* corrisponde ai dati definiti dall'applicazione associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="53c50-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="53c50-113">Tutti gli altri membri di questa struttura sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="53c50-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c50-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53c50-114">Return value</span></span>

<span data-ttu-id="53c50-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="53c50-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c50-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="53c50-116">Remarks</span></span>

<span data-ttu-id="53c50-117">Non aggiungere, eliminare o ridisporre gli elementi nella visualizzazione elenco durante l'elaborazione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="53c50-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c50-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53c50-118">Requirements</span></span>



| <span data-ttu-id="53c50-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c50-119">Requirement</span></span> | <span data-ttu-id="53c50-120">Valore</span><span class="sxs-lookup"><span data-stu-id="53c50-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53c50-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c50-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53c50-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53c50-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53c50-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c50-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53c50-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53c50-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53c50-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53c50-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c50-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c50-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





