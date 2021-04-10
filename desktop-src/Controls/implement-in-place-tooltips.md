---
title: Come implementare In-Place descrizioni comandi
description: Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati. Per un'illustrazione, vedere informazioni sui controlli ToolTip.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047622"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="b1085-104">Come implementare In-Place descrizioni comandi</span><span class="sxs-lookup"><span data-stu-id="b1085-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="b1085-105">Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati.</span><span class="sxs-lookup"><span data-stu-id="b1085-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="b1085-106">Per un'illustrazione, vedere [informazioni sui controlli ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b1085-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="b1085-107">La differenza tra le descrizioni comandi ordinarie e quelle sul posto è il posizionamento.</span><span class="sxs-lookup"><span data-stu-id="b1085-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="b1085-108">Per impostazione predefinita, quando il puntatore del mouse viene posizionato su un'area a cui è associata una descrizione comando, la descrizione comando viene visualizzata accanto all'area.</span><span class="sxs-lookup"><span data-stu-id="b1085-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="b1085-109">Tuttavia, le descrizioni comandi sono finestre e possono essere posizionate in qualsiasi punto in cui si sceglie chiamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="b1085-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="b1085-110">La creazione di una descrizione comando sul posto consiste nel posizionare la finestra della descrizione comando in modo da sovrapporre la stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="b1085-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b1085-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="b1085-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b1085-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="b1085-112">Technologies</span></span>

-   [<span data-ttu-id="b1085-113">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="b1085-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b1085-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b1085-114">Prerequisites</span></span>

-   <span data-ttu-id="b1085-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="b1085-115">C/C++</span></span>
-   <span data-ttu-id="b1085-116">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="b1085-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b1085-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="b1085-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="b1085-118">Posizionamento di una descrizione comando In-Place</span><span class="sxs-lookup"><span data-stu-id="b1085-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="b1085-119">È necessario tenere traccia di tre rettangoli quando si posiziona una descrizione comando sul posto:</span><span class="sxs-lookup"><span data-stu-id="b1085-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="b1085-120">Rettangolo che racchiude il testo completo dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="b1085-121">Rettangolo che racchiude il testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="b1085-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="b1085-122">Il testo della descrizione comando è identico al testo dell'etichetta completo e, in genere, ha le stesse dimensioni e il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="b1085-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="b1085-123">In genere, i due rettangoli di testo hanno le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b1085-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="b1085-124">Rettangolo della finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="b1085-124">The tooltip window rectangle.</span></span> <span data-ttu-id="b1085-125">Questo rettangolo è leggermente più grande del rettangolo di testo della descrizione comando che racchiude.</span><span class="sxs-lookup"><span data-stu-id="b1085-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="b1085-126">I tre rettangoli vengono visualizzati schematicamente nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b1085-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="b1085-127">La parte nascosta del testo dell'etichetta è indicata da uno sfondo grigio.</span><span class="sxs-lookup"><span data-stu-id="b1085-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![diagramma che mostra una stringa lunga, metà delle quali ha uno sfondo grigio, quindi la stessa stringa all'interno di un rettangolo della finestra della descrizione comando più grande](images/inplace.png)

<span data-ttu-id="b1085-129">Per creare una descrizione comando sul posto, è necessario posizionare il rettangolo del testo della descrizione comando in modo che sovrimpressione il rettangolo del testo dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="b1085-130">La procedura per allineare i due rettangoli è relativamente semplice:</span><span class="sxs-lookup"><span data-stu-id="b1085-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="b1085-131">Definire il rettangolo del testo dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="b1085-132">Posizionare la finestra della descrizione comando in modo che il rettangolo del testo della descrizione comandi sovrapposto al rettangolo del testo dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="b1085-133">In pratica, è in genere sufficiente allineare l'angolo superiore sinistro dei due rettangoli di testo.</span><span class="sxs-lookup"><span data-stu-id="b1085-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="b1085-134">Il tentativo di ridimensionare il rettangolo testo della descrizione comando in modo che corrisponda esattamente al rettangolo del testo dell'etichetta può causare problemi con la visualizzazione della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="b1085-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="b1085-135">Il problema con questo semplice schema è che non è possibile posizionare direttamente il rettangolo del testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="b1085-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="b1085-136">Al contrario, è necessario posizionare il rettangolo della finestra della descrizione comando abbastanza a lungo e a sinistra del rettangolo di testo dell'etichetta in modo che gli angoli dei due rettangoli di testo coincidano.</span><span class="sxs-lookup"><span data-stu-id="b1085-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="b1085-137">In altre parole, è necessario essere a conoscenza dell'offset tra il rettangolo della finestra della descrizione comando e il rettangolo del testo racchiuso.</span><span class="sxs-lookup"><span data-stu-id="b1085-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="b1085-138">In generale, non esiste un modo semplice per determinare questo offset.</span><span class="sxs-lookup"><span data-stu-id="b1085-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="b1085-139">Implementare descrizioni comando In-Place</span><span class="sxs-lookup"><span data-stu-id="b1085-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="b1085-140">Il frammento di codice seguente illustra come usare un messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) in un gestore di visualizzazione [TTN \_](ttn-show.md) per visualizzare una descrizione comando sul posto.</span><span class="sxs-lookup"><span data-stu-id="b1085-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="b1085-141">L'applicazione indica che il testo dell'etichetta viene troncato impostando la variabile *fMyStringIsTruncated* privata su **true**.</span><span class="sxs-lookup"><span data-stu-id="b1085-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="b1085-142">Il gestore chiama una funzione definita dall'applicazione, **GetMyItemRect**, per recuperare il rettangolo del testo dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="b1085-143">Questo rettangolo viene passato al controllo ToolTip con **TTM \_ ADJUSTRECT**, che restituisce il rettangolo della finestra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b1085-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="b1085-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) viene quindi chiamato per posizionare la descrizione comando sull'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b1085-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="b1085-145">In questo esempio non viene modificata la dimensione della descrizione comando, bensì solo la relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="b1085-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="b1085-146">I due rettangoli di testo sono allineati negli angoli in alto a sinistra, ma non necessariamente con le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b1085-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="b1085-147">In pratica, la differenza è di solito ridotta e questo approccio è consigliato per la maggior parte degli scopi.</span><span class="sxs-lookup"><span data-stu-id="b1085-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="b1085-148">Sebbene sia possibile, in linea di principio, usare [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per ridimensionare e riposizionare la descrizione comando, in questo modo potrebbe avere conseguenze imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="b1085-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1085-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1085-149">Remarks</span></span>

<span data-ttu-id="b1085-150">Controlli comuni [versione 5,80](common-control-versions.md) semplifica l'uso di descrizioni comando sul posto mediante l'aggiunta di un nuovo messaggio, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md).</span><span class="sxs-lookup"><span data-stu-id="b1085-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="b1085-151">Inviare questo messaggio con le coordinate del rettangolo di testo dell'etichetta che si desidera sovrapporre alla descrizione comando e restituisce le coordinate di un rettangolo della finestra di descrizione comando posizionato in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="b1085-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1085-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1085-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1085-153">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="b1085-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 