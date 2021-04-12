---
title: Messaggio TB_SETPRESSEDIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano in uno stato premuto.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- Controlli di Windows Message TB_SETPRESSEDIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519302"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="586d9-104">TB \_ SETPRESSEDIMAGELIST messaggio</span><span class="sxs-lookup"><span data-stu-id="586d9-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="586d9-105">Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano in uno stato premuto.</span><span class="sxs-lookup"><span data-stu-id="586d9-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="586d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="586d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="586d9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="586d9-108">Indice dell'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="586d9-108">The index of the image list.</span></span> <span data-ttu-id="586d9-109">Se si usa un solo elenco di immagini, impostare questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="586d9-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="586d9-110">Per informazioni dettagliate sull'uso di più elenchi di immagini, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="586d9-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="586d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="586d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="586d9-112">Handle per l'elenco di immagini da impostare.</span><span class="sxs-lookup"><span data-stu-id="586d9-112">Handle to the image list to set.</span></span> <span data-ttu-id="586d9-113">Se questo parametro è **null**, non viene visualizzata alcuna immagine nei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="586d9-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586d9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="586d9-114">Return value</span></span>

<span data-ttu-id="586d9-115">Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti nello stato premuto oppure **null** se tale elenco di immagini non è stato impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="586d9-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="586d9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="586d9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="586d9-117">L'applicazione è responsabile di liberare l'elenco di immagini dopo che la barra degli strumenti è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="586d9-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="586d9-118">Il **messaggio \_ SETPRESSEDIMAGELIST TB** non può essere combinato [**con \_ TB ADDBITMAP**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="586d9-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="586d9-119">Non può essere usato anche con le barre degli strumenti create con [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), che chiama **TB \_ ADDBITMAP** internamente.</span><span class="sxs-lookup"><span data-stu-id="586d9-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="586d9-120">Quando si crea una barra degli strumenti con **CreateToolbarEx** o si usa **TB \_ ADDBITMAP** per aggiungere immagini, la barra degli strumenti gestisce l'elenco di immagini internamente.</span><span class="sxs-lookup"><span data-stu-id="586d9-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="586d9-121">Il tentativo di modificarlo con **TB \_ SETPRESSEDIMAGELIST** ha conseguenze imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="586d9-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="586d9-122">Le immagini dei pulsanti non devono provenire dallo stesso elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="586d9-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="586d9-123">Per usare più elenchi di immagini per le immagini dei pulsanti della barra degli strumenti:</span><span class="sxs-lookup"><span data-stu-id="586d9-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="586d9-124">Abilitare più elenchi di immagini inviando la barra degli strumenti controllare un messaggio di [**\_ versione CCM**](ccm-setversion.md) con *wParam* (il numero di versione) impostato su 5.</span><span class="sxs-lookup"><span data-stu-id="586d9-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="586d9-125">Per ogni elenco di immagini che si vuole usare, inviare il controllo Toolbar a **TB \_ SETPRESSEDIMAGELIST** messaggio.</span><span class="sxs-lookup"><span data-stu-id="586d9-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="586d9-126">Impostare *wParam* su un valore *wParam* definito dall'applicazione che verrà utilizzato per identificare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="586d9-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="586d9-127">Impostare *lParam* sull'handle HIMAGELIST dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="586d9-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="586d9-128">Per ogni pulsante, impostare il membro **iBitmap** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante su MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="586d9-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="586d9-129">Il valore *iImageID* è l'ID dell'elenco di immagini appropriato definito nel passaggio due.</span><span class="sxs-lookup"><span data-stu-id="586d9-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="586d9-130">Il valore *iIndex* è l'indice dell'immagine particolare all'interno dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="586d9-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="586d9-131">Aggiungere i pulsanti inviando la barra degli strumenti per il controllo di un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="586d9-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="586d9-132">Nel frammento di codice seguente viene illustrato come aggiungere cinque pulsanti a una barra degli strumenti, con immagini di tre diversi elenchi di immagini.</span><span class="sxs-lookup"><span data-stu-id="586d9-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="586d9-133">Il supporto per più elenchi di immagini è abilitato con un messaggio di [**\_ versione CCM**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="586d9-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="586d9-134">Gli elenchi di immagini vengono quindi impostati e assegnati gli ID 0-2.</span><span class="sxs-lookup"><span data-stu-id="586d9-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="586d9-135">Ai pulsanti vengono assegnate immagini dagli elenchi di immagini, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="586d9-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="586d9-136">Il pulsante 0 è compreso nell'elenco di immagini zero (Ahim \[ 0 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="586d9-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="586d9-137">Il pulsante 1 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="586d9-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="586d9-138">Il pulsante 2 è da Image List Two (Ahim \[ 2 \] ) con indice 1.</span><span class="sxs-lookup"><span data-stu-id="586d9-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="586d9-139">Il pulsante 3 è da Image List zero (Ahim \[ 0 \] ) con indice 2.</span><span class="sxs-lookup"><span data-stu-id="586d9-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="586d9-140">Il pulsante 4 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 3.</span><span class="sxs-lookup"><span data-stu-id="586d9-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="586d9-141">Infine, i pulsanti vengono aggiunti al controllo Toolbar con un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="586d9-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

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



## <a name="requirements"></a><span data-ttu-id="586d9-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="586d9-142">Requirements</span></span>



| <span data-ttu-id="586d9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="586d9-143">Requirement</span></span> | <span data-ttu-id="586d9-144">Valore</span><span class="sxs-lookup"><span data-stu-id="586d9-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="586d9-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586d9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="586d9-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="586d9-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="586d9-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586d9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="586d9-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="586d9-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="586d9-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="586d9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="586d9-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="586d9-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586d9-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="586d9-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="586d9-152">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="586d9-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="586d9-153">**TB \_ GETPRESSEDIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="586d9-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="586d9-154">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="586d9-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="586d9-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="586d9-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

