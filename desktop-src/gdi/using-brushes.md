---
description: È possibile utilizzare un pennello per disegnare l'interno di praticamente qualsiasi forma utilizzando una funzione GDI (Graphics Device Interface).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Uso di pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65ad4b14ba445642f224b0002eb1e7517c1008b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528819"
---
# <a name="using-brushes"></a><span data-ttu-id="61785-103">Uso di pennelli</span><span class="sxs-lookup"><span data-stu-id="61785-103">Using Brushes</span></span>

<span data-ttu-id="61785-104">È possibile utilizzare un pennello per disegnare l'interno di praticamente qualsiasi forma utilizzando una funzione GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="61785-104">You can use a brush to paint the interior of virtually any shape by using a graphics device interface (GDI) function.</span></span> <span data-ttu-id="61785-105">Sono inclusi gli interni di rettangoli, ellissi, poligoni e percorsi.</span><span class="sxs-lookup"><span data-stu-id="61785-105">This includes the interiors of rectangles, ellipses, polygons, and paths.</span></span> <span data-ttu-id="61785-106">A seconda dei requisiti dell'applicazione, è possibile usare un pennello a tinta unita di un colore specificato, un pennello azionario, un pennello di tratteggio o un pennello per motivi.</span><span class="sxs-lookup"><span data-stu-id="61785-106">Depending on the requirements of your application, you can use a solid brush of a specified color, a stock brush, a hatch brush, or a pattern brush.</span></span>

<span data-ttu-id="61785-107">Questa sezione contiene esempi di codice che illustrano la creazione di una finestra di dialogo personalizzata per il pennello.</span><span class="sxs-lookup"><span data-stu-id="61785-107">This section contains code samples that demonstrate the creation of a custom brush dialog box.</span></span> <span data-ttu-id="61785-108">La finestra di dialogo contiene una griglia che rappresenta la bitmap utilizzata dal sistema come pennello.</span><span class="sxs-lookup"><span data-stu-id="61785-108">The dialog box contains a grid that represents the bitmap the system uses as a brush.</span></span> <span data-ttu-id="61785-109">Un utente può usare questa griglia per creare una bitmap del pennello per i modelli e quindi visualizzare il modello personalizzato facendo clic sul pulsante del **modello di test** .</span><span class="sxs-lookup"><span data-stu-id="61785-109">A user can use this grid to create a pattern-brush bitmap and then view the custom pattern by clicking the **Test Pattern** button.</span></span>

<span data-ttu-id="61785-110">Nella figura seguente viene illustrato un modello creato tramite la finestra di dialogo **personalizzata del pennello** .</span><span class="sxs-lookup"><span data-stu-id="61785-110">The following illustration shows a pattern created by using the **Custom Brush** dialog box.</span></span>

![screenshot della finestra di dialogo del pennello personalizzato](images/custbrush.png)

<span data-ttu-id="61785-112">Per visualizzare una finestra di dialogo, è prima necessario creare un modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61785-112">To display a dialog box, you must first create a dialog box template.</span></span> <span data-ttu-id="61785-113">Il modello di finestra di dialogo seguente definisce la finestra di dialogo del **pennello personalizzato** .</span><span class="sxs-lookup"><span data-stu-id="61785-113">The following dialog box template defines the **Custom Brush** dialog box.</span></span>


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



<span data-ttu-id="61785-114">La finestra di dialogo del **pennello personalizzato** contiene cinque controlli: una finestra della griglia bitmap, una finestra di visualizzazione dei modelli e tre pulsanti di push, etichettato **test pattern**, **OK** e **Cancel**.</span><span class="sxs-lookup"><span data-stu-id="61785-114">The **Custom Brush** dialog box contains five controls: a bitmap-grid window, a pattern-viewing window, and three push buttons, labeled **Test Pattern**, **OK**, and **Cancel**.</span></span> <span data-ttu-id="61785-115">Il pulsante di push **pattern test** consente all'utente di visualizzare il modello.</span><span class="sxs-lookup"><span data-stu-id="61785-115">The **Test Pattern** push button enables the user to view the pattern.</span></span> <span data-ttu-id="61785-116">Il modello di finestra di dialogo Specifica le dimensioni complessive della finestra di dialogo, assegna un valore a ogni controllo, specifica la posizione di ogni controllo e così via.</span><span class="sxs-lookup"><span data-stu-id="61785-116">The dialog box template specifies the overall dimensions of the dialog box window, assigns a value to each control, specifies the location of each control, and so forth.</span></span> <span data-ttu-id="61785-117">Per ulteriori informazioni, vedere [finestre di dialogo](../dlgbox/dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="61785-117">For more information, see [Dialog Boxes](../dlgbox/dialog-boxes.md).</span></span>

<span data-ttu-id="61785-118">I valori di controllo nel modello di finestra di dialogo sono costanti definiti come indicato di seguito nel file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61785-118">The control values in the dialog box template are constants that have been defined as follows in the application's header file.</span></span>


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



<span data-ttu-id="61785-119">Dopo aver creato un modello di finestra di dialogo e averlo incluso nel file di definizione delle risorse dell'applicazione, è necessario scrivere una routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61785-119">After you create a dialog box template and include it in the application's resource-definition file, you must write a dialog procedure.</span></span> <span data-ttu-id="61785-120">Questa procedura consente di elaborare i messaggi inviati dal sistema alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="61785-120">This procedure processes messages that the system sends to the dialog box.</span></span> <span data-ttu-id="61785-121">Il seguente estratto del codice sorgente di un'applicazione mostra la procedura della finestra di dialogo per la finestra di dialogo del **pennello personalizzato** e le due funzioni definite dall'applicazione da essa chiamate.</span><span class="sxs-lookup"><span data-stu-id="61785-121">The following excerpt from an application's source code shows the dialog box procedure for the **Custom Brush** dialog box and the two application-defined functions it calls.</span></span>


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



<span data-ttu-id="61785-122">La procedura della finestra di dialogo per la finestra di dialogo **pennello personalizzato** elabora quattro messaggi, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="61785-122">The dialog box procedure for the **Custom Brush** dialog box processes four messages, as described in the following table.</span></span>



| <span data-ttu-id="61785-123">Message</span><span class="sxs-lookup"><span data-stu-id="61785-123">Message</span></span>                                          | <span data-ttu-id="61785-124">Azione</span><span class="sxs-lookup"><span data-stu-id="61785-124">Action</span></span>                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61785-125">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="61785-125">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)   | <span data-ttu-id="61785-126">Recupera un handle di finestra e le dimensioni per i controlli della finestra griglia e del pennello del pattern, calcola le dimensioni di una singola cella nel controllo della finestra della griglia e Inizializza una matrice di coordinate della cella della griglia.</span><span class="sxs-lookup"><span data-stu-id="61785-126">Retrieves a window handle and dimensions for the grid-window and pattern-brush controls, computes the dimensions of a single cell in the grid-window control, and initializes an array of grid-cell coordinates.</span></span>                                                                                           |
| [<span data-ttu-id="61785-127">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="61785-127">**WM\_PAINT**</span></span>](wm-paint.md)                    | <span data-ttu-id="61785-128">Disegna il motivo della griglia nel controllo della finestra della griglia.</span><span class="sxs-lookup"><span data-stu-id="61785-128">Draws the grid pattern in the grid-window control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="61785-129">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="61785-129">**WM\_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md) | <span data-ttu-id="61785-130">Determina se il cursore si trova all'interno del controllo della finestra della griglia quando l'utente preme il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="61785-130">Determines whether the cursor is within the grid-window control when the user presses the left mouse button.</span></span> <span data-ttu-id="61785-131">In tal caso, la routine della finestra di dialogo inverte la cella della griglia appropriata e registra lo stato della cella in una matrice di bit utilizzata per creare la bitmap per il pennello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="61785-131">If so, the dialog box procedure inverts the appropriate grid cell and records the state of that cell in an array of bits that is used to create the bitmap for the custom brush.</span></span>              |
| [<span data-ttu-id="61785-132">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="61785-132">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)         | <span data-ttu-id="61785-133">Elabora l'input per i tre controlli pulsante di comando.</span><span class="sxs-lookup"><span data-stu-id="61785-133">Processes input for the three push button controls.</span></span> <span data-ttu-id="61785-134">Se l'utente fa clic sul pulsante **test pattern** , la procedura della finestra di dialogo disegna il controllo pattern di test con il nuovo modello di pennello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="61785-134">If the user clicks the **Test Pattern** button, the dialog box procedure paints the Test Pattern control with the new custom brush pattern.</span></span> <span data-ttu-id="61785-135">Se l'utente fa clic sul pulsante **OK** o **Annulla** , la routine della finestra di dialogo esegue le azioni di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="61785-135">If the user clicks the **OK** or **Cancel** button, the dialog box procedure performs actions accordingly.</span></span> |



 

<span data-ttu-id="61785-136">Per ulteriori informazioni sui messaggi e sull'elaborazione dei messaggi, vedere [messaggi e code](../winmsg/messages-and-message-queues.md)di messaggi.</span><span class="sxs-lookup"><span data-stu-id="61785-136">For more information about messages and message processing, see [Messages and Message Queues](../winmsg/messages-and-message-queues.md).</span></span>

<span data-ttu-id="61785-137">Dopo aver scritto la routine della finestra di dialogo, includere la definizione di funzione per la procedura nel file di intestazione dell'applicazione e quindi chiamare la routine della finestra di dialogo nel punto appropriato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61785-137">After you write the dialog box procedure, include the function definition for the procedure in the application's header file and then call the dialog box procedure at the appropriate point in the application.</span></span>

<span data-ttu-id="61785-138">Il seguente estratto dal file di intestazione dell'applicazione mostra la definizione di funzione per la routine della finestra di dialogo e le due funzioni da essa chiamate.</span><span class="sxs-lookup"><span data-stu-id="61785-138">The following excerpt from the application's header file shows the function definition for the dialog box procedure and the two functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



<span data-ttu-id="61785-139">Infine, il codice seguente illustra come viene chiamata la routine della finestra di dialogo dal file del codice sorgente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61785-139">Finally, the following code shows how the dialog box procedure is called from the application's source-code file.</span></span>


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



<span data-ttu-id="61785-140">Questa chiamata viene in genere effettuata in risposta all'utente che sceglie un'opzione dal menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61785-140">This call is usually made in response to the user choosing an option from the application's menu.</span></span>

 

 
