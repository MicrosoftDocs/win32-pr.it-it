---
title: Messaggio TB_SETIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano nello stato predefinito.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Controlli di Windows Message TB_SETIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302124"
---
# <a name="tb_setimagelist-message"></a><span data-ttu-id="0ddae-104">TB- \_ messaggio di DIimmagine</span><span class="sxs-lookup"><span data-stu-id="0ddae-104">TB\_SETIMAGELIST message</span></span>

<span data-ttu-id="0ddae-105">Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="0ddae-105">Sets the image list that the toolbar uses to display buttons that are in their default state.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ddae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ddae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ddae-107">*wParam*</span></span> 
</dt> <dd>

[<span data-ttu-id="0ddae-108">Versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="0ddae-108">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="0ddae-109">Indice dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0ddae-109">The index of the list.</span></span> <span data-ttu-id="0ddae-110">Se si usa un solo elenco di immagini o una versione precedente dei controlli comuni, impostare *wParam* su zero.</span><span class="sxs-lookup"><span data-stu-id="0ddae-110">If you use only one image list, or an earlier version of the common controls, set *wParam* to zero.</span></span> <span data-ttu-id="0ddae-111">Per informazioni dettagliate sull'uso di più elenchi di immagini, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0ddae-111">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="0ddae-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ddae-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ddae-113">Handle per l'elenco di immagini da impostare.</span><span class="sxs-lookup"><span data-stu-id="0ddae-113">Handle to the image list to set.</span></span> <span data-ttu-id="0ddae-114">Se questo parametro è **null**, non viene visualizzata alcuna immagine nei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0ddae-114">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddae-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ddae-115">Return value</span></span>

<span data-ttu-id="0ddae-116">Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti nello stato predefinito oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="0ddae-116">Returns the handle to the image list previously used to display buttons in their default state, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ddae-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ddae-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ddae-118">L'applicazione è responsabile di liberare l'elenco di immagini dopo che la barra degli strumenti è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="0ddae-118">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="0ddae-119">Il **messaggio \_** non può essere combinato con [**TB \_ ADDBITMAP**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="0ddae-119">The **TB\_SETIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="0ddae-120">Non può essere usato anche con le barre degli strumenti create con [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), che chiama **TB \_ ADDBITMAP** internamente.</span><span class="sxs-lookup"><span data-stu-id="0ddae-120">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="0ddae-121">Quando si crea una barra degli strumenti con **CreateToolbarEx** o si usa **TB \_ ADDBITMAP** per aggiungere immagini, la barra degli strumenti gestisce l'elenco di immagini internamente.</span><span class="sxs-lookup"><span data-stu-id="0ddae-121">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="0ddae-122">Il tentativo di modificarlo con l'insieme di **\_ Immagini TB** presenta conseguenze imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="0ddae-122">Attempting to modify it with **TB\_SETIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="0ddae-123">Con la [versione 5,80](common-control-versions.md) o successive dei controlli comuni, le immagini dei pulsanti non devono provenire dallo stesso elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="0ddae-123">With [version 5.80](common-control-versions.md) or later of the common controls, button images need not come from the same image list.</span></span> <span data-ttu-id="0ddae-124">Per usare più elenchi di immagini per le immagini dei pulsanti della barra degli strumenti:</span><span class="sxs-lookup"><span data-stu-id="0ddae-124">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="0ddae-125">Abilitare più elenchi di immagini inviando la barra degli strumenti controllare un messaggio di [**\_ versione CCM**](ccm-setversion.md) con *wParam* (il numero di versione) impostato su 5.</span><span class="sxs-lookup"><span data-stu-id="0ddae-125">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="0ddae-126">Per ogni elenco di immagini da usare, inviare la barra degli strumenti per il controllo di un messaggio di sedicizzazione **TB \_** .</span><span class="sxs-lookup"><span data-stu-id="0ddae-126">For each image list you want to use, send the toolbar control a **TB\_SETIMAGELIST** message.</span></span> <span data-ttu-id="0ddae-127">Impostare *wParam* su un valore *wParam* definito dall'applicazione che verrà utilizzato per identificare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="0ddae-127">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="0ddae-128">Impostare *lParam* sull'handle HIMAGELIST dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0ddae-128">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="0ddae-129">Per ogni pulsante, impostare il membro **iBitmap** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante su MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="0ddae-129">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="0ddae-130">Il valore *iImageID* è l'ID dell'elenco di immagini appropriato definito nel passaggio due.</span><span class="sxs-lookup"><span data-stu-id="0ddae-130">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="0ddae-131">Il valore *iIndex* è l'indice dell'immagine particolare all'interno dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0ddae-131">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="0ddae-132">Aggiungere i pulsanti inviando la barra degli strumenti per il controllo di un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="0ddae-132">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="0ddae-133">Nel frammento di codice seguente viene illustrato come aggiungere cinque pulsanti a una barra degli strumenti, con immagini di tre diversi elenchi di immagini.</span><span class="sxs-lookup"><span data-stu-id="0ddae-133">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="0ddae-134">Il supporto per più elenchi di immagini è abilitato con un messaggio di [**\_ versione CCM**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="0ddae-134">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="0ddae-135">Gli elenchi di immagini vengono quindi impostati e assegnati gli ID 0-2.</span><span class="sxs-lookup"><span data-stu-id="0ddae-135">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="0ddae-136">Ai pulsanti vengono assegnate immagini dagli elenchi di immagini, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0ddae-136">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="0ddae-137">Il pulsante 0 è compreso nell'elenco di immagini zero (Ahim \[ 0 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="0ddae-137">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="0ddae-138">Il pulsante 1 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="0ddae-138">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="0ddae-139">Il pulsante 2 è da Image List Two (Ahim \[ 2 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="0ddae-139">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="0ddae-140">Il pulsante 3 è da Image List zero (Ahim \[ 0 \] ) con indice 2.</span><span class="sxs-lookup"><span data-stu-id="0ddae-140">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="0ddae-141">Il pulsante 4 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 3.</span><span class="sxs-lookup"><span data-stu-id="0ddae-141">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="0ddae-142">Infine, i pulsanti vengono aggiunti al controllo Toolbar con un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="0ddae-142">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="0ddae-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ddae-143">Requirements</span></span>



| <span data-ttu-id="0ddae-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ddae-144">Requirement</span></span> | <span data-ttu-id="0ddae-145">Valore</span><span class="sxs-lookup"><span data-stu-id="0ddae-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddae-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ddae-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddae-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ddae-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ddae-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ddae-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddae-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ddae-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ddae-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ddae-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddae-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddae-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddae-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ddae-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ddae-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0ddae-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

