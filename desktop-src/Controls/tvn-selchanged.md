---
title: Codice di notifica TVN_SELCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione è cambiata da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- Controlli di Windows per il codice di notifica TVN_SELCHANGED
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874474"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="8b972-105">\_Codice di notifica SELCHANGED di TVN</span><span class="sxs-lookup"><span data-stu-id="8b972-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="8b972-106">Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione è cambiata da un elemento a un altro.</span><span class="sxs-lookup"><span data-stu-id="8b972-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="8b972-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8b972-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="8b972-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b972-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b972-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b972-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b972-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="8b972-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="8b972-111">I membri **itemOld** e **ItemNew** della struttura **NMTREEVIEW** sono strutture [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) contenenti informazioni sull'elemento selezionato in precedenza e sull'elemento appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="8b972-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="8b972-112">Sono validi solo i membri **mask**, **hitet**, **state** e **lParam** di queste strutture.</span><span class="sxs-lookup"><span data-stu-id="8b972-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="8b972-113">I membri **stateMask** delle strutture **TVITEM** specificate da **itemOld** e **itemNew** non sono definiti nell'input.</span><span class="sxs-lookup"><span data-stu-id="8b972-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="8b972-114">Il membro **Action** della struttura **NMTREEVIEW** indica il tipo di azione che ha causato la modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="8b972-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="8b972-115">Può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b972-115">It can be one of the following values:</span></span>



| <span data-ttu-id="8b972-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b972-116">Requirement</span></span> | <span data-ttu-id="8b972-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8b972-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="8b972-118">\_BYKEYBOARD TVC</span><span class="sxs-lookup"><span data-stu-id="8b972-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="8b972-119">Da una sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="8b972-119">By a keystroke.</span></span>   |
| <span data-ttu-id="8b972-120">\_BYMOUSE TVC</span><span class="sxs-lookup"><span data-stu-id="8b972-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="8b972-121">Con un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="8b972-121">By a mouse click.</span></span> |
| <span data-ttu-id="8b972-122">TVC \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="8b972-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="8b972-123">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8b972-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b972-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b972-124">Return value</span></span>

<span data-ttu-id="8b972-125">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8b972-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b972-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b972-126">Requirements</span></span>



| <span data-ttu-id="8b972-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b972-127">Requirement</span></span> | <span data-ttu-id="8b972-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8b972-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b972-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b972-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8b972-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b972-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b972-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b972-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8b972-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b972-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b972-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b972-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b972-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b972-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8b972-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8b972-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8b972-136">**TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8b972-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





