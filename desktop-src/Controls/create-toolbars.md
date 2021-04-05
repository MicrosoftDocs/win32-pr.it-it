---
title: Come creare barre degli strumenti
description: Per creare una barra degli strumenti, usare la funzione CreateWindowEx, specificando la classe della finestra TOOLBARCLASSNAME.
ms.assetid: 5D060291-6ACF-478C-97EC-CD8BD55D1FFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69cd40338eaebc0d9de852519dce34dc9bc8aa4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730415"
---
# <a name="how-to-create-toolbars"></a><span data-ttu-id="6b24e-103">Come creare barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="6b24e-103">How to Create Toolbars</span></span>

<span data-ttu-id="6b24e-104">Per creare una barra degli strumenti, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra [**TOOLBARCLASSNAME**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="6b24e-104">To create a toolbar, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**TOOLBARCLASSNAME**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="6b24e-105">La barra degli strumenti risultante inizialmente non contiene pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b24e-105">The resulting toolbar initially contains no buttons.</span></span> <span data-ttu-id="6b24e-106">Aggiungere i pulsanti alla barra degli strumenti usando il messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="6b24e-106">Add buttons to the toolbar by using the [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) message.</span></span> <span data-ttu-id="6b24e-107">È necessario inviare il messaggio di [**\_ ridimensionamento automatico TB**](tb-autosize.md) dopo che tutti gli elementi e le stringhe sono stati inseriti nel controllo per fare in modo che la barra degli strumenti ricalcoli le dimensioni in base al relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="6b24e-107">You must send the [**TB\_AUTOSIZE**](tb-autosize.md) message after all the items and strings have been inserted into the control, to cause the toolbar to recalculate its size based on its content.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6b24e-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="6b24e-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6b24e-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="6b24e-109">Technologies</span></span>

-   [<span data-ttu-id="6b24e-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="6b24e-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6b24e-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="6b24e-111">Prerequisites</span></span>

-   <span data-ttu-id="6b24e-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="6b24e-112">C/C++</span></span>
-   <span data-ttu-id="6b24e-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="6b24e-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6b24e-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="6b24e-114">Instructions</span></span>

### <a name="create-a-toolbar"></a><span data-ttu-id="6b24e-115">Creare una barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="6b24e-115">Create a Toolbar</span></span>

<span data-ttu-id="6b24e-116">Il codice di esempio seguente crea la barra degli strumenti mostrata nell'illustrazione usando le icone di sistema standard.</span><span class="sxs-lookup"><span data-stu-id="6b24e-116">The following example code creates the toolbar shown in the illustration, using standard system icons.</span></span> <span data-ttu-id="6b24e-117">Il pulsante **Salva** viene inizialmente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6b24e-117">The **Save** button is initially disabled.</span></span>

![screenshot che mostra una finestra di dialogo con tre elementi della barra degli strumenti disposti orizzontalmente, ognuno dei quali ha un'icona e un'etichetta di testo](images/tb-codesample1.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateSimpleToolbar(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0, 
                                      hWndParent, NULL, g_hInst, NULL);
        
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize,   // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, (INT_PTR)L"Save"}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



<span data-ttu-id="6b24e-119">Nell'esempio seguente viene creata la stessa barra degli strumenti in modo analogo, ma in questo caso le stringhe vengono lette da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b24e-119">The following example creates the same toolbar in much the same way, but in this case, the strings are read from a resource.</span></span>


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarFromResource(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK, // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Load the text from a resource.
    
    // In the string table, the text for all buttons is a single entry that 
    // appears as "~New~Open~Save~~". The separator character is arbitrary, 
    // but it must appear as the first character of the string. The message 
    // returns the index of the first item, and the items are numbered 
    // consecutively.
    
    int iNew = SendMessage(hWndToolbar, TB_ADDSTRING, 
                           (WPARAM)g_hInst, (LPARAM)IDS_NEW); 
 
    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew + 1},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, iNew + 2}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



## <a name="related-topics"></a><span data-ttu-id="6b24e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b24e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b24e-121">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="6b24e-121">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="6b24e-122">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="6b24e-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 