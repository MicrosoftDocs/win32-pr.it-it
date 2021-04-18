---
title: Uso di finestre di dialogo comuni
description: In questa sezione vengono descritte le attività che richiamano finestre di dialogo comuni.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Libreria finestra di dialogo comune, attività
- finestre di dialogo comuni, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/19/2020
ms.locfileid: "106300724"
---
# <a name="using-common-dialog-boxes"></a>Uso di finestre di dialogo comuni

In questa sezione vengono descritte le attività che richiamano le finestre di dialogo comuni:

-   [Scelta di un colore](#choosing-a-color)
-   [Scelta di un tipo di carattere](#choosing-a-font)
-   [Apertura di un file](#opening-a-file)
-   [Visualizzazione della finestra di dialogo Stampa](#displaying-the-print-dialog-box)
-   [Uso della finestra delle proprietà di stampa](#using-the-print-property-sheet)
-   [Impostazione della pagina stampata](#setting-up-the-printed-page)
-   [Ricerca di testo](#finding-text)

## <a name="choosing-a-color"></a>Scelta di un colore

In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **colore** che consente a un utente di selezionare un colore. Il codice di esempio inizializza prima di tutto una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , quindi chiama la funzione [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) per visualizzare la finestra di dialogo. Se la funzione restituisce **true**, a indicare che l'utente ha selezionato un colore, il codice di esempio usa il colore selezionato per creare un nuovo pennello a tinta unita.

Questo esempio usa la struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per inizializzare la finestra di dialogo nel modo seguente:

-   Inizializza il membro **lpCustColors** con un puntatore a una matrice statica di valori. I colori nella matrice sono inizialmente neri, ma la matrice statica conserva i colori personalizzati creati dall'utente per le successive chiamate [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) .
-   Imposta il **flag \_ RGBINIT di CC** e inizializza il membro **rgbResult** per specificare il colore inizialmente selezionato all'apertura della finestra di dialogo. Se non è specificato, la selezione iniziale è nera. Nell'esempio viene utilizzata la variabile statica *rgbCurrent* per mantenere il valore selezionato tra le chiamate a [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).
-   Imposta il flag **CC \_ FULLOPEN** in modo che l'estensione colori personalizzati della finestra di dialogo sia sempre visualizzata.


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>Scelta di un tipo di carattere

In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **tipo di carattere** in modo che un utente possa scegliere gli attributi di un tipo di carattere. Il codice di esempio inizializza prima di tutto una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , quindi chiama la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per visualizzare la finestra di dialogo.

In questo esempio viene impostato il flag **CF \_ SCREENFONTS** per specificare che nella finestra di dialogo devono essere visualizzati solo i tipi di carattere dello schermo. Imposta il flag **di \_ effetti CF** per visualizzare i controlli che consentono all'utente di selezionare le opzioni per l'attacco, la sottolineatura e il colore.

Se [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **true**, a indicare che l'utente ha fatto clic sul pulsante **OK** , la struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contiene informazioni che descrivono gli attributi del tipo di carattere e del tipo di carattere selezionati dall'utente, inclusi i membri della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta il membro **LPLOGFONT** . Il membro **rgbColors** contiene il colore del testo selezionato. Il codice di esempio usa queste informazioni per impostare il colore del tipo di carattere e del testo per il contesto di dispositivo associato alla finestra proprietaria.


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>Apertura di un file

> [!Note]  
> A partire da Windows Vista, la finestra di dialogo file comune è stata sostituita dalla finestra di dialogo elemento comune quando viene usata per aprire un file. Si consiglia di usare l'API della finestra di dialogo elemento comune anziché l'API della finestra di dialogo file comune. Per altre informazioni, vedere [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).

 

In questo argomento viene descritto il codice di esempio che consente di visualizzare una finestra di dialogo **aperta** , in modo che un utente possa specificare l'unità, la directory e il nome di un file da aprire. Il codice di esempio inizializza prima di tutto una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , quindi chiama la funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) per visualizzare la finestra di dialogo.

In questo esempio, il membro **lpstrFilter** è un puntatore a un buffer che specifica due filtri per i nomi di file che l'utente può selezionare per limitare i nomi di file visualizzati. Il buffer contiene una matrice di stringhe con terminazione null doppia in cui ogni coppia di stringhe specifica un filtro. Il membro **nFilterIndex** specifica che viene utilizzato il primo modello quando viene creata la finestra di dialogo.

In questo esempio vengono impostati i flag **OFN \_ PATHMUSTEXIST** e **OFN \_ FILEMUSTEXIST** nel membro **Flags** . Questi flag provocano la verifica da parte della finestra di dialogo, prima che venga restituito, che il percorso e il nome file specificati dall'utente esistano effettivamente.

La funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) restituisce **true** se l'utente fa clic sul pulsante **OK** e il percorso e il nome file specificati esistono. In questo caso, il buffer a cui punta il membro **lpstrFile** contiene il percorso e il nome del file. Il codice di esempio usa queste informazioni in una chiamata alla funzione per aprire il file.

Anche se in questo esempio non viene impostato il flag **OFN \_ Explorer** , viene comunque visualizzata la finestra di dialogo di **apertura** predefinita in stile Esplora risorse. Tuttavia, se si vuole fornire una routine hook o un modello personalizzato e si vuole usare l'interfaccia utente di Explorer, è necessario impostare il flag **OFN \_ Explorer** .

> [!Note]  
> Nel linguaggio di programmazione C, una stringa racchiusa tra virgolette è con terminazione null.

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>Visualizzazione della finestra di dialogo Stampa

In questo argomento viene descritto il codice di esempio in cui viene visualizzata una finestra di dialogo **stampa** in cui un utente può selezionare le opzioni per la stampa di un documento. Il codice di esempio inizializza prima di tutto una struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , quindi chiama la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la finestra di dialogo.

In questo esempio viene impostato il flag **PD \_ RETURNDC** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Questo fa in modo che [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisca un handle di contesto di dispositivo alla stampante selezionata nel membro **HDC** . È possibile utilizzare l'handle per eseguire il rendering dell'output sulla stampante.

In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**. Se la funzione restituisce **true**, questi membri restituiscono handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>Uso della finestra delle proprietà di stampa

In questo argomento viene descritto il codice di esempio che visualizza una finestra delle proprietà di **stampa** in modo che un utente possa selezionare le opzioni per la stampa di un documento. Il codice di esempio inizializza prima di tutto una struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , quindi chiama la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra delle proprietà.

Il codice di esempio imposta il flag **PD \_ RETURNDC** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . In questo modo, la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) restituisce un handle di contesto di dispositivo alla stampante selezionata nel membro **HDC** .

In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**. Se la funzione restituisce **S \_ OK**, questi membri restituiscono handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.

Al termine dell'operazione di stampa, il codice di esempio libera i buffer [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) e chiama la funzione [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) per eliminare il contesto di dispositivo.


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>Impostazione della pagina stampata

In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **Imposta pagina** in modo che un utente possa selezionare gli attributi della pagina stampata, ad esempio il tipo di carta, l'origine della carta, l'orientamento e i margini della pagina. Il codice di esempio inizializza prima di tutto una struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , quindi chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) per visualizzare la finestra di dialogo.

Questo esempio imposta il flag dei **\_ margini PSD** nel membro **Flags** e usa il membro **rtMargin** per specificare i valori dei margini iniziali. Imposta il flag **\_ INTHOUSANDTHSOFINCHES di PSD** per assicurarsi che la finestra di dialogo esprima le dimensioni dei margini in millesimi di pollice.

In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**. Se la funzione restituisce **true**, la funzione utilizza tali membri per restituire handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.

Nell'esempio seguente viene anche abilitata una procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook per personalizzare il disegno del contenuto della pagina di esempio.


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



Nell'esempio seguente viene illustrata una procedura di hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) di esempio che disegna il rettangolo dei margini nell'area della pagina di esempio:


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>Ricerca di testo

In questo argomento viene descritto il codice di esempio che consente di visualizzare e gestire una finestra di dialogo **trova** in modo che l'utente possa specificare i parametri di un'operazione di ricerca. La finestra di dialogo Invia messaggi alla routine della finestra in modo che sia possibile eseguire l'operazione di ricerca.

Il codice per la visualizzazione e la gestione di una finestra di dialogo di **sostituzione** è simile, ad eccezione del fatto che usa la funzione [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) per visualizzare la finestra di dialogo. La finestra di dialogo **Sostituisci** invia anche messaggi in risposta ai clic dell'utente sui pulsanti **Sostituisci** e **Sostituisci tutto** .

Per utilizzare la finestra di dialogo **trova** o **Sostituisci** , è necessario eseguire tre attività separate:

1.  Ottiene un identificatore di messaggio per il messaggio registrato [**FINDMSGSTRING**](findmsgstring.md) .
2.  Visualizza la finestra di dialogo.
3.  Elabora i messaggi [**FINDMSGSTRING**](findmsgstring.md) quando la finestra di dialogo è aperta.

Quando si inizializza l'applicazione, chiamare la funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio per il messaggio [**FINDMSGSTRING**](findmsgstring.md) registrato.


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Per visualizzare una finestra di dialogo **trova** , prima di tutto inizializzare una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , quindi chiamare la funzione [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . Si noti che la struttura **FindReplace** e il buffer per la stringa di ricerca devono essere una variabile globale o statica, in modo che non esca dall'ambito prima della chiusura della finestra di dialogo. È necessario impostare il membro **hwndOwner** per specificare la finestra che riceve i messaggi registrati. Dopo aver creato la finestra di dialogo, è possibile spostarla o modificarla usando l'handle restituito.


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



Quando la finestra di dialogo è aperta, il ciclo di messaggi principale deve includere una chiamata alla funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Passare un handle alla finestra di dialogo come parametro nella chiamata **IsDialogMessage** . Ciò garantisce che la finestra di dialogo elabori correttamente i messaggi della tastiera.

Per monitorare i messaggi inviati dalla finestra di dialogo, la routine della finestra deve verificare la presenza del messaggio registrato [**FINDMSGSTRING**](findmsgstring.md) ed elaborare i valori passati nella struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) come nell'esempio seguente.


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
