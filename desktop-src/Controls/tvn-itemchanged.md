---
title: Codice di notifica TVN_ITEMCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873881"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="0d9d7-105">\_Codice di notifica ITEMCHANGED di TVN</span><span class="sxs-lookup"><span data-stu-id="0d9d7-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="0d9d7-106">Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="0d9d7-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="0d9d7-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9d7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0d9d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d9d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d9d7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d9d7-110">Puntatore a una struttura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="0d9d7-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="0d9d7-111">Il membro **uChanged** è impostato \_ sullo stato TVIF.</span><span class="sxs-lookup"><span data-stu-id="0d9d7-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9d7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d9d7-112">Return value</span></span>

<span data-ttu-id="0d9d7-113">Restituisce **false** per accettare la modifica o **true** per impedire la modifica.</span><span class="sxs-lookup"><span data-stu-id="0d9d7-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9d7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d9d7-114">Requirements</span></span>



| <span data-ttu-id="0d9d7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d9d7-115">Requirement</span></span> | <span data-ttu-id="0d9d7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0d9d7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9d7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d9d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9d7-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d9d7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d9d7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d9d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9d7-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d9d7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d9d7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d9d7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9d7-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d7-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0d9d7-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0d9d7-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0d9d7-124">**TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0d9d7-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0d9d7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d9d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9d7-126">\_ITEMCHANGING TVN</span><span class="sxs-lookup"><span data-stu-id="0d9d7-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





