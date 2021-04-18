---
title: Codice di notifica PSN_WIZNEXT (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante avanti in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- Controlli di Windows per il codice di notifica PSN_WIZNEXT
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302047"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="6d9ab-105">\_Codice di notifica WIZNEXT PSN</span><span class="sxs-lookup"><span data-stu-id="6d9ab-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="6d9ab-106">Notifica a una pagina che l'utente ha fatto clic sul pulsante **Avanti** in una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="6d9ab-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9ab-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6d9ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d9ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d9ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d9ab-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="6d9ab-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="6d9ab-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d9ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d9ab-113">Return value</span></span>

<span data-ttu-id="6d9ab-114">Restituisce 0 per consentire alla procedura guidata di passare alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="6d9ab-115">Return-1 per impedire la modifica delle pagine da parte della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="6d9ab-116">Per visualizzare una pagina specifica, restituire il relativo identificatore di risorsa della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="6d9ab-117">Se la finestra di dialogo è stata specificata con il flag [**\_ DLGINDIRECT di PSP**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , questa notifica restituisce il puntatore al modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d9ab-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d9ab-118">Remarks</span></span>

<span data-ttu-id="6d9ab-119">Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore **\_ MSGRESULT di DWL** e restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="6d9ab-120">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6d9ab-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="6d9ab-121">La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica WIZNEXT PSN.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="6d9ab-122">È possibile aggiungere, inserire o rimuovere pagine in risposta a questi codici di notifica, ma è necessario prestare particolare attenzione se si inseriscono o si rimuovono le pagine prima della pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="6d9ab-123">Se si inseriscono o si rimuovono pagine prima della pagina corrente, è necessario restituire (tramite **DWL \_ MSGRESULT**) un valore diverso da zero per specificare la nuova pagina desiderata.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="6d9ab-124">Si noti, tuttavia, che se si inserisce o si rimuove una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), è possibile che [PSN \_ KILLACTIVE](psn-killactive.md) venga inviato alla pagina errata.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="6d9ab-125">Per questo motivo, è consigliabile che le procedure guidate che aggiungono e rimuovano le pagine in modo dinamico in risposta a PSN \_ WIZNEXT e [PSN \_ WIZBACK](psn-wizback.md) eseguano questa operazione solo per le pagine alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="6d9ab-126">Se si desidera che la procedura guidata rimuova le pagine in modo accurato, lasciare le pagine dinamiche alla fine dell'elenco e tornare alle pagine permanenti prima di eliminarle.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="6d9ab-127">Si supponga, ad esempio, che una procedura guidata sia costituita da una pagina introduttiva, una serie di pagine dinamiche e una pagina di completamento e si desidera eliminare le pagine dinamiche quando l'utente raggiunge la pagina di completamento.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="6d9ab-128">La procedura guidata inizierà con due pagine, "Introduction" e "complete".</span><span class="sxs-lookup"><span data-stu-id="6d9ab-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="6d9ab-129">L'utente inizia nella pagina "Introduzione".</span><span class="sxs-lookup"><span data-stu-id="6d9ab-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="6d9ab-130">Introduzione (utente qui)</span><span class="sxs-lookup"><span data-stu-id="6d9ab-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="6d9ab-131">Completion</span><span class="sxs-lookup"><span data-stu-id="6d9ab-131">Completion</span></span>
2.  <span data-ttu-id="6d9ab-132">Quando l'utente si sposta da "Introduzione", la procedura guidata aggiunge le pagine dinamiche e inserisce l'utente nella prima pagina dinamica restituendo (tramite **DWL \_ MSGRESULT**) l'identificatore della finestra di dialogo "Dynamic 1".</span><span class="sxs-lookup"><span data-stu-id="6d9ab-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="6d9ab-133">In questo esempio sono disponibili tre pagine dinamiche.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="6d9ab-134">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6d9ab-134">Introduction</span></span>
    2.  <span data-ttu-id="6d9ab-135">Completion</span><span class="sxs-lookup"><span data-stu-id="6d9ab-135">Completion</span></span>
    3.  <span data-ttu-id="6d9ab-136">Dinamica 1 (utente qui)</span><span class="sxs-lookup"><span data-stu-id="6d9ab-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="6d9ab-137">Dinamica 2</span><span class="sxs-lookup"><span data-stu-id="6d9ab-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="6d9ab-138">Dinamica 3</span><span class="sxs-lookup"><span data-stu-id="6d9ab-138">Dynamic 3</span></span>
3.  <span data-ttu-id="6d9ab-139">Quando l'utente passa attraverso le pagine dinamiche a "Dynamic 3" e passa alla pagina successiva, l'applicazione deve inserire l'utente nella pagina "completamento".</span><span class="sxs-lookup"><span data-stu-id="6d9ab-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="6d9ab-140">Anche in questo caso, questa operazione viene eseguita restituendo (tramite **DWL \_ MSGRESULT**) l'identificatore della finestra di dialogo della pagina "completamento".</span><span class="sxs-lookup"><span data-stu-id="6d9ab-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="6d9ab-141">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6d9ab-141">Introduction</span></span>
    2.  <span data-ttu-id="6d9ab-142">Completamento (utente qui)</span><span class="sxs-lookup"><span data-stu-id="6d9ab-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="6d9ab-143">Dinamica 1</span><span class="sxs-lookup"><span data-stu-id="6d9ab-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="6d9ab-144">Dinamica 2</span><span class="sxs-lookup"><span data-stu-id="6d9ab-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="6d9ab-145">Dinamica 3</span><span class="sxs-lookup"><span data-stu-id="6d9ab-145">Dynamic 3</span></span>
4.  <span data-ttu-id="6d9ab-146">L'applicazione può quindi rimuovere le tre pagine dinamiche, numerate da tre a cinque, in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="6d9ab-147">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6d9ab-147">Introduction</span></span>
    2.  <span data-ttu-id="6d9ab-148">Completamento (utente qui)</span><span class="sxs-lookup"><span data-stu-id="6d9ab-148">Completion (User is here)</span></span>

<span data-ttu-id="6d9ab-149">Si noti che questa tecnica è necessaria solo se la procedura guidata rimuove le pagine in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="6d9ab-150">Se la procedura guidata aggiunge pagine in modo dinamico, questo processo non è necessario.</span><span class="sxs-lookup"><span data-stu-id="6d9ab-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9ab-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d9ab-151">Requirements</span></span>



| <span data-ttu-id="6d9ab-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9ab-152">Requirement</span></span> | <span data-ttu-id="6d9ab-153">Valore</span><span class="sxs-lookup"><span data-stu-id="6d9ab-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9ab-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d9ab-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9ab-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d9ab-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d9ab-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d9ab-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9ab-157">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d9ab-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d9ab-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d9ab-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d9ab-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9ab-159"><dt>Prsht.h</dt></span></span> </dl> |



 

