---
title: Come sottoclasse di una casella combinata
description: In questo argomento viene illustrato come eseguire la sottoclasse delle caselle combinate.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047461"
---
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="ddac0-103">Come sottoclasse di una casella combinata</span><span class="sxs-lookup"><span data-stu-id="ddac0-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="ddac0-104">In questo argomento viene illustrato come eseguire la sottoclasse delle caselle combinate.</span><span class="sxs-lookup"><span data-stu-id="ddac0-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="ddac0-105">L'applicazione di esempio C++ crea una finestra della barra degli strumenti che contiene due caselle combinate.</span><span class="sxs-lookup"><span data-stu-id="ddac0-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="ddac0-106">Eseguendo la sottoclasse dei controlli di modifica all'interno delle caselle combinate, la finestra della barra degli strumenti intercetta le chiavi, invio e ESC che altrimenti verrebbero ignorate.</span><span class="sxs-lookup"><span data-stu-id="ddac0-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ddac0-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="ddac0-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ddac0-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="ddac0-108">Technologies</span></span>

-   [<span data-ttu-id="ddac0-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="ddac0-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ddac0-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ddac0-110">Prerequisites</span></span>

-   <span data-ttu-id="ddac0-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ddac0-111">C/C++</span></span>
-   <span data-ttu-id="ddac0-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="ddac0-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ddac0-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ddac0-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="ddac0-114">Elaborare il \_ messaggio di creazione WM</span><span class="sxs-lookup"><span data-stu-id="ddac0-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="ddac0-115">L'applicazione elabora il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) per creare due controlli casella combinata come finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="ddac0-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



<span data-ttu-id="ddac0-116">L'applicazione quindi sottoclasse i controlli di modifica (campi di selezione) in ogni casella combinata, perché ricevono l'input di caratteri per la casella combinata semplice e a discesa.</span><span class="sxs-lookup"><span data-stu-id="ddac0-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="ddac0-117">Infine, chiama la funzione [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) per recuperare l'handle a ogni controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="ddac0-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="ddac0-118">Per sottoclassare i controlli di modifica, l'applicazione chiama la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , sostituendo il puntatore alla routine della finestra della classe con un puntatore alla funzione **SubClassProc** definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ddac0-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="ddac0-119">Il puntatore alla routine della finestra originale viene salvato nella variabile globale *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="ddac0-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="ddac0-120">**SubClassProc** intercetta i tasti TAB, invio e ESC e notifica la finestra della barra degli strumenti inviando messaggi definiti dall'applicazione (WM \_ Tab, WM \_ ESC e WM \_ Enter).</span><span class="sxs-lookup"><span data-stu-id="ddac0-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="ddac0-121">**SubClassProc** usa la funzione [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) per passare la maggior parte dei messaggi alla routine della finestra originale, *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="ddac0-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="ddac0-122">Elaborare il messaggio di SetFocus di WM \_</span><span class="sxs-lookup"><span data-stu-id="ddac0-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="ddac0-123">Quando la finestra della barra degli strumenti riceve lo stato attivo per l'input, imposta immediatamente lo stato attivo sulla prima casella combinata nella barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ddac0-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="ddac0-124">A tale scopo, nell'esempio viene chiamata la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) in risposta al messaggio [**di \_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="ddac0-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="ddac0-125">Elabora messaggi di Application-Defined</span><span class="sxs-lookup"><span data-stu-id="ddac0-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="ddac0-126">La funzione **SubClassProc** invia messaggi definiti dall'applicazione alla finestra della barra degli strumenti quando l'utente preme il tasto TAB, invio o ESC in una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="ddac0-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="ddac0-127">Il messaggio della **\_ scheda WM** viene inviato per il tasto TAB, il messaggio **WM \_ ESC** per il tasto ESC e il messaggio di **\_ immissione WM** per il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="ddac0-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="ddac0-128">L'esempio elabora il messaggio della **\_ scheda WM** impostando lo stato attivo sulla casella combinata successiva sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ddac0-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="ddac0-129">Elabora il messaggio **WM \_ ESC** impostando lo stato attivo sulla finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ddac0-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



<span data-ttu-id="ddac0-130">In risposta al messaggio **di \_ invio di WM** , l'esempio garantisce che la selezione corrente per la casella combinata sia valida, quindi imposta lo stato attivo sulla finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ddac0-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="ddac0-131">Se la casella combinata non contiene alcuna selezione corrente, nell'esempio viene utilizzato il messaggio [**CB \_ FindExactString**](cb-findstringexact.md) per cercare un elemento elenco corrispondente al contenuto del campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="ddac0-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="ddac0-132">Se è presente una corrispondenza, nell'esempio viene impostata la selezione corrente. in caso contrario, viene aggiunto un nuovo elemento elenco.</span><span class="sxs-lookup"><span data-stu-id="ddac0-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a><span data-ttu-id="ddac0-133">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="ddac0-133">Complete example</span></span>

<span data-ttu-id="ddac0-134">Di seguito sono illustrate le procedure della finestra per la barra degli strumenti e la procedura di sottoclasse per le due caselle combinate.</span><span class="sxs-lookup"><span data-stu-id="ddac0-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="ddac0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddac0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddac0-136">Informazioni sulle caselle combinate</span><span class="sxs-lookup"><span data-stu-id="ddac0-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="ddac0-137">Riferimento al controllo ComboBox</span><span class="sxs-lookup"><span data-stu-id="ddac0-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ddac0-138">Uso di caselle combinate</span><span class="sxs-lookup"><span data-stu-id="ddac0-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="ddac0-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="ddac0-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 