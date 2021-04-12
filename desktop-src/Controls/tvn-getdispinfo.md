---
title: Codice di notifica TVN_GETDISPINFO (COMmctrl. h)
description: Richiede che la finestra padre di un controllo di visualizzazione albero fornisca le informazioni necessarie per visualizzare o ordinare un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Controlli di Windows per il codice di notifica TVN_GETDISPINFO
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517829"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="5322e-105">\_Codice di notifica GETDISPINFO di TVN</span><span class="sxs-lookup"><span data-stu-id="5322e-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="5322e-106">Richiede che la finestra padre di un controllo di visualizzazione albero fornisca le informazioni necessarie per visualizzare o ordinare un elemento.</span><span class="sxs-lookup"><span data-stu-id="5322e-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="5322e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5322e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="5322e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5322e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5322e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5322e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5322e-110">Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5322e-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="5322e-111">Il membro dell' **elemento** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **mask**, **hitet**, **state** e **lParam** specificano il tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="5322e-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="5322e-112">È necessario compilare i membri della struttura con le informazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="5322e-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5322e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5322e-113">Return value</span></span>

<span data-ttu-id="5322e-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5322e-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5322e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5322e-115">Remarks</span></span>

<span data-ttu-id="5322e-116">Questo codice di notifica viene inviato nelle circostanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="5322e-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="5322e-117">Se il membro **pszText** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore TEXTCALLBACK di LPSTR \_ , il controllo Invia questo codice di notifica per recuperare il testo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5322e-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="5322e-118">In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag di testo TVIF.</span><span class="sxs-lookup"><span data-stu-id="5322e-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="5322e-119">Se il membro **IImage** o **ISelectedImage** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ IMAGECALLBACK, il controllo Invia questo codice di notifica per recuperare l'indice delle icone di un elemento nell'elenco immagini del controllo.</span><span class="sxs-lookup"><span data-stu-id="5322e-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="5322e-120">In questo caso, se l'elemento è selezionato, il membro **mask** di *lParam* avrà il flag TVIF \_ SELECTEDIMAGE impostato.</span><span class="sxs-lookup"><span data-stu-id="5322e-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="5322e-121">Se l'elemento non è selezionato, per il membro **mask** di *lParam* verrà impostato il \_ flag immagine TVIF.</span><span class="sxs-lookup"><span data-stu-id="5322e-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="5322e-122">Se il membro **cfigli** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento è il valore i \_ CHILDRENCALLBACK, il controllo Invia questo codice di notifica per recuperare un valore che indica se l'elemento contiene elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="5322e-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="5322e-123">In questo caso, per il membro **mask** di *lParam* verrà impostato il \_ flag TVIF Children.</span><span class="sxs-lookup"><span data-stu-id="5322e-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5322e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5322e-124">Requirements</span></span>



| <span data-ttu-id="5322e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5322e-125">Requirement</span></span> | <span data-ttu-id="5322e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5322e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5322e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5322e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5322e-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5322e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5322e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5322e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5322e-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5322e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5322e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5322e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5322e-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5322e-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5322e-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5322e-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5322e-134">**TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5322e-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5322e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5322e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5322e-136">\_SETDISPINFO TVN</span><span class="sxs-lookup"><span data-stu-id="5322e-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 





