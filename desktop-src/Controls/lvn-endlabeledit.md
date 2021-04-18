---
title: Codice di notifica LVN_ENDLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Controlli di Windows per il codice di notifica LVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302803"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="b7493-105">\_Codice di notifica ENDLABELEDIT di LVN</span><span class="sxs-lookup"><span data-stu-id="b7493-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="b7493-106">Notifica alla finestra padre di un controllo di visualizzazione elenco la fine della modifica dell'etichetta per un elemento.</span><span class="sxs-lookup"><span data-stu-id="b7493-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="b7493-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b7493-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b7493-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7493-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7493-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7493-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7493-110">Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b7493-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="b7493-111">Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui membro **iItem** identifica l'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="b7493-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="b7493-112">Il membro **pszText** dell' **elemento** contiene un valore valido quando \_ viene inviato il codice di notifica ENDLABELEDIT LVN, indipendentemente dal fatto che il \_ flag di testo LVIF sia impostato nel membro **mask** della struttura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="b7493-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="b7493-113">Se l'utente annulla la modifica, il membro **pszText** della struttura **LVITEM** è **null**. in caso contrario, **pszText** è l'indirizzo del testo modificato.</span><span class="sxs-lookup"><span data-stu-id="b7493-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7493-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7493-114">Return value</span></span>

<span data-ttu-id="b7493-115">Se il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) è diverso da **null**, restituisce **true** per impostare l'etichetta dell'elemento sul testo modificato.</span><span class="sxs-lookup"><span data-stu-id="b7493-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="b7493-116">Restituisce **false** per rifiutare il testo modificato e ripristinare l'etichetta originale.</span><span class="sxs-lookup"><span data-stu-id="b7493-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="b7493-117">Se il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) è **null**, il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b7493-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7493-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7493-118">Remarks</span></span>

<span data-ttu-id="b7493-119">Il valore restituito dalla routine della finestra di dialogo indica se il messaggio è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="b7493-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="b7493-120">Il secondo valore restituito deve essere impostato chiamando [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) con **DWLP_MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7493-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="b7493-121">Quando l'utente inizia a modificare l'etichetta di un elemento, la finestra padre del controllo elenco-visualizzazione riceve un codice di notifica [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="b7493-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="b7493-122">Quando l'utente annulla o completa la modifica, la finestra padre riceve un \_ codice di notifica ENDLABELEDIT LVN.</span><span class="sxs-lookup"><span data-stu-id="b7493-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7493-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7493-123">Requirements</span></span>



| <span data-ttu-id="b7493-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7493-124">Requirement</span></span> | <span data-ttu-id="b7493-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b7493-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7493-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7493-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b7493-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7493-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7493-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7493-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b7493-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7493-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7493-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7493-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7493-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7493-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b7493-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b7493-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b7493-133">**LVN \_ ENDLABELEDITW** (Unicode) e **LVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b7493-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





