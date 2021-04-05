---
description: Negli esempi di questa sezione viene descritto come eseguire le attività associate all'utilizzo di Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Utilizzo di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884633"
---
# <a name="using-windows"></a>Utilizzo di Windows

Negli esempi di questa sezione viene descritto come eseguire le attività seguenti:

-   [Creazione di una finestra principale](#creating-a-main-window)
-   [Creazione, enumerazione e ridimensionamento di finestre figlio](#creating-enumerating-and-sizing-child-windows)
-   [Eliminazione di una finestra](#destroying-a-window)
-   [Uso di finestre sovrapposte](#using-layered-windows)

## <a name="creating-a-main-window"></a>Creazione di una finestra principale

La prima finestra creata da un'applicazione è in genere la finestra principale. Per creare la finestra principale, usare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra, il nome della finestra, gli stili della finestra, le dimensioni, la posizione, l'handle di menu, l'handle dell'istanza e i dati di creazione. Una finestra principale appartiene a una classe di finestra definita dall'applicazione, quindi è necessario registrare la classe della finestra e fornire una routine della finestra per la classe prima di creare la finestra principale.

La maggior parte delle applicazioni usa in genere lo stile [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) per creare la finestra principale. Questo stile assegna alla finestra una barra del titolo, un menu finestra, un bordo di ridimensionamento e i pulsanti Riduci a icona e Ingrandisci. La funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) restituisce un handle che identifica in modo univoco la finestra.

Nell'esempio seguente viene creata una finestra principale che appartiene a una classe di finestra definita dall'applicazione. Il nome della finestra, la **finestra principale**, verrà visualizzato sulla barra del titolo della finestra. Combinando gli [**stili \_ WS VSCROLL**](window-styles.md) e **WS \_ HSCROLL** con lo stile **WS \_ OVERLAPPEDWINDOW** , l'applicazione crea una finestra principale con barre di scorrimento orizzontali e verticali oltre ai componenti forniti dallo stile **WS \_ OVERLAPPEDWINDOW** . Le quattro occorrenze della costante **\_ usedefault (CW** impostano le dimensioni e la posizione iniziali della finestra sui valori predefiniti definiti dal sistema. Specificando **null** anziché un handle di menu, nella finestra sarà definito il menu per la classe Window.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



Si noti che nell'esempio precedente viene chiamata la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) dopo la creazione della finestra principale. Questa operazione viene eseguita perché il sistema non visualizza automaticamente la finestra principale dopo la creazione. Passando il flag **SW \_ SHOWDEFAULT** a **ShowWindow**, l'applicazione consente al programma che ha avviato l'applicazione di impostare lo stato di visualizzazione iniziale della finestra principale. La funzione [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) invia alla finestra il primo messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) .

## <a name="creating-enumerating-and-sizing-child-windows"></a>Creazione, enumerazione e ridimensionamento di finestre figlio

È possibile dividere l'area client di una finestra in aree funzionali diverse utilizzando le finestre figlio. La creazione di una finestra figlio è simile alla creazione di una finestra principale: si usa la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Per creare una finestra di una classe di finestra definita dall'applicazione, è necessario registrare la classe della finestra e fornire una routine della finestra prima di creare la finestra figlio. È necessario assegnare alla finestra figlio lo stile [**WS \_ child**](window-styles.md) e specificare una finestra padre per la finestra figlio al momento della creazione.

Nell'esempio seguente l'area client della finestra principale di un'applicazione viene divisa in tre aree funzionali creando tre finestre figlio di uguale dimensione. Ogni finestra figlio ha la stessa altezza dell'area client della finestra principale, ma ogni finestra è la cui larghezza è pari a un terzo. La finestra principale crea le finestre figlio in risposta al messaggio [**WM \_ create**](wm-create.md) , che la finestra principale riceve durante il processo di creazione di una finestra. Poiché ogni finestra figlio ha lo stile del [**\_ bordo WS**](window-styles.md) , ognuno ha un bordo sottile. Inoltre, poiché non è specificato lo stile di visualizzazione **WS \_** , ogni finestra figlio viene inizialmente nascosta. Si noti inoltre che a ogni finestra figlio viene assegnato un identificatore della finestra figlio.

La finestra principale ridimensiona e posiziona le finestre figlio in risposta al messaggio [**di \_ dimensioni WM**](wm-size.md) , che la finestra principale riceve quando cambiano le dimensioni. In risposta a **\_ dimensioni WM**, la finestra principale recupera le dimensioni dell'area client usando la funzione [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) e quindi passa le dimensioni alla funzione [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) . **EnumChildWindows** passa l'handle a ogni finestra figlio, a sua volta, alla funzione di callback [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definita dall'applicazione. Questa funzione ridimensiona e posiziona ogni finestra figlio chiamando la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) . le dimensioni e la posizione sono basate sulle dimensioni dell'area client della finestra principale e sull'identificatore della finestra figlio. Successivamente, **EnumChildProc** chiama la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) per rendere visibile la finestra.


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a>Eliminazione di una finestra

Per eliminare una finestra, è possibile usare la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . In genere, un'applicazione invia il messaggio di [**\_ chiusura WM**](wm-close.md) prima di eliminare una finestra, offrendo alla finestra la possibilità di chiedere conferma all'utente prima che la finestra venga distrutta. Una finestra che include un menu finestra riceve automaticamente il messaggio di **\_ chiusura WM** quando l'utente fa clic su **Chiudi** dal menu finestra. Se l'utente conferma che la finestra deve essere distrutta, l'applicazione chiama **DestroyWindow**. Il sistema invia il messaggio [**WM \_ Destroy**](wm-destroy.md) alla finestra dopo averlo rimosso dalla schermata. In risposta a **WM \_ Destroy**, la finestra Salva i dati e libera tutte le risorse allocate. Una finestra principale conclude l'elaborazione di **WM \_ Destroy** chiamando la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) per uscire dall'applicazione.

Nell'esempio seguente viene illustrato come richiedere la conferma dell'utente prima di eliminare una finestra. In risposta a [**WM \_ Close**](wm-close.md), nell'esempio viene visualizzata una finestra di dialogo che contiene i pulsanti **Sì**, **No** e **Annulla** . Se l'utente fa clic su **Sì**, viene chiamato [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . in caso contrario, la finestra non viene distrutta. Poiché la finestra distrutta è una finestra principale, l'esempio chiama [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in risposta a [**WM \_ Destroy**](wm-destroy.md).


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a>Uso di finestre sovrapposte

Per fare in modo che una finestra di dialogo venga visualizzata come finestra traslucida, creare innanzitutto la finestra di dialogo come di consueto. Quindi, su [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), impostare il bit a più livelli dello stile esteso della finestra e chiamare [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) con il valore alfa desiderato. Il codice potrebbe essere simile al seguente:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Si noti che il terzo parametro di [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) è un valore compreso tra 0 e 255, con 0 rendendo la finestra completamente trasparente e 255 rendendola completamente opaca. Questo parametro simula la [**BlendFunction**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) più versatile della funzione [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .

Per rendere questa finestra completamente opaca, rimuovere il bit **WS \_ ex \_ sovrapposto** chiamando [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e quindi chiedere di ridisegnare la finestra. La rimozione del bit si desidera per informare il sistema che può liberare memoria associata a livelli e reindirizzamento. Il codice potrebbe essere simile al seguente:


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



Per utilizzare le finestre figlio sovrapposte, l'applicazione deve dichiarare se stessa Windows 8 nel manifesto.

 

 
