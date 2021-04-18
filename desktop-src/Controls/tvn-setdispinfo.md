---
title: Codice di notifica TVN_SETDISPINFO (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che deve aggiornare le informazioni che gestisce su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- Controlli di Windows per il codice di notifica TVN_SETDISPINFO
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301176"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="09fba-105">\_Codice di notifica SETDISPINFO di TVN</span><span class="sxs-lookup"><span data-stu-id="09fba-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="09fba-106">Notifica alla finestra padre di un controllo di visualizzazione albero che deve aggiornare le informazioni che gestisce su un elemento.</span><span class="sxs-lookup"><span data-stu-id="09fba-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="09fba-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="09fba-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="09fba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09fba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09fba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09fba-110">Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) che descrive l'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="09fba-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="09fba-111">Il membro **hitey** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) specifica l'elemento da aggiornare e il membro **mask** specifica gli attributi dell'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="09fba-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09fba-112">Return value</span></span>

<span data-ttu-id="09fba-113">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="09fba-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="09fba-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="09fba-114">Remarks</span></span>

<span data-ttu-id="09fba-115">Se il membro **pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore TEXTCALLBACK di LPSTR \_ , il controllo Invia la notifica per impostare il testo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="09fba-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="09fba-116">In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag di testo TVIF.</span><span class="sxs-lookup"><span data-stu-id="09fba-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="09fba-117">Se il membro **IImage** o **ISelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ IMAGECALLBACK, il controllo Invia la notifica per recuperare l'indice dell'immagine dell'icona da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="09fba-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="09fba-118">In questo caso, per il membro **mask** di *lParam* sarà impostata l' \_ immagine TVIF o il \_ flag TVIF SELECTEDIMAGE.</span><span class="sxs-lookup"><span data-stu-id="09fba-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fba-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09fba-119">Requirements</span></span>



| <span data-ttu-id="09fba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fba-120">Requirement</span></span> | <span data-ttu-id="09fba-121">Valore</span><span class="sxs-lookup"><span data-stu-id="09fba-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09fba-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09fba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09fba-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09fba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09fba-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09fba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09fba-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09fba-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09fba-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09fba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fba-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fba-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="09fba-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="09fba-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="09fba-129">**TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="09fba-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="09fba-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09fba-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fba-131">**TVITEM**</span><span class="sxs-lookup"><span data-stu-id="09fba-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="09fba-132">**TVITEMEX**</span><span class="sxs-lookup"><span data-stu-id="09fba-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="09fba-133">\_GETDISPINFO TVN</span><span class="sxs-lookup"><span data-stu-id="09fba-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 





