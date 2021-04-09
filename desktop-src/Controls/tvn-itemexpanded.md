---
title: Codice di notifica TVN_ITEMEXPANDED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco di elementi figlio di un elemento padre è espanso o compresso. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMEXPANDED
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121282"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="674eb-105">\_Codice di notifica ITEMEXPANDED di TVN</span><span class="sxs-lookup"><span data-stu-id="674eb-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="674eb-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco di elementi figlio di un elemento padre è espanso o compresso.</span><span class="sxs-lookup"><span data-stu-id="674eb-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="674eb-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="674eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="674eb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="674eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="674eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="674eb-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="674eb-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="674eb-111">Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **Hite**, **state** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="674eb-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="674eb-112">Il membro dell' **azione** indica se l'elenco è espanso o compresso.</span><span class="sxs-lookup"><span data-stu-id="674eb-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="674eb-113">Per un elenco di valori possibili, vedere la descrizione del messaggio [**di \_ espansione TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="674eb-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674eb-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="674eb-114">Return value</span></span>

<span data-ttu-id="674eb-115">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="674eb-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="674eb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="674eb-116">Requirements</span></span>



| <span data-ttu-id="674eb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="674eb-117">Requirement</span></span> | <span data-ttu-id="674eb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="674eb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="674eb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="674eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="674eb-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="674eb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="674eb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="674eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="674eb-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="674eb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="674eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="674eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="674eb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="674eb-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="674eb-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="674eb-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="674eb-126">**TVN \_ ITEMEXPANDEDW** (Unicode) e **TVN \_ ITEMEXPANDEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="674eb-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="674eb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="674eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674eb-128">\_ITEMEXPANDING TVN</span><span class="sxs-lookup"><span data-stu-id="674eb-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





