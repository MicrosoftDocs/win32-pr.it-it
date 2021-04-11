---
title: Codice di notifica LVN_SETDISPINFO (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che deve aggiornare le informazioni gestite per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Controlli di Windows per il codice di notifica LVN_SETDISPINFO
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964572"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="bf3d4-105">\_Codice di notifica SETDISPINFO di LVN</span><span class="sxs-lookup"><span data-stu-id="bf3d4-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="bf3d4-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che deve aggiornare le informazioni gestite per un elemento.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="bf3d4-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf3d4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="bf3d4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf3d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf3d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf3d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf3d4-110">Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) che specifica le informazioni per l'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="bf3d4-111">Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene informazioni sull'elemento che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="bf3d4-112">Il membro **pszText** dell' **elemento** contiene un valore valido, indipendentemente dal fatto che il \_ flag di testo LVIF sia impostato nel membro **mask** della struttura.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf3d4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf3d4-113">Return value</span></span>

<span data-ttu-id="bf3d4-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf3d4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf3d4-115">Remarks</span></span>

<span data-ttu-id="bf3d4-116">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bf3d4-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="bf3d4-117">Il parametro *wParam* contiene il codice del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bf3d4-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf3d4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf3d4-118">Requirements</span></span>



| <span data-ttu-id="bf3d4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf3d4-119">Requirement</span></span> | <span data-ttu-id="bf3d4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bf3d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3d4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf3d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bf3d4-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf3d4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf3d4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf3d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bf3d4-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf3d4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf3d4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf3d4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf3d4-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf3d4-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bf3d4-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bf3d4-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf3d4-128">**LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf3d4-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bf3d4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf3d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3d4-130">\_GETDISPINFO LVN</span><span class="sxs-lookup"><span data-stu-id="bf3d4-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





