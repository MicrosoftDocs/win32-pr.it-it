---
title: Codice di notifica TVN_BEGINLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- Controlli di Windows per il codice di notifica TVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301702"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="f95ce-105">\_Codice di notifica BEGINLABELEDIT di TVN</span><span class="sxs-lookup"><span data-stu-id="f95ce-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="f95ce-106">Notifica alla finestra padre di un controllo di visualizzazione albero l'inizio della modifica dell'etichetta per un elemento.</span><span class="sxs-lookup"><span data-stu-id="f95ce-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="f95ce-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f95ce-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="f95ce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f95ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f95ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f95ce-110">Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f95ce-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="f95ce-111">Il membro dell' **elemento** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento da modificare nei membri **Hite**, **state**, **lParam** e **pszText** .</span><span class="sxs-lookup"><span data-stu-id="f95ce-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95ce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f95ce-112">Return value</span></span>

<span data-ttu-id="f95ce-113">Restituisce **true** per annullare la modifica dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="f95ce-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="f95ce-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f95ce-114">Remarks</span></span>

<span data-ttu-id="f95ce-115">Quando viene avviata la modifica dell'etichetta, viene creato un controllo di modifica, ma non è posizionato o visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f95ce-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="f95ce-116">Prima che venga visualizzato, il controllo di visualizzazione albero Invia la finestra padre a un \_ codice di notifica di TVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="f95ce-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="f95ce-117">Per personalizzare la modifica delle etichette, implementare un gestore per TVN \_ BEGINLABELEDIT e fare in modo che invii un messaggio [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) al controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="f95ce-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="f95ce-118">Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="f95ce-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="f95ce-119">Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali \_ messaggi em xxx.</span><span class="sxs-lookup"><span data-stu-id="f95ce-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="f95ce-120">Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di [notifica \_ ENDLABELEDIT di TVN](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="f95ce-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95ce-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f95ce-121">Requirements</span></span>



| <span data-ttu-id="f95ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f95ce-122">Requirement</span></span> | <span data-ttu-id="f95ce-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f95ce-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f95ce-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f95ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f95ce-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f95ce-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f95ce-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f95ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f95ce-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f95ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f95ce-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f95ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f95ce-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f95ce-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f95ce-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f95ce-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f95ce-131">**TVN \_ BEGINLABELEDITW** (Unicode) e **TVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f95ce-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





