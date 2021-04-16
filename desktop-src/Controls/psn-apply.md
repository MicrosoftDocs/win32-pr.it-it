---
title: Codice di notifica PSN_APPLY (Prsht. h)
description: Inviato a ogni pagina della finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o applica e desidera che tutte le modifiche abbiano effetto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- Controlli di Windows per il codice di notifica PSN_APPLY
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477548"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="aeaa3-105">PSN \_ applicare il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="aeaa3-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="aeaa3-106">Inviato a ogni pagina della finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o applica e desidera che tutte le modifiche abbiano effetto.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="aeaa3-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aeaa3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aeaa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeaa3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aeaa3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeaa3-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica, incluso l'ID della pagina.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeaa3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aeaa3-111">Return value</span></span>

<span data-ttu-id="aeaa3-112">Impostare PSNRET \_ NOERROR per indicare che le modifiche apportate a questa pagina sono valide e sono state applicate.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="aeaa3-113">Se tutte le pagine impostano PSNRET \_ NOERROR, la finestra delle proprietà può essere eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="aeaa3-114">Per indicare che le modifiche apportate a questa pagina non sono valide e per impedire che la finestra delle proprietà venga distrutta, impostare uno dei valori restituiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="aeaa3-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="aeaa3-115">PSNRET \_ non valido.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="aeaa3-116">La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito a questa pagina.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="aeaa3-117">\_NOCHANGEPAGE PSNRET non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="aeaa3-118">La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito alla pagina con lo stato attivo quando è stato premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="aeaa3-119">Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeaa3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeaa3-120">Remarks</span></span>

<span data-ttu-id="aeaa3-121">Quando l'utente fa clic sul pulsante OK, applica o Chiudi, la finestra delle proprietà Invia una notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina attiva, offrendo la possibilità di convalidare le modifiche apportate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="aeaa3-122">Se le modifiche sono valide, la finestra delle proprietà Invia un \_ codice di notifica di applicazione PSN a ogni pagina, indirizzando l'applicazione alle nuove proprietà all'elemento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="aeaa3-123">La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica dell'applicazione PSN.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="aeaa3-124">Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione della notifica.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="aeaa3-125">In questo modo si otterranno risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="aeaa3-126">Il membro **lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* è impostato su **true** se l'utente fa clic sul pulsante OK.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="aeaa3-127">Viene inoltre impostata su **true** se il messaggio [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) è stato inviato e l'utente fa clic sul pulsante Chiudi.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="aeaa3-128">Viene impostato su **false** se l'utente fa clic sul pulsante Applica.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="aeaa3-129">La struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="aeaa3-130">Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="aeaa3-131">Una finestra delle proprietà modale viene distrutta se l'utente fa clic sul pulsante OK e ogni pagina restituisce il \_ valore PSNRET NOERROR in risposta a **PSN \_ Apply**.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="aeaa3-132">Se una pagina restituisce PSNRET \_ non valido o \_ PSNRET \_ NOCHANGEPAGE non valido, il processo Apply viene annullato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="aeaa3-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="aeaa3-133">Le pagine dopo la pagina di annullamento non riceveranno un codice di notifica per l'applicazione di PSN \_ .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="aeaa3-134">Per ricevere il codice di notifica, una pagina deve impostare il \_ valore DWL MSGRESULT su **false** in risposta al codice di notifica [ \_ KILLACTIVE di PSN](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa3-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="aeaa3-135">Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="aeaa3-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aeaa3-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeaa3-136">Requirements</span></span>



| <span data-ttu-id="aeaa3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeaa3-137">Requirement</span></span> | <span data-ttu-id="aeaa3-138">Valore</span><span class="sxs-lookup"><span data-stu-id="aeaa3-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aeaa3-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeaa3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="aeaa3-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeaa3-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aeaa3-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeaa3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="aeaa3-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aeaa3-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aeaa3-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aeaa3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeaa3-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeaa3-144"><dt>Prsht.h</dt></span></span> </dl> |



 

