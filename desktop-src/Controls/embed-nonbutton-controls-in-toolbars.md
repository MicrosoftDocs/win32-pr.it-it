---
title: Come incorporare controlli non Button nelle barre degli strumenti
description: Le barre degli strumenti supportano solo i pulsanti; Pertanto, se l'applicazione richiede un tipo di controllo diverso, è necessario creare una finestra figlio. Nella figura seguente è illustrata una barra degli strumenti con un controllo di modifica incorporato.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872219"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="d1845-104">Come incorporare controlli non Button nelle barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="d1845-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="d1845-105">Le barre degli strumenti supportano solo i pulsanti; Pertanto, se l'applicazione richiede un tipo di controllo diverso, è necessario creare una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="d1845-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="d1845-106">Nella figura seguente è illustrata una barra degli strumenti con un controllo di modifica incorporato.</span><span class="sxs-lookup"><span data-stu-id="d1845-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![Screenshot di una finestra di dialogo con un controllo di modifica nella barra degli strumenti, che precede tre icone della barra degli strumenti](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="d1845-108">Si consiglia di usare i [controlli Rebar](rebar-controls.md) anziché posizionare i controlli nelle barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="d1845-109">Qualsiasi tipo di finestra può essere posizionata su una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="d1845-110">Il codice di esempio seguente aggiunge un controllo di modifica come figlio della finestra di controllo della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="d1845-111">Poiché la barra degli strumenti è stata creata e quindi il controllo di modifica è stato aggiunto, è necessario fornire spazio per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="d1845-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="d1845-112">Un modo per eseguire questa operazione consiste nell'aggiungere un separatore come segnaposto nella barra degli strumenti, impostando la larghezza del separatore sul numero di pixel che si desidera riservare.</span><span class="sxs-lookup"><span data-stu-id="d1845-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d1845-113">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="d1845-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d1845-114">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="d1845-114">Technologies</span></span>

-   [<span data-ttu-id="d1845-115">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="d1845-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d1845-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="d1845-116">Prerequisites</span></span>

-   <span data-ttu-id="d1845-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="d1845-117">C/C++</span></span>
-   <span data-ttu-id="d1845-118">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="d1845-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d1845-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="d1845-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="d1845-120">Incorporare un controllo non Button in una barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="d1845-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="d1845-121">Il frammento di codice seguente crea la barra degli strumenti nella figura precedente.</span><span class="sxs-lookup"><span data-stu-id="d1845-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="d1845-122">In questo esempio vengono hardcoded i codici delle dimensioni della finestra figlio; Tuttavia, per creare un'applicazione più affidabile, determinare la dimensione della barra degli strumenti e fare in modo che la finestra di controllo di modifica si adatti.</span><span class="sxs-lookup"><span data-stu-id="d1845-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="d1845-123">È possibile che le notifiche dei controlli di modifica passino a un'altra finestra, ad esempio l'elemento padre della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="d1845-124">A tale scopo, creare il controllo di modifica come figlio della finestra padre della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="d1845-125">Modificare quindi l'elemento padre del controllo di modifica sulla barra degli strumenti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d1845-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="d1845-126">Le notifiche vengono inviate all'elemento padre originale.</span><span class="sxs-lookup"><span data-stu-id="d1845-126">Notifications go to the original parent.</span></span> <span data-ttu-id="d1845-127">Pertanto, i messaggi di controllo di modifica passano all'elemento padre della barra degli strumenti anche se la finestra di modifica risiede nella finestra della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d1845-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1845-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1845-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1845-129">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="d1845-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="d1845-130">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d1845-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




