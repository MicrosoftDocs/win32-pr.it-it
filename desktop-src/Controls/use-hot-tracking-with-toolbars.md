---
title: Come usare Hot-Tracking con le barre degli strumenti
description: Quando un puntatore del mouse viene posizionato su un elemento, l'elemento diventa attivo. Se è abilitata la funzionalità di rilevamento a caldo, l'elemento critico viene evidenziato. Per impostazione predefinita, una barra degli strumenti creata con lo \_ stile TBSTYLE flat o un oggetto che utilizza stili visivi supporta il rilevamento a caldo.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104046462"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="6de4f-105">Come usare Hot-Tracking con le barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="6de4f-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="6de4f-106">Quando un puntatore del mouse viene posizionato su un elemento, l'elemento diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="6de4f-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="6de4f-107">Se è abilitata la funzionalità di rilevamento a caldo, l'elemento critico viene evidenziato.</span><span class="sxs-lookup"><span data-stu-id="6de4f-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="6de4f-108">Per impostazione predefinita, una barra degli strumenti creata con lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o un oggetto che utilizza [stili visivi](themes-overview.md)supporta il rilevamento a caldo.</span><span class="sxs-lookup"><span data-stu-id="6de4f-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="6de4f-109">Per il rilevamento a caldo è necessario creare elenchi di immagini; non è quindi possibile usare il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) o la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) per creare la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="6de4f-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="6de4f-110">Quando il mouse viene spostato su un pulsante della barra degli strumenti, il pulsante viene indicato per evidenziarlo.</span><span class="sxs-lookup"><span data-stu-id="6de4f-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="6de4f-111">Nell'illustrazione seguente viene mostrata una barra degli strumenti con rilevamento a caldo abilitato; il puntatore del mouse è stato spostato sul pulsante Salva quando è stata eseguita la cattura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6de4f-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![Screenshot di una finestra di dialogo con una barra degli strumenti di tre elementi; l'icona selezionata è delineata](images/tb-withstyles.png)

<span data-ttu-id="6de4f-113">Se si vuole modificare la bitmap di un pulsante della barra degli strumenti quando lo stato del controllo cambia, archiviare le diverse immagini negli [elenchi di immagini](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="6de4f-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="6de4f-114">Alcune applicazioni, ad esempio, dispongono di pulsanti della barra degli strumenti neri e bianchi che diventano colorate quando vengono selezionate.</span><span class="sxs-lookup"><span data-stu-id="6de4f-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="6de4f-115">Le due diverse immagini vengono archiviate in elenchi di immagini.</span><span class="sxs-lookup"><span data-stu-id="6de4f-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="6de4f-116">Le barre degli strumenti supportano l'utilizzo di un massimo di tre elenchi di immagini.</span><span class="sxs-lookup"><span data-stu-id="6de4f-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="6de4f-117">In genere, un'applicazione dispone di un elenco di immagini predefinito, disabilitato e con rilevamento attivo.</span><span class="sxs-lookup"><span data-stu-id="6de4f-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="6de4f-118">Per impostare e recuperare elenchi di immagini per i pulsanti della barra degli strumenti caldi, usare i messaggi [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) e [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="6de4f-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6de4f-119">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="6de4f-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6de4f-120">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="6de4f-120">Technologies</span></span>

-   [<span data-ttu-id="6de4f-121">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="6de4f-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6de4f-122">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="6de4f-122">Prerequisites</span></span>

-   <span data-ttu-id="6de4f-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="6de4f-123">C/C++</span></span>
-   <span data-ttu-id="6de4f-124">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="6de4f-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6de4f-125">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="6de4f-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="6de4f-126">Usare Hot-Tracking con una barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="6de4f-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="6de4f-127">Nell'esempio di codice seguente viene creato, compilato e assegnato un elenco di immagini per i pulsanti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="6de4f-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="6de4f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6de4f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de4f-129">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="6de4f-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="6de4f-130">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="6de4f-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




