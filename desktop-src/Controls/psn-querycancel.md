---
title: Codice di notifica PSN_QUERYCANCEL (Prsht. h)
description: Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- Controlli di Windows per il codice di notifica PSN_QUERYCANCEL
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964111"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="7a718-105">\_Codice di notifica QUERYCANCEL PSN</span><span class="sxs-lookup"><span data-stu-id="7a718-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="7a718-106">Indica che l'utente ha annullato la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a718-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="7a718-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a718-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="7a718-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a718-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a718-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a718-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a718-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7a718-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="7a718-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a718-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="7a718-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="7a718-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a718-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a718-113">Return value</span></span>

<span data-ttu-id="7a718-114">Restituisce **true** per evitare l'operazione di annullamento o **false** per consentirne l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7a718-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a718-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a718-115">Remarks</span></span>

<span data-ttu-id="7a718-116">Questo codice di notifica viene in genere inviato quando un utente fa clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="7a718-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="7a718-117">Viene inoltre inviato quando un utente fa clic sul pulsante **X** nell'angolo superiore destro della finestra delle proprietà oppure preme il tasto di escape.</span><span class="sxs-lookup"><span data-stu-id="7a718-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="7a718-118">Una pagina della finestra delle proprietà può gestire questo codice di notifica per richiedere all'utente di verificare l'operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="7a718-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="7a718-119">Per impostare un valore restituito, la routine della finestra di dialogo per la pagina deve chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT impostato sul valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7a718-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="7a718-120">La routine della finestra di dialogo deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="7a718-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a718-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a718-121">Requirements</span></span>



| <span data-ttu-id="7a718-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a718-122">Requirement</span></span> | <span data-ttu-id="7a718-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7a718-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a718-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a718-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a718-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a718-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7a718-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a718-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a718-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a718-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a718-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a718-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a718-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a718-129"><dt>Prsht.h</dt></span></span> </dl> |



 

