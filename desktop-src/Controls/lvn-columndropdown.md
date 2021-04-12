---
title: Codice di notifica LVN_COLUMNDROPDOWN (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando viene premuto il pulsante a discesa della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNDROPDOWN
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517788"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="c7e90-105">\_Codice di notifica COLUMNDROPDOWN di LVN</span><span class="sxs-lookup"><span data-stu-id="c7e90-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="c7e90-106">Inviato da un controllo di visualizzazione elenco quando viene premuto il pulsante a discesa della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="c7e90-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="c7e90-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e90-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c7e90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7e90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e90-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7e90-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e90-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che descrive il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7e90-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="c7e90-111">Il chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.</span><span class="sxs-lookup"><span data-stu-id="c7e90-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="c7e90-112">Impostare i membri della struttura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="c7e90-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="c7e90-113">Il membro del **codice** deve essere impostato su LVN \_ COLUMNDROPDOWN.</span><span class="sxs-lookup"><span data-stu-id="c7e90-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="c7e90-114">Impostare il membro **iItem** della struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) su-1.</span><span class="sxs-lookup"><span data-stu-id="c7e90-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="c7e90-115">Impostare il membro **iSubItem** sull'indice dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="c7e90-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="c7e90-116">Impostare i membri **uNewState**, **uOldState** e **lParam** su zero.</span><span class="sxs-lookup"><span data-stu-id="c7e90-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="c7e90-117">Gli altri membri della struttura **NMLISTVIEW** non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="c7e90-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e90-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7e90-118">Return value</span></span>

<span data-ttu-id="c7e90-119">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c7e90-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e90-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7e90-120">Remarks</span></span>

<span data-ttu-id="c7e90-121">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="c7e90-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="c7e90-122">Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7e90-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="c7e90-123">Se un controllo intestazione è figlio della visualizzazione elenco, il controllo intestazione deve inviare questo codice notifiche al controllo elenco-visualizzazione quando il controllo intestazione riceve il codice di notifica a [ \_ discesa HDN](hdn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e90-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e90-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7e90-124">Requirements</span></span>



| <span data-ttu-id="c7e90-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e90-125">Requirement</span></span> | <span data-ttu-id="c7e90-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c7e90-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e90-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7e90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e90-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7e90-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7e90-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7e90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e90-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7e90-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7e90-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7e90-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e90-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e90-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





