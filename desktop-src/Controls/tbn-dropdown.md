---
title: Codice di notifica TBN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- Controlli di Windows per il codice di notifica TBN_DROPDOWN
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964035"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="9cf29-105">\_Codice di notifica a discesa TBN</span><span class="sxs-lookup"><span data-stu-id="9cf29-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="9cf29-106">Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante a discesa.</span><span class="sxs-lookup"><span data-stu-id="9cf29-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="9cf29-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf29-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9cf29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cf29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cf29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cf29-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9cf29-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="9cf29-111">Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="9cf29-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf29-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cf29-112">Return value</span></span>

<span data-ttu-id="9cf29-113">Restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cf29-113">Returns one of the following values:</span></span>



| <span data-ttu-id="9cf29-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9cf29-114">Return code</span></span>                                                                                          | <span data-ttu-id="9cf29-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cf29-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cf29-116"><dt>**\_impostazione predefinita TBDDRET**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf29-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="9cf29-117">L'elenco a discesa è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="9cf29-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9cf29-118"><dt>**TBDDRET \_ NOdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf29-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="9cf29-119">L'elenco a discesa non è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="9cf29-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="9cf29-120"><dt>**\_TREATPRESSED TBDDRET**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf29-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="9cf29-121">L'elenco a discesa è stato gestito, ma viene considerato come un pulsante normale.</span><span class="sxs-lookup"><span data-stu-id="9cf29-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9cf29-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cf29-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9cf29-123">I pulsanti a discesa possono essere semplici (stile [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md) ), visualizzare una freccia accanto all'immagine del pulsante (stile [**\_ WHOLEDROPDOWN BTNS**](toolbar-control-and-button-styles.md) ) o visualizzare una freccia separata dall'immagine (stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="9cf29-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="9cf29-124">Se viene utilizzata una freccia separata, \_ l'elenco a discesa TBN viene inviato solo se l'utente fa clic sulla parte della freccia del pulsante.</span><span class="sxs-lookup"><span data-stu-id="9cf29-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="9cf29-125">Se l'utente fa clic sulla parte principale del pulsante, viene inviato un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con ID del pulsante, come per un pulsante standard.</span><span class="sxs-lookup"><span data-stu-id="9cf29-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="9cf29-126">Per gli altri due stili del pulsante a discesa, \_ l'elenco a discesa TBN viene inviato quando l'utente fa clic su una parte del pulsante.</span><span class="sxs-lookup"><span data-stu-id="9cf29-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9cf29-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cf29-127">Requirements</span></span>



| <span data-ttu-id="9cf29-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cf29-128">Requirement</span></span> | <span data-ttu-id="9cf29-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9cf29-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf29-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cf29-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf29-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cf29-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cf29-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cf29-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf29-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cf29-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cf29-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cf29-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cf29-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cf29-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

