---
description: In questa sezione viene illustrato come eseguire le attività seguenti associate alle routine della finestra.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Utilizzo delle routine della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884634"
---
# <a name="using-window-procedures"></a>Utilizzo delle routine della finestra

In questa sezione viene illustrato come eseguire le attività seguenti associate alle routine della finestra.

-   [Progettazione di una routine di finestra](#designing-a-window-procedure)
-   [Associazione di una routine di finestra a una classe di finestra](#associating-a-window-procedure-with-a-window-class)
-   [Sottoclasse di una finestra](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Progettazione di una routine di finestra

Nell'esempio seguente viene illustrata la struttura di una tipica routine della finestra. La routine della finestra utilizza l'argomento del messaggio in un'istruzione **Switch** con singoli messaggi gestiti da istruzioni **case** separate. Si noti che ogni case restituisce un valore specifico per ogni messaggio. Per i messaggi non elaborati, la routine della finestra chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .


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



Il messaggio [**WM \_ NCCREATE**](wm-nccreate.md) viene inviato subito dopo la creazione della finestra, ma se un'applicazione risponde a questo messaggio restituendo **false**, la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ha esito negativo. Il messaggio [**WM \_ create**](wm-create.md) viene inviato dopo che la finestra è già stata creata.

Il messaggio [**WM \_ Destroy**](wm-destroy.md) viene inviato quando la finestra sta per essere eliminata definitivamente. La funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) si occupa dell'eliminazione definitiva di tutte le finestre figlio della finestra distrutta. Il messaggio [**WM \_ NCDESTROY**](wm-ncdestroy.md) viene inviato immediatamente prima che venga distrutta una finestra.

Una routine della finestra deve almeno elaborare il messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) per disegnare se stesso. In genere, deve gestire anche i messaggi del mouse e della tastiera. Per determinare se la routine della finestra deve gestirli, consultare le descrizioni dei singoli messaggi.

L'applicazione può chiamare la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come parte dell'elaborazione di un messaggio. In tal caso, l'applicazione può modificare i parametri del messaggio prima di passare il messaggio a **DefWindowProc** oppure continuare con l'elaborazione predefinita dopo aver eseguito le proprie operazioni.

Una routine della finestra di dialogo riceve un messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) anziché un messaggio [**WM \_ create**](wm-create.md) e non passa messaggi non elaborati alla funzione [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) . In caso contrario, una routine della finestra di dialogo è esattamente identica a quella di una finestra.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Associazione di una routine di finestra a una classe di finestra

Si associa una routine di finestra a una classe della finestra quando si registra la classe. È necessario compilare una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con le informazioni sulla classe e il membro **lpfnWndProc** deve specificare l'indirizzo della routine della finestra. Per registrare la classe, passare l'indirizzo della struttura **WNDCLASS** alla funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . Una volta registrata la classe della finestra, la routine della finestra viene associata automaticamente a ogni nuova finestra creata con tale classe.

Nell'esempio seguente viene illustrato come associare la routine della finestra nell'esempio precedente a una classe di finestra.


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



## <a name="subclassing-a-window"></a>Sottoclasse di una finestra

Per sottoporre a una sottoclasse un'istanza di una finestra, chiamare la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e specificare l'handle della finestra per sottoporre a sottoclasse il \_ flag GWL WndProc e un puntatore alla routine della sottoclasse. **SetWindowLong** restituisce un puntatore alla routine della finestra originale; utilizzare questo puntatore per passare i messaggi alla routine originale. La routine della finestra di sottoclasse deve utilizzare la funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) per chiamare la routine della finestra originale.

> [!Note]  
> Per scrivere codice compatibile con le versioni di Windows a 32 bit e a 64 bit, usare la funzione [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .

 

Nell'esempio seguente viene illustrato come sottoporre a una sottoclasse un'istanza di un controllo di modifica in una finestra di dialogo. La procedura della finestra delle sottoclassi consente al controllo di modifica di ricevere tutti gli input da tastiera, inclusi i tasti INVIO e TABULAzione, ogni volta che il controllo ha lo stato attivo per l'input.


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



 

 
