---
title: Gestione dello stato di un'applicazione
description: Una routine finestra è solo una funzione che viene richiamata per ogni messaggio, pertanto è intrinsecamente senza stato. È quindi necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068066"
---
# <a name="managing-application-state"></a>Gestione dello stato di un'applicazione

Una routine finestra è solo una funzione che viene richiamata per ogni messaggio, pertanto è intrinsecamente senza stato. È quindi necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.

L'approccio più semplice consiste semplicemente nell'inserire tutto nelle variabili globali. Questo approccio funziona abbastanza bene per i programmi di piccole dimensioni e molti esempi di SDK usano questo approccio. In un programma di grandi dimensioni, tuttavia, si genera una proliferazione di variabili globali. È anche possibile avere diverse finestre, ognuna con una propria routine della finestra. Tenere traccia di quale finestra deve accedere a quali variabili può generare confusione e determinare errori.

La [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) consente di passare qualsiasi struttura di dati a una finestra. Quando questa funzione viene chiamata, invia i due messaggi seguenti alla routine della finestra:

- [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)
- [**CREAZIONE \_ DI WM**](/windows/desktop/winmsg/wm-create)

Questi messaggi vengono inviati nell'ordine elencato. Non si tratta degli unici due messaggi inviati durante [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)ma è possibile ignorare gli altri per questa discussione.

Il [**messaggio WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) vengono inviati prima che la finestra diventi visibile. In questo modo è possibile inizializzare l'interfaccia utente, ad esempio per determinare il layout iniziale della finestra.

L'ultimo parametro di [**CreateWindowEx è**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) un puntatore di tipo **\* void* _. È possibile passare qualsiasi valore del puntatore desiderato in questo parametro. Quando la routine della finestra gestisce [il messaggio _ WM *\_ NCCREATE* *](/windows/desktop/winmsg/wm-nccreate) o [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) può estrarre questo valore dai dati del messaggio.

Verrà ora illustrato come usare questo parametro per passare i dati dell'applicazione alla finestra. Definire prima di tutto una classe o una struttura che contiene informazioni sullo stato.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Quando si chiama [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)passare un puntatore a questa struttura nel parametro **void \*** finale.

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    pState      // Additional application data
    );
```

Quando si ricevono i [**messaggi WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) il *parametro lParam* di ogni messaggio è un puntatore a [**una struttura CREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-createstructa) La **struttura CREATESTRUCT,** a sua volta, contiene il puntatore passato in [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

![Diagramma che mostra il layout della struttura createstruct](images/appstate01.png)

Ecco come estrarre il puntatore alla struttura dei dati. Per prima cosa, ottenere [**la struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) eseguendo il cast del *parametro lParam.*

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Il **membro lpCreateParams** della [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) è il puntatore void originale specificato in [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Ottenere un puntatore alla propria struttura di dati eseguendo il cast **di lpCreateParams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Chiamare quindi la [**funzione SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) e passare il puntatore alla struttura dei dati.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

Lo scopo di questa ultima chiamata di funzione è archiviare il *puntatore StateInfo* nei dati dell'istanza per la finestra. Dopo questa operazione, è sempre possibile ottenere il puntatore dalla finestra chiamando [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Ogni finestra ha i propri dati di istanza, quindi è possibile creare più finestre e assegnare a ogni finestra la propria istanza della struttura dei dati. Questo approccio è particolarmente utile se si definisce una classe di finestre e si creano più finestre di tale classe, ad esempio se si crea una classe di controllo personalizzata. È utile eseguire il wrapping della [**chiamata GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) in una funzione helper di piccole dimensioni.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

È ora possibile scrivere la routine della finestra come indicato di seguito.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a>Approccio Object-Oriented

È possibile estendere ulteriormente questo approccio. È già stata definita una struttura di dati per contenere informazioni sullo stato della finestra. È opportuno fornire questa struttura di dati con funzioni membro (metodi) che operano sui dati. Questo porta naturalmente a una progettazione in cui la struttura (o la classe) è responsabile di tutte le operazioni nella finestra. La routine della finestra diventerà quindi parte della classe .

In altre parole, si vuole passare da questo:

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

A questo scopo:

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

L'unico problema è come associare il `MyWindow::WindowProc` metodo . La [**funzione RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) prevede che la routine della finestra sia un puntatore a funzione. Non è possibile passare un puntatore a una funzione membro (non statica) in questo contesto. Tuttavia, è possibile passare un puntatore a una *funzione membro statica* e quindi delegare alla funzione membro. Ecco un modello di classe che illustra questo approccio:

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

La `BaseWindow` classe è una classe di base astratta, da cui derivano classi finestra specifiche. Ad esempio, di seguito è illustrata la dichiarazione di una classe semplice derivata da `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Per creare la finestra, chiamare `BaseWindow::Create` :

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

Il metodo pure-virtual `BaseWindow::HandleMessage` viene usato per implementare la routine della finestra. Ad esempio, l'implementazione seguente equivale alla routine della finestra visualizzata all'inizio del [modulo 1.](your-first-windows-program.md)

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

Si noti che l'handle di finestra viene archiviato in una variabile membro (*m \_ hwnd*), quindi non è necessario passarlo come parametro a `HandleMessage` .

Molti dei framework di programmazione Windows esistenti, ad esempio Microsoft Foundation Classes (MFC) e Active Template Library (ATL), usano approcci fondamentalmente simili a quelli illustrati qui. Naturalmente, un framework completamente generalizzato, ad esempio MFC, è più complesso di questo esempio relativamente semplicistico.

## <a name="next"></a>Prossima

[Modulo 2: Uso di COM nel programma Windows client](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Argomenti correlati

[Esempio di BaseWindow](basewindow-sample.md)