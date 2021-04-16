---
title: Come creare una casella combinata semplice
description: In questo argomento viene descritto come creare, aggiungere e recuperare elementi da una semplice casella combinata.
ms.assetid: E432AEC0-6C06-40C7-BBFE-B66C21DB8ACA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4175d435ac78795e7020fd84099d512cc65be20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474374"
---
# <a name="how-to-create-a-simple-combo-box"></a><span data-ttu-id="4f8b6-103">Come creare una casella combinata semplice</span><span class="sxs-lookup"><span data-stu-id="4f8b6-103">How to Create a Simple Combo Box</span></span>

<span data-ttu-id="4f8b6-104">In questo argomento viene descritto come creare, aggiungere e recuperare elementi da una semplice casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-104">This topic describes how to create, add items to, and retrieve items from a simple combo box.</span></span> <span data-ttu-id="4f8b6-105">In particolare, gli esempi di codice associati dimostrano come eseguire le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f8b6-105">Specifically, the accompanying code examples demonstrate how to perform the following functions:</span></span>

-   <span data-ttu-id="4f8b6-106">Crea dinamicamente una casella combinata semplice in una finestra padre.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-106">Dynamically create a simple combo box in a parent window.</span></span>
-   <span data-ttu-id="4f8b6-107">Aggiungere un elenco di elementi alla casella combinata e visualizzare un elemento iniziale nel campo di selezione della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-107">Add a list of items to the combo box and display an initial item in the selection field of the combo box.</span></span>
-   <span data-ttu-id="4f8b6-108">Rileva quando l'utente ha selezionato un elemento dalla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-108">Detect when the user has selected an item from the combo box.</span></span>
-   <span data-ttu-id="4f8b6-109">Recupera l'elemento selezionato dalla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-109">Retrieve the selected item from the combo box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4f8b6-110">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="4f8b6-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4f8b6-111">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="4f8b6-111">Technologies</span></span>

-   [<span data-ttu-id="4f8b6-112">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="4f8b6-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4f8b6-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4f8b6-113">Prerequisites</span></span>

-   <span data-ttu-id="4f8b6-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="4f8b6-114">C/C++</span></span>
-   <span data-ttu-id="4f8b6-115">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="4f8b6-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4f8b6-116">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4f8b6-116">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-combo-box"></a><span data-ttu-id="4f8b6-117">Passaggio 1: creare un'istanza della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-117">Step 1: Create an instance of the combo box.</span></span>

<span data-ttu-id="4f8b6-118">L'applicazione di esempio chiama la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) per creare una finestra figlio della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-118">The example application calls the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a child window of the application window.</span></span> <span data-ttu-id="4f8b6-119">Lo stile della finestra [**\_ ComboBox WC**](common-control-window-classes.md) specifica che si tratta di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-119">The [**WC\_COMBOBOX**](common-control-window-classes.md) window style specifies that it is a combo box.</span></span>


```C++
// Create the Combobox
//
// Uses the CreateWindow function to create a child window of 
// the application window. The WC_COMBOBOX window style specifies  
// that it is a combobox.

 int xpos = 100;            // Horizontal position of the window.
 int ypos = 100;            // Vertical position of the window.
 int nwidth = 200;          // Width of the window
 int nheight = 200;         // Height of the window
 HWND hwndParent =  m_hwnd; // Handle to the parent window

 HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
     CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
     xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
     NULL);

```



### <a name="step-2-load-the-combo-box-with-the-item-list"></a><span data-ttu-id="4f8b6-120">Passaggio 2: caricare la casella combinata con l'elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-120">Step 2: Load the combo box with the item list.</span></span>

<span data-ttu-id="4f8b6-121">L'applicazione invia un messaggio [**CB \_ ADDSTRING**](cb-addstring.md) per ogni elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-121">The application sends a [**CB\_ADDSTRING**](cb-addstring.md) message for each item in the list.</span></span> <span data-ttu-id="4f8b6-122">Dopo il caricamento dell'elenco, l'applicazione invia il messaggio di errore [**CB \_**](cb-setcursel.md) per visualizzare un elemento iniziale nel campo di selezione della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-122">After the list is loaded, the application sends the [**CB\_SETCURSEL**](cb-setcursel.md) message to display an initial item in the combo box selection field.</span></span>


```C++
// load the combobox with item list.  
// Send a CB_ADDSTRING message to load each item

TCHAR Planets[9][10] =  
{
    TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
    TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
    TEXT("Pluto??") 
};
       
TCHAR A[16]; 
int  k = 0; 

memset(&A,0,sizeof(A));       
for (k = 0; k <= 8; k += 1)
{
    wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

    // Add string to combobox.
    SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
}
  
// Send the CB_SETCURSEL message to display an initial item 
//  in the selection field  
SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);
```



### <a name="step-3-detect-when-the-user-selects-an-item-and-retrieve-it-from-the-combo-box"></a><span data-ttu-id="4f8b6-123">Passaggio 3: rilevare quando l'utente seleziona un elemento e lo recupera dalla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-123">Step 3: Detect when the user selects an item and retrieve it from the combo box.</span></span>

<span data-ttu-id="4f8b6-124">Quando l'utente effettua una selezione dall'elenco, la casella combinata invia una notifica [ \_ selChange CBN](cbn-selchange.md) alla finestra padre tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="4f8b6-124">When the user makes a selection from the list, the combo box sends a [CBN\_SELCHANGE](cbn-selchange.md) notification to the parent window via a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="4f8b6-125">L'applicazione recupera il punto di controllo per la casella combinata dal campo *lParam* del messaggio di notifica e invia un messaggio di richiesta [**\_ GetCurSel CB**](cb-getcursel.md) alla casella combinata per recuperare l'indice dell'elemento di elenco selezionato.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-125">The application retrieves the handle to the combo box from the *lParam* field of the notification message and sends a [**CB\_GETCURSEL**](cb-getcursel.md) message to the combo box to retrieve the index of the selected list item.</span></span> <span data-ttu-id="4f8b6-126">Dopo aver ottenuto l'indice dell'elemento, l'applicazione invia un messaggio [**CB \_ GETLBTEXT**](cb-getlbtext.md) per ottenere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-126">After obtaining the item index, the application sends a [**CB\_GETLBTEXT**](cb-getlbtext.md) message to get the item.</span></span> <span data-ttu-id="4f8b6-127">Viene quindi visualizzato l'elemento in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-127">It then displays the item in a message box.</span></span>

> [!Note]  
> <span data-ttu-id="4f8b6-128">La [notifica \_ selChange di CBN](cbn-selchange.md) viene inviata ed elaborata prima che l'elemento venga inserito nel campo di selezione della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-128">The [CBN\_SELCHANGE](cbn-selchange.md) notification is sent and processed before the item is placed in the combo box selection field.</span></span> <span data-ttu-id="4f8b6-129">Come risultato, in questo esempio l'elemento selezionato non verrà visualizzato nel campo di selezione fino alla chiusura della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4f8b6-129">As result, in this example, the selected item won't appear in selection field until after the message box is closed.</span></span>

 


```C++
switch (message)
{   
    case WM_COMMAND:

        if(HIWORD(wParam) == CBN_SELCHANGE)
        // If the user makes a selection from the list:
        //   Send CB_GETCURSEL message to get the index of the selected list item.
        //   Send CB_GETLBTEXT message to get the item.
        //   Display the item in a messagebox.
        { 
            int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                (WPARAM) 0, (LPARAM) 0);
                TCHAR  ListItem[256];
                (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                (WPARAM) ItemIndex, (LPARAM) ListItem);
            MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
        }
        
        wasHandled = true;
    result = 0;
    break;
```



## <a name="complete-example"></a><span data-ttu-id="4f8b6-130">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="4f8b6-130">Complete example</span></span>


```C++
// Windows Header Files:
#include <windows.h>
#include <CommCtrl.h>

// C RunTime Header Files
#include <math.h>

#include <objbase.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif


#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT CreateResources();
    void DiscardResources();

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;

 };
```


```C++
#include "SimpleComboBox.h"

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE     /* hInstance */,
    HINSTANCE     /* hPrevInstance */,
    LPSTR     /* lpCmdLine */,
    int     /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()        
{
    // TODO: Release app resource here.
}

/*******************************************************************
*                                                                  *
*  Create the application window and the combobox.                 *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = TEXT("DemoApp");

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        TEXT("DemoApp"),
        TEXT("Simple Combo Box Example"),
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);
    }


    // Create the Combobox
    //
    // Uses the CreateWindow function to create a child window of 
    // the application window. The WC_COMBOBOX window style specifies  
    // that it is a combobox.

     int xpos = 100;            // Horizontal position of the window.
     int ypos = 100;            // Vertical position of the window.
     int nwidth = 200;          // Width of the window
     int nheight = 200;         // Height of the window
     HWND hwndParent =  m_hwnd; // Handle to the parent window

     HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
         CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
         xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
         NULL);


    
    // load the combobox with item list.  
    // Send a CB_ADDSTRING message to load each item

    TCHAR Planets[9][10] =  
    {
        TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
        TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
        TEXT("Pluto??") 
    };
           
    TCHAR A[16]; 
    int  k = 0; 

    memset(&A,0,sizeof(A));       
    for (k = 0; k <= 8; k += 1)
    {
        wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

        // Add string to combobox.
        SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
    }
      
    // Send the CB_SETCURSEL message to display an initial item 
    //  in the selection field  
    SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);

    return hr;
}


/******************************************************************
*                                                                 *
*  The main window's message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}


/******************************************************************
*                                                                 *
*  The window's message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {   
                case WM_COMMAND:

                    if(HIWORD(wParam) == CBN_SELCHANGE)
                    // If the user makes a selection from the list:
                    //   Send CB_GETCURSEL message to get the index of the selected list item.
                    //   Send CB_GETLBTEXT message to get the item.
                    //   Display the item in a messagebox.
                    { 
                        int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                            (WPARAM) 0, (LPARAM) 0);
                            TCHAR  ListItem[256];
                            (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                            (WPARAM) ItemIndex, (LPARAM) ListItem);
                        MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
                    }
                    
                    wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
```


## <a name="related-topics"></a><span data-ttu-id="4f8b6-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f8b6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f8b6-132">Informazioni sulle caselle combinate</span><span class="sxs-lookup"><span data-stu-id="4f8b6-132">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="4f8b6-133">Riferimento al controllo ComboBox</span><span class="sxs-lookup"><span data-stu-id="4f8b6-133">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4f8b6-134">Uso di caselle combinate</span><span class="sxs-lookup"><span data-stu-id="4f8b6-134">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="4f8b6-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="4f8b6-135">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 