---
description: In questa sezione viene illustrato come eseguire le attività seguenti associate alle procedure della finestra.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Uso delle procedure della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05e5999b216ad8c51be4de6fdec80b5f58ff94956f8c1129d74c3f7075a90eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028299"
---
# <a name="using-window-procedures"></a>Uso delle procedure della finestra

In questa sezione viene illustrato come eseguire le attività seguenti associate alle procedure della finestra.

-   [Progettazione di una routine finestra](#designing-a-window-procedure)
-   [Associazione di una routine window a una classe Window](#associating-a-window-procedure-with-a-window-class)
-   [Sottoclassazione di una finestra](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Progettazione di una routine finestra

Nell'esempio seguente viene illustrata la struttura di una tipica routine della finestra. La routine window usa l'argomento message in **un'istruzione switch** con singoli messaggi gestiti da istruzioni **case** separate. Si noti che ogni case restituisce un valore specifico per ogni messaggio. Per i messaggi che non elabora, la routine della finestra chiama la [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



Il [**messaggio WM \_ NCCREATE**](wm-nccreate.md) viene inviato subito dopo la creazione della finestra, ma se un'applicazione risponde a questo messaggio restituisce **FALSE,** la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ha esito negativo. Il [**messaggio WM \_ CREATE**](wm-create.md) viene inviato dopo la creazione della finestra.

Il [**messaggio WM \_ DESTROY**](wm-destroy.md) viene inviato quando la finestra sta per essere distrutta. La [**funzione DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) consente di eliminare tutte le finestre figlio della finestra da eliminare. Il [**messaggio \_ WM NCDESTROY**](wm-ncdestroy.md) viene inviato subito prima dell'eliminazione di una finestra.

Come minimo, una routine della finestra deve elaborare il [**messaggio WM \_ PAINT**](../gdi/wm-paint.md) per disegnare se stesso. In genere, deve gestire anche i messaggi del mouse e della tastiera. Consultare le descrizioni dei singoli messaggi per determinare se la routine della finestra deve gestirli.

L'applicazione può chiamare [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come parte dell'elaborazione di un messaggio. In tal caso, l'applicazione può modificare i parametri del messaggio prima di passare il messaggio a **DefWindowProc** oppure può continuare con l'elaborazione predefinita dopo aver eseguito le proprie operazioni.

Una routine della finestra di dialogo riceve un messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) anziché un messaggio [**WM \_ CREATE**](wm-create.md) e non passa messaggi non elaborati alla [**funzione DefDlgProc.**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) In caso contrario, una routine della finestra di dialogo è esattamente uguale a una routine della finestra.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Associazione di una routine finestra a una classe Window

Quando si registra la classe, si associa una routine della finestra a una classe finestra. È necessario compilare una [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con informazioni sulla classe e il membro **lpfnWndProc** deve specificare l'indirizzo della routine della finestra. Per registrare la classe, passare l'indirizzo **della struttura WNDCLASS** alla [**funzione RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Dopo la registrazione della classe della finestra, la routine della finestra viene associata automaticamente a ogni nuova finestra creata con tale classe.

Nell'esempio seguente viene illustrato come associare la routine della finestra nell'esempio precedente a una classe window.


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a>Sottoclassazione di una finestra

Per sottoclassare un'istanza di una finestra, chiamare la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e specificare l'handle per la finestra per sottoclassare il flag WNDPROC GWL e un puntatore alla routine della \_ sottoclasse. **SetWindowLong restituisce** un puntatore alla routine della finestra originale. usare questo puntatore per passare messaggi alla procedura originale. La routine della finestra della sottoclasse deve usare la [**funzione CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) per chiamare la routine della finestra originale.

> [!Note]  
> Per scrivere codice compatibile con le versioni a 32 bit e a 64 bit di Windows, usare la [**funzione SetWindowLongPtr.**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

 

Nell'esempio seguente viene illustrato come sottoclassare un'istanza di un controllo di modifica in una finestra di dialogo. La routine della finestra della sottoclasse consente al controllo di modifica di ricevere tutti gli input da tastiera, inclusi i tasti INVIO e TAB, ogni volta che il controllo ha lo stato attivo per l'input.


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
