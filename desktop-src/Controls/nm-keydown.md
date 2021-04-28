---
title: NM_KEYDOWN codice di notifica (Commctrl.h)
description: "NM_KEYDOWN codice di notifica: inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio WM \\_ NOTIFY."
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN codice di notifica controlli Windows
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
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112349"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="84ad5-105">Codice \_ di notifica NM KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="84ad5-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="84ad5-106">Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="84ad5-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="84ad5-107">Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="84ad5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="84ad5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="84ad5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84ad5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84ad5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84ad5-110">Puntatore a una [**struttura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) che contiene informazioni aggiuntive sulla chiave che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="84ad5-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84ad5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84ad5-111">Return value</span></span>

<span data-ttu-id="84ad5-112">Restituisce un valore diverso da zero per impedire al controllo di elaborare la chiave oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="84ad5-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ad5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84ad5-113">Requirements</span></span>



| <span data-ttu-id="84ad5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84ad5-114">Requirement</span></span> | <span data-ttu-id="84ad5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="84ad5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84ad5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84ad5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84ad5-117">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="84ad5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84ad5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84ad5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84ad5-119">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="84ad5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84ad5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84ad5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ad5-121"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="84ad5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





