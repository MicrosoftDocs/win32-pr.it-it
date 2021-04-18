---
title: Codice di notifica PSN_RESET (Prsht. h)
description: Notifica a una pagina che la finestra delle proprietà sta per essere eliminata definitivamente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- Controlli di Windows per il codice di notifica PSN_RESET
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301180"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="a5158-105">\_Codice di notifica di reimpostazione di PSN</span><span class="sxs-lookup"><span data-stu-id="a5158-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="a5158-106">Notifica a una pagina che la finestra delle proprietà sta per essere eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="a5158-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="a5158-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a5158-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5158-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5158-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5158-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5158-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5158-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a5158-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5158-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5158-111">Return value</span></span>

<span data-ttu-id="a5158-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a5158-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5158-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5158-113">Remarks</span></span>

<span data-ttu-id="a5158-114">Tutte le modifiche apportate dopo l'ultimo codice di notifica dell' [ \_ applicazione di PSN](psn-apply.md) vengono annullate, tranne nel caso di [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), che non supporta tale codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a5158-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="a5158-115">Il membro **lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* verrà impostato su **true** se l'utente ha fatto clic sul pulsante **X** nell'angolo superiore destro della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5158-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="a5158-116">Sarà **false** se l'utente ha fatto clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="a5158-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="a5158-117">La struttura **PSHNOTIFY** contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5158-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="a5158-118">Un'applicazione può usare questo codice di notifica come opportunità per eseguire operazioni di pulizia.</span><span class="sxs-lookup"><span data-stu-id="a5158-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="a5158-119">La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando \_ viene inviato il codice di notifica di reimpostazione di PSN.</span><span class="sxs-lookup"><span data-stu-id="a5158-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="a5158-120">Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a5158-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="a5158-121">In questo modo si otterranno risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="a5158-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="a5158-122">Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a5158-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5158-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5158-123">Requirements</span></span>



| <span data-ttu-id="a5158-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5158-124">Requirement</span></span> | <span data-ttu-id="a5158-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a5158-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5158-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5158-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5158-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5158-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5158-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5158-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5158-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a5158-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5158-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5158-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5158-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5158-131"><dt>Prsht.h</dt></span></span> </dl> |



 

