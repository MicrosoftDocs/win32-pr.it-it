---
title: Codice di notifica LVN_HOTTRACK (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente sposta il puntatore del mouse su un elemento. Questo codice di notifica viene inviato solo da controlli visualizzazione elenco con \_ \_ stile di visualizzazione elenco esteso LVS ex TRACKSELECT. Viene inviato sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Controlli di Windows per il codice di notifica LVN_HOTTRACK
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874702"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="fb906-106">\_Codice di notifica HOTTRACK di LVN</span><span class="sxs-lookup"><span data-stu-id="fb906-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="fb906-107">Inviato da un controllo di visualizzazione elenco quando l'utente sposta il puntatore del mouse su un elemento.</span><span class="sxs-lookup"><span data-stu-id="fb906-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="fb906-108">Questo codice di notifica viene inviato solo da controlli visualizzazione elenco con stile di visualizzazione elenco esteso [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fb906-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="fb906-109">Viene inviato sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fb906-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fb906-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb906-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb906-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb906-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb906-112">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="fb906-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="fb906-113">I membri **iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="fb906-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="fb906-114">L'applicazione ricevente può modificare il membro **iItem** per specificare l'elemento che verrà selezionato.</span><span class="sxs-lookup"><span data-stu-id="fb906-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="fb906-115">Se **iItem** è impostato su-1, non verrà selezionato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="fb906-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb906-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb906-116">Return value</span></span>

<span data-ttu-id="fb906-117">Restituisce zero per consentire alla visualizzazione elenco di eseguire la normale elaborazione SELECT di selezione.</span><span class="sxs-lookup"><span data-stu-id="fb906-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="fb906-118">Se l'applicazione restituisce un valore diverso da zero, l'elemento non verrà selezionato.</span><span class="sxs-lookup"><span data-stu-id="fb906-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb906-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb906-119">Requirements</span></span>



| <span data-ttu-id="fb906-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb906-120">Requirement</span></span> | <span data-ttu-id="fb906-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fb906-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb906-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb906-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fb906-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb906-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb906-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb906-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fb906-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb906-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb906-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb906-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb906-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb906-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





