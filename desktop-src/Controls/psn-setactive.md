---
title: Codice di notifica PSN_SETACTIVE (Prsht. h)
description: Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- Controlli di Windows per il codice di notifica PSN_SETACTIVE
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964468"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="c2202-105">\_Codice di notifica SEATTIVO PSN</span><span class="sxs-lookup"><span data-stu-id="c2202-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="c2202-106">Notifica a una pagina che sta per essere attivata.</span><span class="sxs-lookup"><span data-stu-id="c2202-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="c2202-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c2202-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c2202-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2202-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2202-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2202-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c2202-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="c2202-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2202-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="c2202-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="c2202-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2202-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2202-113">Return value</span></span>

<span data-ttu-id="c2202-114">Restituisce zero per accettare l'attivazione oppure-1 per attivare la pagina successiva o precedente (a seconda che l'utente abbia fatto clic sul pulsante **Avanti** o **indietro** ).</span><span class="sxs-lookup"><span data-stu-id="c2202-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="c2202-115">Per impostare l'attivazione su una pagina specifica, restituire l'identificatore di risorsa della pagina.</span><span class="sxs-lookup"><span data-stu-id="c2202-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2202-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2202-116">Remarks</span></span>

<span data-ttu-id="c2202-117">Il \_ codice di notifica SEATTIVO PSN viene inviato prima che la pagina sia visibile.</span><span class="sxs-lookup"><span data-stu-id="c2202-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="c2202-118">Un'applicazione può usare questo codice di notifica per inizializzare i dati nella pagina.</span><span class="sxs-lookup"><span data-stu-id="c2202-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="c2202-119">La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica SEATTIVO PSN.</span><span class="sxs-lookup"><span data-stu-id="c2202-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="c2202-120">Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c2202-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="c2202-121">In questo modo si otterranno risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="c2202-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="c2202-122">Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="c2202-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2202-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2202-123">Requirements</span></span>



| <span data-ttu-id="c2202-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2202-124">Requirement</span></span> | <span data-ttu-id="c2202-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c2202-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2202-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2202-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2202-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2202-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2202-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2202-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2202-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2202-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2202-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2202-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2202-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2202-131"><dt>Prsht.h</dt></span></span> </dl> |



 

