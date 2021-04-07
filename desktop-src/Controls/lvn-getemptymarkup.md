---
title: Codice di notifica LVN_GETEMPTYMARKUP (COMmctrl. h)
description: Inviato dal controllo visualizzazione elenco alla relativa finestra padre quando il controllo non dispone di elementi. Il \_ codice di notifica GETEMPTYMARKUP di LVN è una richiesta che la finestra padre fornisca il testo di markup. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Controlli di Windows per il codice di notifica LVN_GETEMPTYMARKUP
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874705"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="b8b08-106">\_Codice di notifica GETEMPTYMARKUP di LVN</span><span class="sxs-lookup"><span data-stu-id="b8b08-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="b8b08-107">Inviato dal controllo visualizzazione elenco alla relativa finestra padre quando il controllo non dispone di elementi.</span><span class="sxs-lookup"><span data-stu-id="b8b08-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="b8b08-108">Il \_ codice di notifica GETEMPTYMARKUP di LVN è una richiesta che la finestra padre fornisca il testo di markup.</span><span class="sxs-lookup"><span data-stu-id="b8b08-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="b8b08-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b08-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b8b08-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8b08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b08-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8b08-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b08-112">Puntatore a una struttura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="b8b08-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="b8b08-113">Impostare i membri di questa struttura per fornire il testo di markup per il controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="b8b08-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b08-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8b08-114">Return value</span></span>

<span data-ttu-id="b8b08-115">Restituisce **true** per impostare il testo del markup nel controllo visualizzazione elenco oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b8b08-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b08-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8b08-116">Remarks</span></span>

<span data-ttu-id="b8b08-117">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="b8b08-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="b8b08-118">Il parametro *wParam* contiene l'ID del controllo che invia questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="b8b08-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b08-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8b08-119">Requirements</span></span>



| <span data-ttu-id="b8b08-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b08-120">Requirement</span></span> | <span data-ttu-id="b8b08-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8b08-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b08-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8b08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b08-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8b08-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8b08-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8b08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b08-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8b08-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8b08-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8b08-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b08-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b08-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





