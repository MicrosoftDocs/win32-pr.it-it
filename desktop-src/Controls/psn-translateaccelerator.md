---
title: Codice di notifica PSN_TRANSLATEACCELERATOR (Prsht. h)
description: Notifica a una finestra delle proprietà che è stato ricevuto un messaggio da tastiera. Fornisce alla pagina la possibilità di eseguire la conversione dell'acceleratore di tastiera privata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Controlli di Windows per il codice di notifica PSN_TRANSLATEACCELERATOR
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301016"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="66b01-106">\_Codice di notifica TRANSLATEACCELERATOR PSN</span><span class="sxs-lookup"><span data-stu-id="66b01-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="66b01-107">Notifica a una finestra delle proprietà che è stato ricevuto un messaggio da tastiera.</span><span class="sxs-lookup"><span data-stu-id="66b01-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="66b01-108">Fornisce alla pagina la possibilità di eseguire la conversione dell'acceleratore di tastiera privata.</span><span class="sxs-lookup"><span data-stu-id="66b01-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="66b01-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66b01-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="66b01-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="66b01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b01-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66b01-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b01-112">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="66b01-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="66b01-113">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="66b01-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="66b01-114">Il membro **lParam** della struttura **PSHNOTIFY** è un puntatore al [**msg**](/windows/win32/api/winuser/ns-winuser-msg)del messaggio.</span><span class="sxs-lookup"><span data-stu-id="66b01-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="66b01-115">È possibile eseguire il cast a un tipo **lpMsg** per ottenere l'accesso ai parametri del messaggio da tradurre.</span><span class="sxs-lookup"><span data-stu-id="66b01-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b01-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66b01-116">Return value</span></span>

<span data-ttu-id="66b01-117">Restituisce PSNRET \_ MESSAGEHANDLED per indicare che non è necessaria alcuna ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="66b01-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="66b01-118">Restituisce PSNRET \_ NOERROR per richiedere l'elaborazione normale.</span><span class="sxs-lookup"><span data-stu-id="66b01-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b01-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="66b01-119">Remarks</span></span>

<span data-ttu-id="66b01-120">Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore DWL MSGRESULT.</span><span class="sxs-lookup"><span data-stu-id="66b01-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="66b01-121">La routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="66b01-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b01-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66b01-122">Requirements</span></span>



| <span data-ttu-id="66b01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b01-123">Requirement</span></span> | <span data-ttu-id="66b01-124">Valore</span><span class="sxs-lookup"><span data-stu-id="66b01-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66b01-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66b01-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66b01-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66b01-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66b01-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66b01-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66b01-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66b01-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b01-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b01-130"><dt>Prsht.h</dt></span></span> </dl> |



 

