---
title: Codice di notifica TBN_HOTITEMCHANGE (COMmctrl. h)
description: Inviato da un controllo Toolbar quando viene modificato l'elemento attivo (evidenziato). Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- Controlli di Windows per il codice di notifica TBN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739890"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="faff8-105">\_Codice di notifica HOTITEMCHANGE di TBN</span><span class="sxs-lookup"><span data-stu-id="faff8-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="faff8-106">Inviato da un controllo Toolbar quando viene modificato l'elemento attivo (evidenziato).</span><span class="sxs-lookup"><span data-stu-id="faff8-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="faff8-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="faff8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="faff8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="faff8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faff8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faff8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faff8-110">Puntatore a una struttura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="faff8-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faff8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="faff8-111">Return value</span></span>

<span data-ttu-id="faff8-112">Restituisce zero per consentire l'evidenziazione dell'elemento o un valore diverso da zero per impedire che l'elemento venga evidenziato.</span><span class="sxs-lookup"><span data-stu-id="faff8-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="faff8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faff8-113">Requirements</span></span>



| <span data-ttu-id="faff8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="faff8-114">Requirement</span></span> | <span data-ttu-id="faff8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="faff8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="faff8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="faff8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="faff8-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="faff8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="faff8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="faff8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="faff8-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="faff8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="faff8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="faff8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="faff8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="faff8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





