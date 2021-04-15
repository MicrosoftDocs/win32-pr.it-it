---
title: Codice di notifica LVN_COLUMNOVERFLOWCLICK (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNOVERFLOWCLICK
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479448"
---
# <a name="lvn_columnoverflowclick-notification-code"></a><span data-ttu-id="62c17-105">\_Codice di notifica COLUMNOVERFLOWCLICK di LVN</span><span class="sxs-lookup"><span data-stu-id="62c17-105">LVN\_COLUMNOVERFLOWCLICK notification code</span></span>

<span data-ttu-id="62c17-106">Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow.</span><span class="sxs-lookup"><span data-stu-id="62c17-106">Sent by a list-view control when its overflow button is clicked.</span></span> <span data-ttu-id="62c17-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62c17-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="62c17-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="62c17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c17-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c17-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c17-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che descrive il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="62c17-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="62c17-111">Il chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.</span><span class="sxs-lookup"><span data-stu-id="62c17-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="62c17-112">Impostare i membri della struttura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="62c17-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="62c17-113">Il membro del **codice** deve essere impostato su LVN \_ COLUMNOVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="62c17-113">The **code** member must be set to LVN\_COLUMNOVERFLOWCLICK.</span></span>

<span data-ttu-id="62c17-114">Impostare il membro **iItem** della struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) su-1.</span><span class="sxs-lookup"><span data-stu-id="62c17-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="62c17-115">Impostare il membro **iSubItem** sull'indice dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="62c17-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="62c17-116">Impostare i membri **uNewState**, **uOldState** e **lParam** su zero.</span><span class="sxs-lookup"><span data-stu-id="62c17-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="62c17-117">Gli altri membri della struttura **NMLISTVIEW** non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="62c17-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c17-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62c17-118">Return value</span></span>

<span data-ttu-id="62c17-119">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="62c17-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c17-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="62c17-120">Remarks</span></span>

<span data-ttu-id="62c17-121">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="62c17-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="62c17-122">Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="62c17-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="62c17-123">Se un controllo intestazione è figlio di ListView, il controllo intestazione deve inviare questo codice di notifica al controllo ListView quando il controllo intestazione riceve il codice di [notifica \_ OVERFLOWCLICK HDN](hdn-overflowclick.md) .</span><span class="sxs-lookup"><span data-stu-id="62c17-123">If a header control is a child of the listview, the header control should send this notification code to the listview control when the header control receives the [HDN\_OVERFLOWCLICK](hdn-overflowclick.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c17-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c17-124">Requirements</span></span>



| <span data-ttu-id="62c17-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c17-125">Requirement</span></span> | <span data-ttu-id="62c17-126">Valore</span><span class="sxs-lookup"><span data-stu-id="62c17-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c17-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c17-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62c17-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62c17-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62c17-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c17-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62c17-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62c17-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62c17-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c17-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c17-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c17-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





