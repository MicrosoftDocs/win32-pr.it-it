---
title: Codice di notifica TVN_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- Controlli di Windows per il codice di notifica TVN_BEGINDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873882"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="4d182-105">\_Codice di notifica BEGINDRAG di TVN</span><span class="sxs-lookup"><span data-stu-id="4d182-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="4d182-106">Notifica alla finestra padre di un controllo di visualizzazione albero che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="4d182-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="4d182-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4d182-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="4d182-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d182-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d182-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d182-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="4d182-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="4d182-111">Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento trascinato nei membri **Hite**, **state** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="4d182-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="4d182-112">Il membro **ptDrag** specifica le coordinate dello schermo correnti del mouse.</span><span class="sxs-lookup"><span data-stu-id="4d182-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d182-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d182-113">Return value</span></span>

<span data-ttu-id="4d182-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4d182-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d182-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d182-115">Remarks</span></span>

<span data-ttu-id="4d182-116">Un controllo di visualizzazione albero con lo stile [**\_ DISABLEDRAGDROP TV**](tree-view-control-window-styles.md) non invia questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d182-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d182-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d182-117">Requirements</span></span>



| <span data-ttu-id="4d182-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d182-118">Requirement</span></span> | <span data-ttu-id="4d182-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4d182-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d182-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d182-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d182-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d182-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d182-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d182-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d182-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d182-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d182-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d182-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d182-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d182-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4d182-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4d182-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d182-127">**TVN \_ BEGINDRAGW** (Unicode) e **TVN \_ BEGINDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4d182-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





