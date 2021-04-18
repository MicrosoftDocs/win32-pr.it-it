---
title: Codice di notifica LVN_ITEMCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302799"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="10040-105">\_Codice di notifica ITEMCHANGED di LVN</span><span class="sxs-lookup"><span data-stu-id="10040-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="10040-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che un elemento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="10040-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="10040-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10040-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="10040-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10040-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10040-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10040-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quali attributi sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="10040-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="10040-111">Se il membro **iItem** della struttura a cui punta *lParam* è-1, la modifica è stata applicata a tutti gli elementi nella visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="10040-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10040-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10040-112">Return value</span></span>

<span data-ttu-id="10040-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="10040-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10040-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="10040-114">Remarks</span></span>

<span data-ttu-id="10040-115">Se un controllo di visualizzazione elenco ha lo [**stile \_ OWNERDATA LVS**](list-view-window-styles.md) e l'utente seleziona un intervallo di elementi tenendo premuto il tasto MAIUSC e facendo clic sul mouse, i \_ codici di notifica LVN ITEMCHANGED non vengono inviati per ogni elemento selezionato o deselezionato.</span><span class="sxs-lookup"><span data-stu-id="10040-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="10040-116">Si riceverà invece un solo codice di notifica [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) , che indica che un intervallo di elementi è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="10040-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="10040-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10040-117">Requirements</span></span>



| <span data-ttu-id="10040-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10040-118">Requirement</span></span> | <span data-ttu-id="10040-119">Valore</span><span class="sxs-lookup"><span data-stu-id="10040-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10040-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10040-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10040-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10040-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10040-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10040-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10040-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10040-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10040-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10040-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10040-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10040-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





