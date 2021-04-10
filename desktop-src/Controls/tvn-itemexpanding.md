---
title: Codice di notifica TVN_ITEMEXPANDING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco degli elementi figlio di un elemento padre sta per espandersi o comprimere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMEXPANDING
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964843"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="a9d32-105">\_Codice di notifica ITEMEXPANDING di TVN</span><span class="sxs-lookup"><span data-stu-id="a9d32-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="a9d32-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco degli elementi figlio di un elemento padre sta per espandersi o comprimere.</span><span class="sxs-lookup"><span data-stu-id="a9d32-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="a9d32-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d32-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a9d32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9d32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9d32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d32-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="a9d32-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="a9d32-111">Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **Hite**, **state** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="a9d32-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="a9d32-112">Il membro dell' **azione** indica se l'elenco deve essere espanso o compresso.</span><span class="sxs-lookup"><span data-stu-id="a9d32-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="a9d32-113">Per un elenco di valori possibili, vedere la descrizione del messaggio [**di \_ espansione TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d32-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d32-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9d32-114">Return value</span></span>

<span data-ttu-id="a9d32-115">Restituisce **true** per impedire l'espansione o la compressione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a9d32-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d32-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9d32-116">Requirements</span></span>



| <span data-ttu-id="a9d32-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d32-117">Requirement</span></span> | <span data-ttu-id="a9d32-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a9d32-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d32-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d32-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9d32-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9d32-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d32-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9d32-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9d32-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9d32-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d32-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d32-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a9d32-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a9d32-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9d32-126">**TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_ ITEMEXPANDINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a9d32-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a9d32-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9d32-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d32-128">\_ITEMEXPANDED TVN</span><span class="sxs-lookup"><span data-stu-id="a9d32-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





