---
title: Codice di notifica NM_KILLFOCUS (data/ora) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha perso lo stato attivo per l'input. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (data/ora) del codice di notifica controlli Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963756"
---
# <a name="nm_killfocus-date-time-notification-code"></a><span data-ttu-id="e7aa6-105">\_Codice di notifica di KILLFOCUS (data/ora) Nm</span><span class="sxs-lookup"><span data-stu-id="e7aa6-105">NM\_KILLFOCUS (date time) notification code</span></span>

<span data-ttu-id="e7aa6-106">Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha perso lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="e7aa6-106">Notifies a date and time picker control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="e7aa6-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e7aa6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7aa6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7aa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aa6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7aa6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7aa6-110">Indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="e7aa6-110">The address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aa6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7aa6-111">Return value</span></span>

<span data-ttu-id="e7aa6-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e7aa6-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7aa6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7aa6-113">Requirements</span></span>



| <span data-ttu-id="e7aa6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7aa6-114">Requirement</span></span> | <span data-ttu-id="e7aa6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e7aa6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aa6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7aa6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7aa6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7aa6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7aa6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7aa6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7aa6-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7aa6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7aa6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7aa6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7aa6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7aa6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





