---
title: Codice di notifica TVN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento stanno per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517824"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="25470-105">\_Codice di notifica ITEMCHANGING di TVN</span><span class="sxs-lookup"><span data-stu-id="25470-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="25470-106">Notifica alla finestra padre di un controllo di visualizzazione albero che gli attributi dell'elemento stanno per cambiare.</span><span class="sxs-lookup"><span data-stu-id="25470-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="25470-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="25470-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="25470-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25470-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25470-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25470-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25470-110">Puntatore a una struttura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) che descrive l'elemento in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="25470-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="25470-111">Il membro **uChanged** è impostato \_ sullo stato TVIF.</span><span class="sxs-lookup"><span data-stu-id="25470-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25470-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25470-112">Return value</span></span>

<span data-ttu-id="25470-113">Restituisce **false** per accettare la modifica o **true** per impedire la modifica.</span><span class="sxs-lookup"><span data-stu-id="25470-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="25470-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25470-114">Requirements</span></span>



| <span data-ttu-id="25470-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25470-115">Requirement</span></span> | <span data-ttu-id="25470-116">Valore</span><span class="sxs-lookup"><span data-stu-id="25470-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25470-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25470-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25470-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25470-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25470-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25470-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25470-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25470-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25470-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25470-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="25470-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25470-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="25470-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="25470-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="25470-124">**TVN \_ ITEMCHANGINGW** (Unicode) e **TVN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="25470-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="25470-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25470-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25470-126">\_ITEMCHANGED TVN</span><span class="sxs-lookup"><span data-stu-id="25470-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





