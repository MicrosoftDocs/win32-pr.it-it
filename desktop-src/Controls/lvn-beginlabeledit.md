---
title: Codice di notifica LVN_BEGINLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco l'inizio della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963802"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="fb237-105">\_Codice di notifica BEGINLABELEDIT di LVN</span><span class="sxs-lookup"><span data-stu-id="fb237-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="fb237-106">Notifica alla finestra padre di un controllo di visualizzazione elenco l'inizio della modifica dell'etichetta per un elemento.</span><span class="sxs-lookup"><span data-stu-id="fb237-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="fb237-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fb237-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fb237-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb237-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb237-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb237-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb237-110">Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fb237-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="fb237-111">Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui membro **iItem** identifica l'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="fb237-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="fb237-112">Si noti che gli elementi secondari non possono essere modificati; il membro **iSubItem** è sempre impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="fb237-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb237-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb237-113">Return value</span></span>

<span data-ttu-id="fb237-114">Per consentire all'utente di modificare l'etichetta, restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="fb237-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="fb237-115">Per impedire all'utente di modificare l'etichetta, restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="fb237-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb237-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb237-116">Remarks</span></span>

<span data-ttu-id="fb237-117">Quando viene avviata la modifica dell'etichetta, viene creato, posizionato e inizializzato un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fb237-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="fb237-118">Prima che venga visualizzato, il controllo elenco-visualizzazione Invia la finestra padre di un \_ codice di notifica BEGINLABELEDIT LVN.</span><span class="sxs-lookup"><span data-stu-id="fb237-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="fb237-119">Per personalizzare la modifica delle etichette, implementare un gestore per LVN \_ BEGINLABELEDIT e inviare un messaggio [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al controllo List-View.</span><span class="sxs-lookup"><span data-stu-id="fb237-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="fb237-120">Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fb237-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="fb237-121">Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="fb237-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="fb237-122">Quando l'utente annulla o completa la modifica, la finestra padre riceve un codice di [notifica \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="fb237-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb237-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb237-123">Requirements</span></span>



| <span data-ttu-id="fb237-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb237-124">Requirement</span></span> | <span data-ttu-id="fb237-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fb237-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb237-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb237-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb237-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb237-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb237-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb237-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb237-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb237-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb237-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb237-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb237-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb237-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fb237-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="fb237-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fb237-133">**LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fb237-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





