---
title: Codice di notifica TVN_BEGINRDRAG (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero l'avvio di un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- Controlli di Windows per il codice di notifica TVN_BEGINRDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964844"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="62c2d-105">\_Codice di notifica BEGINRDRAG di TVN</span><span class="sxs-lookup"><span data-stu-id="62c2d-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="62c2d-106">Notifica alla finestra padre di un controllo di visualizzazione albero l'avvio di un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="62c2d-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="62c2d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="62c2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="62c2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62c2d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62c2d-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="62c2d-111">Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide nei membri **Hite**, **state** e **lParam** sull'elemento da trascinare.</span><span class="sxs-lookup"><span data-stu-id="62c2d-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="62c2d-112">Il membro **ptDrag** specifica le coordinate dello schermo correnti del mouse.</span><span class="sxs-lookup"><span data-stu-id="62c2d-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c2d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62c2d-113">Return value</span></span>

<span data-ttu-id="62c2d-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="62c2d-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c2d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c2d-115">Requirements</span></span>



| <span data-ttu-id="62c2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c2d-116">Requirement</span></span> | <span data-ttu-id="62c2d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="62c2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c2d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62c2d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62c2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62c2d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62c2d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62c2d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62c2d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c2d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c2d-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="62c2d-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="62c2d-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="62c2d-125">**TVN \_ BEGINRDRAGW** (Unicode) e **TVN \_ BEGINRDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="62c2d-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





