---
title: Codice di notifica PSN_QUERYINITIALFOCUS (Prsht. h)
description: Inviato da una finestra delle proprietà per fornire una pagina della finestra delle proprietà la possibilità di specificare quale controllo finestra di dialogo deve ricevere lo stato attivo iniziale. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Controlli di Windows per il codice di notifica PSN_QUERYINITIALFOCUS
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119079"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="a40cc-105">\_Codice di notifica QUERYINITIALFOCUS PSN</span><span class="sxs-lookup"><span data-stu-id="a40cc-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="a40cc-106">Inviato da una finestra delle proprietà per fornire una pagina della finestra delle proprietà la possibilità di specificare quale controllo finestra di dialogo deve ricevere lo stato attivo iniziale.</span><span class="sxs-lookup"><span data-stu-id="a40cc-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="a40cc-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a40cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a40cc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a40cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a40cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a40cc-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) .</span><span class="sxs-lookup"><span data-stu-id="a40cc-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="a40cc-111">Eseguire il cast del membro **lParam** di questa struttura in un tipo **HWND** per recuperare l'handle del controllo a cui verrà assegnato lo stato attivo per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a40cc-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="a40cc-112">La struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a40cc-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40cc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a40cc-113">Return value</span></span>

<span data-ttu-id="a40cc-114">Per specificare quale controllo deve ricevere lo stato attivo, restituire l'handle del controllo.</span><span class="sxs-lookup"><span data-stu-id="a40cc-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="a40cc-115">In caso contrario, restituirà zero e lo stato attivo passerà al controllo predefinito.</span><span class="sxs-lookup"><span data-stu-id="a40cc-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="a40cc-116">Per impostare il valore restituito, è necessario che la routine della finestra di dialogo chiami la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valore **\_ MSGRESULT DWL** e restituisca **true**.</span><span class="sxs-lookup"><span data-stu-id="a40cc-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40cc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a40cc-117">Remarks</span></span>

<span data-ttu-id="a40cc-118">Un'applicazione non deve chiamare la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) durante la gestione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a40cc-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="a40cc-119">Restituisce l'handle del controllo che deve ricevere lo stato attivo e il gestore della finestra delle proprietà gestirà la modifica dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="a40cc-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="a40cc-120">Il \_ codice di notifica QUERYINITIALFOCUS PSN non viene inviato se il gestore della finestra delle proprietà determina che nessun controllo nella pagina deve ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="a40cc-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="a40cc-121">Questo frammento di codice implementa un semplice gestore per PSN \_ QUERYINITIALFOCUS.</span><span class="sxs-lookup"><span data-stu-id="a40cc-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="a40cc-122">Richiede che lo stato attivo iniziale venga assegnato al controllo location (**\_ posizione IDC**).</span><span class="sxs-lookup"><span data-stu-id="a40cc-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="a40cc-123">Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a40cc-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a40cc-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a40cc-124">Requirements</span></span>



| <span data-ttu-id="a40cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40cc-125">Requirement</span></span> | <span data-ttu-id="a40cc-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a40cc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a40cc-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a40cc-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a40cc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a40cc-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a40cc-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a40cc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a40cc-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a40cc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a40cc-132"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a40cc-132"><dt>Prsht.h</dt></span></span> </dl> |



 

