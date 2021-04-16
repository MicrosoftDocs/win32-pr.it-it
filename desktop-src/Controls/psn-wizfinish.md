---
title: Codice di notifica PSN_WIZFINISH (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante fine in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Controlli di Windows per il codice di notifica PSN_WIZFINISH
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477891"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="f8405-105">\_Codice di notifica WIZFINISH PSN</span><span class="sxs-lookup"><span data-stu-id="f8405-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="f8405-106">Notifica a una pagina che l'utente ha fatto clic sul pulsante **fine** in una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f8405-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="f8405-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f8405-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f8405-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8405-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8405-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8405-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8405-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f8405-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="f8405-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8405-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="f8405-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="f8405-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8405-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8405-113">Return value</span></span>

-   <span data-ttu-id="f8405-114">Restituisce **true** per impedire il completamento della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f8405-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="f8405-115">Versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="f8405-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="f8405-116">e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f8405-116">and later.</span></span> <span data-ttu-id="f8405-117">Restituisce un handle di finestra per impedire il completamento della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f8405-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="f8405-118">La procedura guidata imposta lo stato attivo su tale finestra.</span><span class="sxs-lookup"><span data-stu-id="f8405-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="f8405-119">La finestra deve essere di proprietà della pagina della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f8405-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="f8405-120">Restituisce **false** per consentire il completamento della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f8405-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8405-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8405-121">Remarks</span></span>

<span data-ttu-id="f8405-122">Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="f8405-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="f8405-123">Versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="f8405-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="f8405-124">Se l'applicazione restituisce **true** per impedire che venga completata una procedura guidata, non ha alcun controllo su quale finestra della pagina riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f8405-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="f8405-125">Le applicazioni che devono arrestare una procedura guidata devono in genere eseguire questa operazione restituendo l'handle della finestra nella pagina della procedura guidata che consente di ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f8405-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8405-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8405-126">Requirements</span></span>



| <span data-ttu-id="f8405-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8405-127">Requirement</span></span> | <span data-ttu-id="f8405-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f8405-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8405-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8405-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8405-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8405-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8405-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8405-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8405-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8405-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8405-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8405-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8405-134"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8405-134"><dt>Prsht.h</dt></span></span> </dl> |



 

