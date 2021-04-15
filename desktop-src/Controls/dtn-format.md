---
title: Codice di notifica DTN_FORMAT (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) per richiedere il testo da visualizzare in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Controlli di Windows per il codice di notifica DTN_FORMAT
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477633"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="c11e9-105">\_Codice di notifica del formato DTN</span><span class="sxs-lookup"><span data-stu-id="c11e9-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="c11e9-106">Inviato da un controllo di selezione data e ora (DTP) per richiedere il testo da visualizzare in un campo di callback.</span><span class="sxs-lookup"><span data-stu-id="c11e9-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="c11e9-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c11e9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c11e9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c11e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c11e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c11e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c11e9-110">Puntatore a una struttura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) contenente informazioni relative a questa istanza del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c11e9-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="c11e9-111">La struttura contiene la sottostringa che definisce il campo di callback e riceve la stringa formattata che il controllo visualizzerà.</span><span class="sxs-lookup"><span data-stu-id="c11e9-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c11e9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c11e9-112">Return value</span></span>

<span data-ttu-id="c11e9-113">Il proprietario del controllo deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="c11e9-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c11e9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c11e9-114">Remarks</span></span>

<span data-ttu-id="c11e9-115">La gestione di questo codice di notifica consente al proprietario del controllo di fornire una stringa personalizzata che verrà visualizzata dal controllo.</span><span class="sxs-lookup"><span data-stu-id="c11e9-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="c11e9-116">Per ulteriori informazioni sui campi di callback, vedere [campi callback](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c11e9-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="c11e9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c11e9-117">Requirements</span></span>



| <span data-ttu-id="c11e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c11e9-118">Requirement</span></span> | <span data-ttu-id="c11e9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c11e9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c11e9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c11e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c11e9-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c11e9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c11e9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c11e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c11e9-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c11e9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c11e9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c11e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c11e9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c11e9-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c11e9-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c11e9-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c11e9-127">**DTN \_ FORMATW** (Unicode) e **DTN \_ formata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c11e9-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





