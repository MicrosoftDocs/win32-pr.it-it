---
title: Codice di notifica LVN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è in corso la modifica di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965012"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="1b8ec-105">\_Codice di notifica ITEMCHANGING di LVN</span><span class="sxs-lookup"><span data-stu-id="1b8ec-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="1b8ec-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è in corso la modifica di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="1b8ec-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8ec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1b8ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b8ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b8ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b8ec-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che identifica l'elemento e specifica quali attributi sono in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8ec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b8ec-111">Return value</span></span>

<span data-ttu-id="1b8ec-112">Restituisce **true** per impedire la modifica o **false** per consentire la modifica.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8ec-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b8ec-113">Remarks</span></span>

<span data-ttu-id="1b8ec-114">Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) , i \_ codici di notifica LVN ITEMCHANGING non vengono inviati.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8ec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b8ec-115">Requirements</span></span>



| <span data-ttu-id="1b8ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b8ec-116">Requirement</span></span> | <span data-ttu-id="1b8ec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1b8ec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8ec-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b8ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8ec-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b8ec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b8ec-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b8ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8ec-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b8ec-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b8ec-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b8ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b8ec-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8ec-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





