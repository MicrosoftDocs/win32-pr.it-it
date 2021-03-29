---
description: È possibile utilizzare le funzioni linea e curva per tracciare un grafico a torta.
ms.assetid: 788d3bc2-1010-436c-a95f-6fe55daac88e
title: Disegno di un grafico a torta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d14928c3f90c3222c2a01d6a063d46f109ad7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130794"
---
# <a name="drawing-a-pie-chart"></a><span data-ttu-id="6992b-103">Disegno di un grafico a torta</span><span class="sxs-lookup"><span data-stu-id="6992b-103">Drawing a Pie Chart</span></span>

<span data-ttu-id="6992b-104">È possibile utilizzare le funzioni linea e curva per tracciare un grafico a torta.</span><span class="sxs-lookup"><span data-stu-id="6992b-104">You can use the line and curve functions to draw a pie chart.</span></span> <span data-ttu-id="6992b-105">La funzione primaria utilizzata per creare grafici a torta è la funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) , che richiede di specificare le coordinate del centro della torta, il raggio della torta, l'angolo iniziale e l'angolo di apertura.</span><span class="sxs-lookup"><span data-stu-id="6992b-105">The primary function used to draw pie charts is the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function, which requires you to supply the coordinates of the center of the pie, the radius of the pie, a start angle, and a sweep angle.</span></span> <span data-ttu-id="6992b-106">Lo screenshot seguente mostra una finestra di dialogo che l'utente può usare per immettere questi valori.</span><span class="sxs-lookup"><span data-stu-id="6992b-106">The following screen shot shows a dialog box that the user can use to enter these values.</span></span>

![cattura di schermata che mostra una finestra di dialogo per l'immissione di valori per il grafico a torta](images/pie.png)

<span data-ttu-id="6992b-108">I valori indicati sopra producono il grafico a torta seguente.</span><span class="sxs-lookup"><span data-stu-id="6992b-108">The values shown above produce the following pie chart.</span></span>

![screenshot del grafico a torta risultante](images/sampleapp.png)

<span data-ttu-id="6992b-110">Il modello della finestra di dialogo trovato nello script di risorsa dell'applicazione (. RC) specifica le caratteristiche della finestra di dialogo precedente (l'altezza, i controlli in esso contenuti e il relativo stile), come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6992b-110">The dialog box template found in the application's resource script (.RC) file specifies characteristics of the preceding dialog box (its height, the controls it contains, and its style), as follows.</span></span>


```C++
AngleArc DIALOG 6, 18, 160, 100 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Pie Chart" 
FONT 8, "MS Sans Serif" 
BEGIN 
    EDITTEXT   IDD_X, 18, 22, 25, 12, ES_AUTOHSCROLL 
    LTEXT      "X", 102, 4, 24, 9, 8 
    EDITTEXT   IDD_Y, 18, 39, 25, 12, ES_AUTOHSCROLL 
    LTEXT      "Y", 104, 5, 42, 12, 8 
    LTEXT      "Center", 105, 19, 11, 23, 8 
    EDITTEXT   IDD_RADIUS, 103, 9, 32, 12, ES_AUTOHSCROLL 
    EDITTEXT   IDD_STARTANGLE, 103, 31, 32, 12, ES_AUTOHSCROLL 
    EDITTEXT   IDD_SWEEPANGLE, 103, 53, 32, 12, ES_AUTOHSCROLL 
    LTEXT      "Radius", 109, 73, 11, 25, 8 
    LTEXT      "Start Angle", 110, 59, 33, 42, 8 
    LTEXT      "Sweep Angle", 111, 55, 55, 43, 8 
    PUSHBUTTON "OK", IDD_OK, 9, 82, 40, 14 
    PUSHBUTTON "Cancel", IDD_CANCEL, 110, 82, 40, 14 
END 
```



<span data-ttu-id="6992b-111">La routine della finestra di dialogo, disponibile nel file di origine dell'applicazione, recupera i dati (coordinate centrali, raggio arco e angoli iniziali e di apertura) attenendosi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="6992b-111">The dialog box procedure, found in the application's source file, retrieves data (center coordinates, arc radius, and start and sweep angles) by following these steps:</span></span>

1.  <span data-ttu-id="6992b-112">La funzione ClearBits definita dall'applicazione Inizializza la matrice che riceve l'input dell'utente su zero.</span><span class="sxs-lookup"><span data-stu-id="6992b-112">The application-defined ClearBits function initializes the array that receives the user-input to zero.</span></span>
2.  <span data-ttu-id="6992b-113">La funzione GetStrLngth definita dall'applicazione recupera la lunghezza della stringa immessa dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6992b-113">The application-defined GetStrLngth function retrieves the length of the string entered by the user.</span></span>
3.  <span data-ttu-id="6992b-114">La funzione RetrieveInput definita dall'applicazione recupera il valore immesso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6992b-114">The application-defined RetrieveInput function retrieves the value entered by the user.</span></span>

<span data-ttu-id="6992b-115">Nell'esempio di codice seguente viene illustrata la procedura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6992b-115">The following sample code shows the dialog box procedure.</span></span>


```C++
void ClearBits(LPTSTR, int); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveInput(LPTSTR, int); 

BOOL CALLBACK ArcDlgProc(HWND hdlg, UINT uMsg, WPARAM wParam, 
LPARAM lParam) 
{ 
    CHAR chInput[4];    // receives control-window input  
    int cch;            // array-size and count variable  
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
            return FALSE; 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
                // If the user pressed the OK button, retrieve the  
                // data that was entered in the various AngleArc  
                // controls.  
 
                case IDD_OK: 
                    // Retrieve the x-coordinate of the arc's center.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_X, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    nX = (int)RetrieveInput(chInput, cch); 
 
                    // Retrieve the y-coordinate of the arc's center.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_Y, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    nY = (int)RetrieveInput(chInput, cch); 
 
                    // Retrieve the radius of the arc.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_RADIUS, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    dwRadius = (DWORD) RetrieveInput(chInput, cch); 
 
                    // Retrieve the start angle.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_STARTANGLE, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    xStartAngle = (float) RetrieveInput(chInput, cch); 
 
                    // Retrieve the sweep angle.  
 
                    ClearBits(chInput, sizeof(chInput)); 
                    GetDlgItemText(hdlg, IDD_SWEEPANGLE, chInput, 
                        sizeof(chInput)); 
                    cch = GetStrLngth(chInput); 
                    xSweepAngle = (float) RetrieveInput(chInput, cch); 
 
                    EndDialog(hdlg, FALSE); 
                    return TRUE; 
 
                // If user presses the CANCEL button, close the  
                // dialog box.  
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, FALSE); 
                    return TRUE; 
            } // end switch (wParam)  
 
            break; 
 
        default: 
            return FALSE; 
    } // end switch (message)  
 
    UNREFERENCED_PARAMETER(lParam); 
} 
 
 
void ClearBits(LPTSTR cArray, int iLength) 
{ 
    int i; 
 
    for (i = 0; i < iLength; i++) 
        cArray[i] = 0; 
} 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
        return i - 1; 
} 
 
DWORD RetrieveInput(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double) (iLength - 1); 
 
    // Convert ASCII input to a floating-point value.  
 
    for (i = 0; i < iLength; i++) 
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD) dVal; 
} 
```



<span data-ttu-id="6992b-116">Per tracciare ogni sezione del grafico a torta, passare i valori immessi dall'utente alla funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .</span><span class="sxs-lookup"><span data-stu-id="6992b-116">To draw each section of the pie chart, pass the values entered by the user to the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span> <span data-ttu-id="6992b-117">Per riempire il grafico a torta utilizzando il pennello corrente, incorporare la chiamata a **AngleArc** in una parentesi del percorso.</span><span class="sxs-lookup"><span data-stu-id="6992b-117">To fill the pie chart using the current brush, embed the call to **AngleArc** in a path bracket.</span></span> <span data-ttu-id="6992b-118">Nell'esempio di codice seguente viene illustrata la parentesi del percorso definita e la chiamata a **AngleArc**.</span><span class="sxs-lookup"><span data-stu-id="6992b-118">The following code sample shows the defined path bracket and the call to **AngleArc**.</span></span>


```C++
    int nX; 
    int nY; 
    DWORD dwRadius; 
    float xStartAngle; 
    float xSweepAngle; 
 
    hdc = GetDC(hwnd); 
    BeginPath(hdc); 
    SelectObject(hdc, GetStockObject(GRAY_BRUSH)); 
    MoveToEx(hdc, nX, nY, (LPPOINT) NULL); 
    AngleArc(hdc, nX, nY, dwRadius, xStartAngle, xSweepAngle); 
    LineTo(hdc, nX, nY); 
    EndPath(hdc); 
    StrokeAndFillPath(hdc); 
    ReleaseDC(hwnd, hdc); 
```



 

 



