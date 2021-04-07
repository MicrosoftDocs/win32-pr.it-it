---
title: Codice di notifica IPN_FIELDCHANGED (COMmctrl. h)
description: Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Controlli di Windows per il codice di notifica IPN_FIELDCHANGED
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048611"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="46f6d-105">Codice di notifica di IPN \_ FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="46f6d-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="46f6d-106">Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro.</span><span class="sxs-lookup"><span data-stu-id="46f6d-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="46f6d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="46f6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="46f6d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46f6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46f6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46f6d-110">Puntatore a una struttura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) che contiene informazioni sull'indirizzo modificato.</span><span class="sxs-lookup"><span data-stu-id="46f6d-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="46f6d-111">Il membro **iValue** della struttura conterrà il valore immesso, anche se non è compreso nell'intervallo del campo.</span><span class="sxs-lookup"><span data-stu-id="46f6d-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="46f6d-112">È possibile modificare questo membro in qualsiasi valore compreso nell'intervallo per il campo in risposta a questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="46f6d-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f6d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46f6d-113">Return value</span></span>

<span data-ttu-id="46f6d-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="46f6d-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f6d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="46f6d-115">Remarks</span></span>

<span data-ttu-id="46f6d-116">Questo codice di notifica non viene inviato in risposta a un messaggio di [**\_ Indirizzo IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="46f6d-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="46f6d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46f6d-117">Requirements</span></span>



| <span data-ttu-id="46f6d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f6d-118">Requirement</span></span> | <span data-ttu-id="46f6d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="46f6d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46f6d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46f6d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46f6d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46f6d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46f6d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46f6d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46f6d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46f6d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46f6d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46f6d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f6d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f6d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





