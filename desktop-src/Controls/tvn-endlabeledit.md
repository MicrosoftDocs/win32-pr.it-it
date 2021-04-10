---
title: Codice di notifica TVN_ENDLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Controlli di Windows per il codice di notifica TVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119918"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="48069-105">\_Codice di notifica ENDLABELEDIT di TVN</span><span class="sxs-lookup"><span data-stu-id="48069-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="48069-106">Notifica alla finestra padre di un controllo di visualizzazione albero la fine della modifica dell'etichetta per un elemento.</span><span class="sxs-lookup"><span data-stu-id="48069-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="48069-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="48069-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="48069-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48069-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48069-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48069-110">Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="48069-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="48069-111">Il membro dell' **elemento** di questa struttura è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **Hite**, **lParam** e **pszText** contengono informazioni valide sull'elemento che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="48069-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="48069-112">Se la modifica dell'etichetta è stata annullata, il membro **pszText** della struttura **TVITEM** è **null**. in caso contrario, **pszText** è l'indirizzo del testo modificato.</span><span class="sxs-lookup"><span data-stu-id="48069-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48069-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48069-113">Return value</span></span>

<span data-ttu-id="48069-114">Se il membro **pszText** è diverso da **null**, restituire **true** per impostare l'etichetta dell'elemento sul testo modificato.</span><span class="sxs-lookup"><span data-stu-id="48069-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="48069-115">Restituisce **false** per rifiutare il testo modificato e ripristinare l'etichetta originale.</span><span class="sxs-lookup"><span data-stu-id="48069-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="48069-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="48069-116">Remarks</span></span>

<span data-ttu-id="48069-117">Se il membro **pszText** è **null**, il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="48069-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="48069-118">Se è stato specificato il \_ valore TEXTCALLBACK di LPSTR per questo elemento e il membro **pszText** è diverso da **null**, il \_ gestore ENDLABELEDIT di TVN deve copiare il testo da **pszText** nella risorsa di archiviazione locale.</span><span class="sxs-lookup"><span data-stu-id="48069-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="48069-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48069-119">Requirements</span></span>



| <span data-ttu-id="48069-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48069-120">Requirement</span></span> | <span data-ttu-id="48069-121">Valore</span><span class="sxs-lookup"><span data-stu-id="48069-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48069-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48069-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48069-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48069-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48069-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48069-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48069-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48069-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48069-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48069-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="48069-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48069-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="48069-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="48069-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="48069-129">**TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="48069-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





