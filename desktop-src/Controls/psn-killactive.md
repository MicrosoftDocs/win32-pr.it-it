---
title: Codice di notifica PSN_KILLACTIVE (Prsht. h)
description: Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o se l'utente ha fatto clic sul pulsante OK. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Controlli di Windows per il codice di notifica PSN_KILLACTIVE
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964113"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="9f034-105">\_Codice di notifica KILLACTIVE PSN</span><span class="sxs-lookup"><span data-stu-id="9f034-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="9f034-106">Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o se l'utente ha fatto clic sul pulsante OK.</span><span class="sxs-lookup"><span data-stu-id="9f034-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="9f034-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9f034-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9f034-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f034-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f034-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f034-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9f034-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="9f034-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f034-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="9f034-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="9f034-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f034-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f034-113">Return value</span></span>

<span data-ttu-id="9f034-114">Restituisce **true** per evitare che la pagina perda l'attivazione o **false** per consentirne l'attivazione.</span><span class="sxs-lookup"><span data-stu-id="9f034-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f034-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f034-115">Remarks</span></span>

<span data-ttu-id="9f034-116">Un'applicazione gestisce questo codice di notifica per convalidare le informazioni immesse dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9f034-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="9f034-117">La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica KILLACTIVE PSN.</span><span class="sxs-lookup"><span data-stu-id="9f034-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="9f034-118">Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9f034-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="9f034-119">In questo modo si otterranno risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="9f034-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="9f034-120">Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un \_ valore DWL MSGRESULT impostato sul valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9f034-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="9f034-121">La routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="9f034-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="9f034-122">Se la routine della finestra di dialogo Imposta DWL \_ MSGRESULT su **true**, verrà visualizzata una finestra di messaggio per spiegare il problema all'utente.</span><span class="sxs-lookup"><span data-stu-id="9f034-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f034-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f034-123">Requirements</span></span>



| <span data-ttu-id="9f034-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f034-124">Requirement</span></span> | <span data-ttu-id="9f034-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9f034-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f034-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f034-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9f034-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f034-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9f034-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f034-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9f034-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f034-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9f034-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f034-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f034-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f034-131"><dt>Prsht.h</dt></span></span> </dl> |



 

