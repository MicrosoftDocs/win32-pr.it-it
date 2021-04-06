---
title: Codice di notifica DTN_CLOSEUP (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente chiude il calendario mensile a discesa.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- Controlli di Windows per il codice di notifica DTN_CLOSEUP
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742831"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="95138-104">\_Codice di notifica closeup DTN</span><span class="sxs-lookup"><span data-stu-id="95138-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="95138-105">Inviato da un controllo di selezione data e ora (DTP) quando l'utente chiude il calendario mensile a discesa.</span><span class="sxs-lookup"><span data-stu-id="95138-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="95138-106">Il calendario mensile viene chiuso quando l'utente sceglie una data del calendario mensile o fa clic sulla freccia a discesa mentre il calendario è aperto.</span><span class="sxs-lookup"><span data-stu-id="95138-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="95138-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="95138-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="95138-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="95138-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95138-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95138-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95138-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sulla notifica.</span><span class="sxs-lookup"><span data-stu-id="95138-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95138-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95138-111">Return value</span></span>

<span data-ttu-id="95138-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="95138-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="95138-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="95138-113">Remarks</span></span>

<span data-ttu-id="95138-114">I controlli DTP non gestiscono un controllo calendario mensile figlio statico.</span><span class="sxs-lookup"><span data-stu-id="95138-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="95138-115">Il controllo DTP Elimina il controllo di calendario mensile figlio prima di inviare il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="95138-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="95138-116">Quindi, l'applicazione non deve basarsi su un handle di finestra statico per il calendario mensile figlio del controllo.</span><span class="sxs-lookup"><span data-stu-id="95138-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="95138-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95138-117">Requirements</span></span>



| <span data-ttu-id="95138-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="95138-118">Requirement</span></span> | <span data-ttu-id="95138-119">Valore</span><span class="sxs-lookup"><span data-stu-id="95138-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95138-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95138-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95138-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95138-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95138-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95138-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95138-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95138-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95138-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95138-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95138-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95138-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95138-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95138-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="95138-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="95138-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95138-128">\_elenco a discesa DTN</span><span class="sxs-lookup"><span data-stu-id="95138-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="95138-129">**\_GETMONTHCAL DTM**</span><span class="sxs-lookup"><span data-stu-id="95138-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





