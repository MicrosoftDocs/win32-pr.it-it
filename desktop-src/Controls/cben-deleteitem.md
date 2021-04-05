---
title: Codice di notifica CBEN_DELETEITEM (COMmctrl. h)
description: Inviato quando un elemento è stato eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- Controlli di Windows per il codice di notifica CBEN_DELETEITEM
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874425"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="d1a7b-105">\_Codice di notifica DeleteItem di CBEN</span><span class="sxs-lookup"><span data-stu-id="d1a7b-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="d1a7b-106">Inviato quando un elemento è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="d1a7b-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="d1a7b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d1a7b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1a7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1a7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a7b-110">Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica e sull'elemento eliminato.</span><span class="sxs-lookup"><span data-stu-id="d1a7b-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a7b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1a7b-111">Return value</span></span>

<span data-ttu-id="d1a7b-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="d1a7b-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a7b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1a7b-113">Requirements</span></span>



| <span data-ttu-id="d1a7b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a7b-114">Requirement</span></span> | <span data-ttu-id="d1a7b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d1a7b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a7b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1a7b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a7b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1a7b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1a7b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1a7b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a7b-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1a7b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1a7b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1a7b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a7b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a7b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





