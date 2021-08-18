---
description: È possibile usare un pennello per disegnare l'interno di praticamente qualsiasi forma usando una funzione GDI (Graphics Device Interface).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Uso di pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42e09dc5731ceba7961dfd66b296df531897f2915cff53ccdacf1b5b5740160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037499"
---
# <a name="using-brushes"></a>Uso di pennelli

È possibile usare un pennello per disegnare l'interno di praticamente qualsiasi forma usando una funzione GDI (Graphics Device Interface). Sono inclusi gli interni di rettangoli, ellissi, poligoni e tracciati. A seconda dei requisiti dell'applicazione, è possibile usare un pennello a tinta unita di un colore specificato, un pennello predefinito, un pennello tratteggiato o un pennello motivo.

Questa sezione contiene esempi di codice che illustrano la creazione di una finestra di dialogo pennello personalizzata. La finestra di dialogo contiene una griglia che rappresenta la bitmap utilizzata dal sistema come pennello. Un utente può usare questa griglia per creare una bitmap del pennello a pattern e quindi visualizzare il criterio personalizzato facendo clic sul **pulsante Test Pattern (Modello di** test).

La figura seguente mostra un modello creato usando la finestra **di dialogo Pennello** personalizzato.

![Screenshot della finestra di dialogo del pennello personalizzato](images/custbrush.png)

Per visualizzare una finestra di dialogo, è innanzitutto necessario creare un modello di finestra di dialogo. Il modello di finestra di dialogo seguente definisce la **finestra di dialogo Pennello** personalizzato.


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



La **finestra di dialogo** Pennello personalizzato contiene cinque controlli: una finestra griglia bitmap, una finestra di visualizzazione pattern e tre pulsanti di comando, con etichetta Test **Pattern**, **OK** e **Cancel.** Il **pulsante di push** Modello di test consente all'utente di visualizzare il modello. Il modello di finestra di dialogo specifica le dimensioni complessive della finestra di dialogo, assegna un valore a ogni controllo, specifica la posizione di ogni controllo e così via. Per altre informazioni, vedere [Finestre di dialogo.](../dlgbox/dialog-boxes.md)

I valori dei controlli nel modello della finestra di dialogo sono costanti definite come indicato di seguito nel file di intestazione dell'applicazione.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



Dopo aver creato un modello di finestra di dialogo e averlo incluso nel file di definizione delle risorse dell'applicazione, è necessario scrivere una routine della finestra di dialogo. Questa procedura elabora i messaggi inviati dal sistema alla finestra di dialogo. L'estratto seguente del codice sorgente di un'applicazione  mostra la procedura della finestra di dialogo per la finestra di dialogo Pennello personalizzato e le due funzioni definite dall'applicazione chiamate.


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



La procedura della finestra di dialogo **per la** finestra di dialogo Pennello personalizzato elabora quattro messaggi, come descritto nella tabella seguente.



| Message                                          | Azione                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)   | Recupera un handle di finestra e le dimensioni per i controlli griglia e pennello a linee, calcola le dimensioni di una singola cella nel controllo della finestra della griglia e inizializza una matrice di coordinate della cella della griglia.                                                                                           |
| [**WM \_ PAINT**](wm-paint.md)                    | Disegna il modello griglia nel controllo della finestra della griglia.                                                                                                                                                                                                                                                         |
| [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) | Determina se il cursore si trova all'interno del controllo della finestra della griglia quando l'utente preme il pulsante sinistro del mouse. In questo caso, la routine della finestra di dialogo inverte la cella della griglia appropriata e registra lo stato di tale cella in una matrice di bit utilizzata per creare la bitmap per il pennello personalizzato.              |
| [**COMANDO \_ WM**](../menurc/wm-command.md)         | Elabora l'input per i tre controlli pulsante di comando. Se l'utente fa clic sul **pulsante Modello di test,** la routine della finestra di dialogo disegna il controllo Test Pattern con il nuovo modello di pennello personalizzato. Se l'utente fa clic sul **pulsante OK** **o Annulla,** la procedura della finestra di dialogo esegue le azioni di conseguenza. |



 

Per altre informazioni sui messaggi e sull'elaborazione dei messaggi, [vedere Messaggi e code di messaggi.](../winmsg/messages-and-message-queues.md)

Dopo aver scritto la routine della finestra di dialogo, includere la definizione della funzione per la procedura nel file di intestazione dell'applicazione e quindi chiamare la routine della finestra di dialogo nel punto appropriato dell'applicazione.

L'estratto seguente del file di intestazione dell'applicazione mostra la definizione della funzione per la routine della finestra di dialogo e le due funzioni chiamate.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Infine, il codice seguente illustra come viene chiamata la routine della finestra di dialogo dal file di codice sorgente dell'applicazione.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Questa chiamata viene in genere effettuata in risposta alla scelta da parte dell'utente di un'opzione dal menu dell'applicazione.

 

 
