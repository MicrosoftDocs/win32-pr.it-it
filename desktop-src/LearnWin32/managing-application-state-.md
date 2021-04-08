---
title: Gestione dello stato di un'applicazione
description: Una routine di finestra è semplicemente una funzione che viene richiamata per ogni messaggio, quindi è intrinsecamente senza stato. Pertanto, è necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046719"
---
# <a name="managing-application-state"></a>Gestione dello stato di un'applicazione

Una routine di finestra è semplicemente una funzione che viene richiamata per ogni messaggio, quindi è intrinsecamente senza stato. Pertanto, è necessario un modo per tenere traccia dello stato dell'applicazione da una chiamata di funzione a quella successiva.

L'approccio più semplice consiste semplicemente nell'inserire tutti gli elementi delle variabili globali. Questo approccio funziona correttamente per i programmi di piccole dimensioni e molti degli esempi di SDK usano questo approccio. In un programma di grandi dimensioni, tuttavia, comporta una proliferazione di variabili globali. Inoltre, è possibile disporre di più finestre, ognuna con la propria routine della finestra. Tenere traccia della finestra che dovrebbe accedere alle variabili che risultano confuse e soggette a errori.

La funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) fornisce un modo per passare qualsiasi struttura di dati a una finestra. Quando questa funzione viene chiamata, invia i due messaggi seguenti alla routine della finestra:

- [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)
- [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)

Questi messaggi vengono inviati nell'ordine indicato. (Questi non sono gli unici due messaggi inviati durante [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), ma è possibile ignorare gli altri per questa discussione).

I messaggi [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ create**](/windows/desktop/winmsg/wm-create) vengono inviati prima che la finestra diventi visibile. Questo consente di inizializzare l'interfaccia utente, ad esempio per determinare il layout iniziale della finestra.

L'ultimo parametro di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) è un puntatore di tipo **void \***. È possibile passare qualsiasi valore del puntatore che si desidera in questo parametro. Quando la routine della finestra gestisce il messaggio [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) o [**WM \_ create**](/windows/desktop/winmsg/wm-create) , può estrarre questo valore dai dati del messaggio.

Viene ora illustrato come usare questo parametro per passare i dati dell'applicazione alla finestra. In primo luogo, definire una classe o una struttura che include informazioni sullo stato.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Quando si chiama [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), passare un puntatore a questa struttura nel parametro **void \*** finale.

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

Quando si ricevono i [**messaggi \_ WM NCCREATE**](/windows/desktop/winmsg/wm-nccreate) e [**WM \_ create**](/windows/desktop/winmsg/wm-create) , il parametro *lParam* di ogni messaggio è un puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . La struttura **struttura CREATESTRUCT** contiene a sua volta il puntatore passato in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

![diagramma che mostra il layout della struttura struttura CREATESTRUCT](images/appstate01.png)

Ecco come estrarre il puntatore nella struttura dei dati. Per prima cosa, ottenere la struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) eseguendo il cast del parametro *lParam* .

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Il membro **lpCreateParams** della struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) è il puntatore void originale specificato in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Ottenere un puntatore alla struttura dei dati personalizzata eseguendo il cast di **lpCreateParams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Chiamare quindi la funzione [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) e passare il puntatore alla struttura dei dati.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

Lo scopo di questa ultima chiamata di funzione consiste nell'archiviare il puntatore *stateInfo* nei dati dell'istanza per la finestra. Una volta eseguita questa operazione, è sempre possibile riportare il puntatore dalla finestra chiamando [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Ogni finestra ha i propri dati di istanza, pertanto è possibile creare più finestre e assegnare a ogni finestra una propria istanza della struttura dei dati. Questo approccio è particolarmente utile se si definisce una classe di finestre e si crea più di una finestra di tale classe, ad esempio se si crea una classe di controlli personalizzata. È consigliabile eseguire il wrapping della chiamata [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) in una piccola funzione helper.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

A questo punto è possibile scrivere la routine della finestra come indicato di seguito.

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

## <a name="an-object-oriented-approach"></a>Un approccio Object-Oriented

È possibile estendere ulteriormente questo approccio. È già stata definita una struttura di dati per contenere le informazioni sullo stato relative alla finestra. È sensato fornire questa struttura di dati con funzioni membro (metodi) che operano sui dati. Questo comporta naturalmente un progetto in cui la struttura (o la classe) è responsabile di tutte le operazioni nella finestra. La routine della finestra diventerebbe quindi parte della classe.

In altre parole, si desidera procedere nel modo seguente:

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

L'unico problema è come associare il `MyWindow::WindowProc` metodo. La funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) prevede che la routine della finestra sia un puntatore a funzione. Non è possibile passare un puntatore a una funzione membro (non statica) in questo contesto. È tuttavia possibile passare un puntatore a una funzione membro *statica* e quindi delegare la funzione membro. Ecco un modello di classe che mostra questo approccio:

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

La `BaseWindow` classe è una classe di base astratta dalla quale derivano le classi di finestra specifiche. Ecco, ad esempio, la dichiarazione di una classe semplice derivata da `BaseWindow` :

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

Il metodo virtuale puro `BaseWindow::HandleMessage` viene usato per implementare la routine della finestra. Ad esempio, l'implementazione seguente equivale alla procedura della finestra visualizzata all'inizio del [modulo 1](your-first-windows-program.md).

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

Si noti che l'handle della finestra viene archiviato in una variabile membro (*\_ HWND m*), pertanto non è necessario passarlo come parametro a `HandleMessage` .

Molti dei framework di programmazione Windows esistenti, ad esempio Microsoft Foundation Classes (MFC) e Active Template Library (ATL), usano approcci sostanzialmente simili a quelli illustrati di seguito. Naturalmente, un Framework completamente generalizzato, ad esempio MFC, è più complesso rispetto a questo esempio relativamente semplicistico.

## <a name="next"></a>Prossima

[Modulo 2: uso di COM nel programma Windows](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Argomenti correlati

[Esempio BaseWindow](basewindow-sample.md)