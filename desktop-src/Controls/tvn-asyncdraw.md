---
title: Codice di notifica TVN_ASYNCDRAW (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrapposizione non riesce. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Controlli di Windows per il codice di notifica TVN_ASYNCDRAW
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302510"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="2955f-105">\_Codice di notifica ASYNCDRAW di TVN</span><span class="sxs-lookup"><span data-stu-id="2955f-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="2955f-106">Inviato da un controllo di visualizzazione albero al relativo elemento padre quando il disegno di un'icona o di una sovrapposizione non riesce.</span><span class="sxs-lookup"><span data-stu-id="2955f-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="2955f-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2955f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2955f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2955f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2955f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2955f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2955f-110">Puntatore a una struttura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="2955f-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="2955f-111">La struttura **NMTVASYNCDRAW** contiene il motivo per cui il progetto non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2955f-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2955f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2955f-112">Return value</span></span>

<span data-ttu-id="2955f-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2955f-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2955f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2955f-114">Remarks</span></span>

<span data-ttu-id="2955f-115">Il controllo di visualizzazione albero deve avere lo stile esteso [**\_ \_ DRAWIMAGEASYNC TV ex**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2955f-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="2955f-116">Si noti che questa operazione equivale al flag ASYNCDRAWN LVN di visualizzazione elenco \_ e allo stile corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2955f-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="2955f-117">Questo controllo non viene disegnato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2955f-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="2955f-118">Il valore asincrono viene usato nel contesto in cui il controllo di visualizzazione albero non estrae in modo sincrono un'immagine se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="2955f-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="2955f-119">Ad esempio, l'immagine potrebbe non essere disponibile se il controllo di visualizzazione albero utilizza un elenco di immagini di tipo sparse, poiché l'immagine potrebbe essere scaricata. Al contrario, quando un'immagine non è disponibile, il controllo chiede in modo sincrono all'elemento padre quale azione intraprendere inviando al padre una \_ notifica ASYNCDRAW di TVN con una struttura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="2955f-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="2955f-120">Il membro **HR** di questa struttura descrive il motivo per cui il progetto del controllo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2955f-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="2955f-121">Un risultato **HR** di E \_ in sospeso indica che l'immagine non è presente (l'immagine deve essere estratta).</span><span class="sxs-lookup"><span data-stu-id="2955f-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="2955f-122">Success indica che l'immagine è presente ma non con la qualità dell'immagine richiesta.</span><span class="sxs-lookup"><span data-stu-id="2955f-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="2955f-123">Il padre imposta il membro **dwRetFlags** della struttura per informare il controllo come procedere.</span><span class="sxs-lookup"><span data-stu-id="2955f-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="2955f-124">Ad esempio, l'elemento padre può restituire un'altra immagine, nel membro **iRetImageIndex** , per il controllo da creare.</span><span class="sxs-lookup"><span data-stu-id="2955f-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="2955f-125">In questo caso, l'elemento padre imposta il membro **dwRetFlags** su ADRF \_ DRAWIMAGE.</span><span class="sxs-lookup"><span data-stu-id="2955f-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="2955f-126">Se il controllo rileva che l'immagine restituita non è stata estratta, è \_ possibile che il controllo invii un'altra notifica ASYNCDRAW di TVN.</span><span class="sxs-lookup"><span data-stu-id="2955f-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="2955f-127">Se un'immagine non è disponibile, l'idea dietro asincrona consiste nel consentire all'elemento padre di eseguire l'estrazione in background, in modo che l'estrazione non blocchi il thread dell'interfaccia utente, ovvero il thread su cui si trova il controllo.</span><span class="sxs-lookup"><span data-stu-id="2955f-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="2955f-128">L'elemento padre può restituire ADRF \_ DRAWNOTHING al controllo, quindi avviare un thread in background per estrarre l'icona.</span><span class="sxs-lookup"><span data-stu-id="2955f-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="2955f-129">Una volta estratto, l'elemento padre può impostare l'icona nel controllo TreeView con la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span><span class="sxs-lookup"><span data-stu-id="2955f-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="2955f-130">In questo modo, la visualizzazione albero non invalida l'elemento e infine lo ridisegna con l'immagine estratta nell'elenco immagini.</span><span class="sxs-lookup"><span data-stu-id="2955f-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="2955f-131">L'esempio di codice seguente, da usare come parte di un programma più ampio, Mostra come un elemento padre può elaborare due possibili codici restituiti in questa notifica da un controllo e decidere quale azione deve assumere il controllo.</span><span class="sxs-lookup"><span data-stu-id="2955f-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="2955f-132">L'impostazione di **dwRetFlags** non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="2955f-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="2955f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2955f-133">Requirements</span></span>



| <span data-ttu-id="2955f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2955f-134">Requirement</span></span> | <span data-ttu-id="2955f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2955f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2955f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2955f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2955f-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2955f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2955f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2955f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2955f-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2955f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2955f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2955f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2955f-141"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2955f-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





