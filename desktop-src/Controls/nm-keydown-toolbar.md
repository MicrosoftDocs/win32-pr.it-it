---
title: NM_KEYDOWN di notifica (barra degli strumenti) (Commctrl.h)
description: "NM_KEYDOWN di notifica (barra degli strumenti): inviato da un controllo quando il controllo ha lo stato attivo e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio WM \\_ NOTIFY."
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN controlli Windows del codice di notifica (barra degli strumenti)
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112359"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="3fc1e-105">Codice di \_ notifica NM KEYDOWN (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="3fc1e-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="3fc1e-106">Inviato da un controllo quando il controllo ha lo stato attivo e l'utente preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="3fc1e-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="3fc1e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="3fc1e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3fc1e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fc1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fc1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc1e-110">Puntatore a una [**struttura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="3fc1e-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fc1e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fc1e-111">Return value</span></span>

<span data-ttu-id="3fc1e-112">Restituisce un valore diverso da zero per impedire al controllo di elaborare il tasto oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3fc1e-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc1e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fc1e-113">Remarks</span></span>

<span data-ttu-id="3fc1e-114">Attualmente, solo il controllo barra degli strumenti invia questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="3fc1e-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc1e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fc1e-115">Requirements</span></span>



| <span data-ttu-id="3fc1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc1e-116">Requirement</span></span> | <span data-ttu-id="3fc1e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3fc1e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc1e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc1e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc1e-119">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3fc1e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fc1e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc1e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc1e-121">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fc1e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fc1e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fc1e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc1e-123"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc1e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





