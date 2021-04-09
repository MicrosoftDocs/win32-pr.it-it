---
title: Gestire BCN_DROPDOWN notifiche da SplitButtons
description: In questo argomento viene descritta una possibile modalità di risposta alla \_ notifica a discesa BCN in una procedura di dialogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118554"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="4331d-103">Come gestire la notifica a \_ discesa BCN da un pulsante di menu combinato</span><span class="sxs-lookup"><span data-stu-id="4331d-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="4331d-104">In questo argomento viene descritta una possibile modalità di risposta alla notifica a [ \_ discesa BCN](bcn-dropdown.md) in una procedura di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4331d-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="4331d-105">L'applicazione C++ recupera le coordinate client del pulsante dall'intestazione della notifica e le converte in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4331d-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="4331d-106">Viene quindi creato un menu popup che viene visualizzato nella parte inferiore del pulsante.</span><span class="sxs-lookup"><span data-stu-id="4331d-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="4331d-107">Per semplificare l'esempio, i tasti di scelta rapida non sono implementati per il menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4331d-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="4331d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4331d-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="4331d-109">Technologies</span></span>

-   [<span data-ttu-id="4331d-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="4331d-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4331d-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4331d-111">Prerequisites</span></span>

-   <span data-ttu-id="4331d-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="4331d-112">C/C++</span></span>
-   <span data-ttu-id="4331d-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="4331d-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4331d-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4331d-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="4331d-115">Passaggio 1: attendere la notifica *a \_ discesa BCN* .</span><span class="sxs-lookup"><span data-stu-id="4331d-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="4331d-116">Passaggio 2: ottenere le coordinate dello schermo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="4331d-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="4331d-117">Usare la funzione [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) per convertire le coordinate della finestra del bordo inferiore sinistro del pulsante in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4331d-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="4331d-118">Passaggio 3: creare un menu e aggiungere elementi.</span><span class="sxs-lookup"><span data-stu-id="4331d-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="4331d-119">Utilizzare la funzione [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) per creare un menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="4331d-120">Utilizzare la funzione [**AppendMenu**](/windows/desktop/menurc/u) per aggiungere elementi al menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="4331d-121">IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 sono costanti definite dall'applicazione per i comandi di menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="4331d-122">Passaggio 4: visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="4331d-123">La funzione [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) Visualizza un menu di scelta rapida nella posizione specificata e tiene traccia della selezione degli elementi nel menu.</span><span class="sxs-lookup"><span data-stu-id="4331d-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="4331d-124">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="4331d-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="4331d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4331d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4331d-126">\_Codice di notifica a discesa BCN</span><span class="sxs-lookup"><span data-stu-id="4331d-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="4331d-127">Informazioni sui pulsanti</span><span class="sxs-lookup"><span data-stu-id="4331d-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="4331d-128">Riferimento al controllo Button</span><span class="sxs-lookup"><span data-stu-id="4331d-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4331d-129">Uso di pulsanti</span><span class="sxs-lookup"><span data-stu-id="4331d-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="4331d-130">Button</span><span class="sxs-lookup"><span data-stu-id="4331d-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 