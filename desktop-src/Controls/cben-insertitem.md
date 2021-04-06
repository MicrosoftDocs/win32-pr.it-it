---
title: Codice di notifica CBEN_INSERTITEM (COMmctrl. h)
description: Inviato quando un nuovo elemento è stato inserito nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- Controlli di Windows per il codice di notifica CBEN_INSERTITEM
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743818"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="82341-105">Codice di notifica di CBEN \_ INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="82341-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="82341-106">Inviato quando un nuovo elemento è stato inserito nel controllo.</span><span class="sxs-lookup"><span data-stu-id="82341-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="82341-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="82341-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="82341-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="82341-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82341-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82341-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82341-110">Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica e sull'elemento inserito.</span><span class="sxs-lookup"><span data-stu-id="82341-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82341-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82341-111">Return value</span></span>

<span data-ttu-id="82341-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="82341-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="82341-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82341-113">Requirements</span></span>



| <span data-ttu-id="82341-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82341-114">Requirement</span></span> | <span data-ttu-id="82341-115">Valore</span><span class="sxs-lookup"><span data-stu-id="82341-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82341-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82341-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82341-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82341-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82341-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82341-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82341-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82341-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82341-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82341-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="82341-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82341-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





