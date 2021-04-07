---
title: Codice di notifica DTN_DATETIMECHANGE (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) ogni volta che viene apportata una modifica. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Controlli di Windows per il codice di notifica DTN_DATETIMECHANGE
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874166"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="d3b96-105">\_Codice di notifica DATETIMECHANGE di DTN</span><span class="sxs-lookup"><span data-stu-id="d3b96-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="d3b96-106">Inviato da un controllo di selezione data e ora (DTP) ogni volta che viene apportata una modifica.</span><span class="sxs-lookup"><span data-stu-id="d3b96-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="d3b96-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b96-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d3b96-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3b96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b96-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3b96-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b96-110">Puntatore a una struttura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) contenente informazioni sulla modifica che ha avuto luogo nel controllo.</span><span class="sxs-lookup"><span data-stu-id="d3b96-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b96-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3b96-111">Return value</span></span>

<span data-ttu-id="d3b96-112">Il proprietario del controllo deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="d3b96-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b96-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3b96-113">Requirements</span></span>



| <span data-ttu-id="d3b96-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b96-114">Requirement</span></span> | <span data-ttu-id="d3b96-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b96-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b96-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b96-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b96-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3b96-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3b96-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b96-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b96-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3b96-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3b96-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3b96-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b96-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b96-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





