---
title: Uso di finestre di dialogo comuni
description: Questa sezione illustra le attività che richiamano finestre di dialogo comuni.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Libreria di finestre di dialogo comuni,attività
- finestre di dialogo comuni, uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773382a34b048e812a3fb093da0492b0c628fb14
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590658"
---
# <a name="using-common-dialog-boxes"></a>Uso di finestre di dialogo comuni

Questa sezione illustra le attività che richiamano finestre di dialogo comuni:

-   [Scelta di un colore](#choosing-a-color)
-   [Scelta di un tipo di carattere](#choosing-a-font)
-   [Apertura di un file](#opening-a-file)
-   [Visualizzazione della finestra di dialogo Stampa](#displaying-the-print-dialog-box)
-   [Utilizzo della finestra delle proprietà Stampa](#using-the-print-property-sheet)
-   [Configurazione della pagina stampata](#setting-up-the-printed-page)
-   [Ricerca di testo](#finding-text)

## <a name="choosing-a-color"></a>Scelta di un colore

Questo argomento descrive il codice di esempio che visualizza una **finestra di** dialogo Colore in modo che un utente possa selezionare un colore. Il codice di esempio inizializza prima una [**struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e quindi chiama la [**funzione ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) per visualizzare la finestra di dialogo. Se la funzione restituisce **TRUE,** a indicare che l'utente ha selezionato un colore, il codice di esempio usa il colore selezionato per creare un nuovo pennello a tinta unita.

In questo esempio viene utilizzata [**la struttura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per inizializzare la finestra di dialogo come indicato di seguito:

-   Inizializza il membro **lpCustColors** con un puntatore a una matrice statica di valori. I colori nella matrice sono inizialmente neri, ma la matrice statica mantiene i colori personalizzati creati dall'utente per le chiamate [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) successive.
-   Imposta il flag **\_ CC RGBINIT** e inizializza il membro **rgbResult** per specificare il colore selezionato inizialmente all'apertura della finestra di dialogo. Se non specificato, la selezione iniziale è nera. L'esempio usa la variabile statica *rgbCurrent* per mantenere il valore selezionato tra le chiamate a [**ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))
-   Imposta il flag **CC \_ FULLOPEN** in modo che l'estensione dei colori personalizzati della finestra di dialogo sia sempre visualizzata.


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

Questo argomento descrive il codice di esempio che visualizza una **finestra di** dialogo Tipo di carattere in modo che un utente possa scegliere gli attributi di un tipo di carattere. Il codice di esempio inizializza prima una [**struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e quindi chiama la [**funzione ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per visualizzare la finestra di dialogo.

In questo esempio viene impostato il flag **CF \_ SCREENFONTS** per specificare che nella finestra di dialogo devono essere visualizzati solo i tipi di carattere dello schermo. Imposta il flag **CF \_ EFFECTS** per visualizzare i controlli che consentono all'utente di selezionare le opzioni barrato, sottolineatura e colore.

Se [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **TRUE,** a indicare che l'utente ha fatto clic sul pulsante **OK,** la struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contiene informazioni che descrivono il tipo di carattere e gli attributi del tipo di carattere selezionati dall'utente, inclusi i membri della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta il membro **lpLogFont.** Il **membro rgbColors** contiene il colore del testo selezionato. Il codice di esempio usa queste informazioni per impostare il tipo di carattere e il colore del testo per il contesto di dispositivo associato alla finestra proprietaria.


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
> A partire da Windows Vista, la finestra di dialogo file comune è stata sostituita dalla finestra di dialogo elemento comune quando viene usata per aprire un file. È consigliabile usare l'API Common Item Dialog anziché l'API Common File Dialog. Per altre informazioni, vedere [Finestra di dialogo elemento comune](/windows/win32/shell/common-file-dialog).

 

Questo argomento descrive il codice  di esempio che visualizza una finestra di dialogo Apri in modo che un utente possa specificare l'unità, la directory e il nome di un file da aprire. Il codice di esempio inizializza prima una [**struttura OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e quindi chiama la [**funzione GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) per visualizzare la finestra di dialogo.

In questo esempio il membro **lpstrFilter** è un puntatore a un buffer che specifica due filtri di nome file che l'utente può selezionare per limitare i nomi di file visualizzati. Il buffer contiene una matrice di stringhe con terminazione Double-Null in cui ogni coppia di stringhe specifica un filtro. Il **membro nFilterIndex** specifica che il primo criterio viene usato quando viene creata la finestra di dialogo.

In questo esempio vengono impostati i flag **OFN \_ PATHMUSTEXIST** e **OFN \_ FILEMUSTEXIST** nel **membro Flags.** Questi flag determinano che la finestra di dialogo verifichi, prima di restituire , che il percorso e il nome file specificati dall'utente esistano effettivamente.

La [**funzione GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) restituisce **TRUE** se l'utente fa clic sul pulsante **OK** e il percorso e il nome file specificati esistono. In questo caso, il buffer a cui punta il **membro lpstrFile** contiene il percorso e il nome del file. Il codice di esempio usa queste informazioni in una chiamata alla funzione per aprire il file.

Anche se in questo esempio non viene impostato il flag  **OFN \_ EXPLORER,** viene comunque visualizzata la finestra di dialogo Apri in stile Esplora risorse predefinita. Tuttavia, se si desidera fornire una routine hook o un modello personalizzato e si vuole l'interfaccia utente di Explorer, è necessario impostare il flag **OFN \_ EXPLORER.**

> [!Note]  
> Nel linguaggio di programmazione C una stringa racchiusa tra virgolette ha terminazione Null.

 


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

In questo argomento viene descritto il codice di esempio che visualizza una **finestra** di dialogo Stampa in modo che un utente possa selezionare le opzioni per la stampa di un documento. Il codice di esempio inizializza prima una [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e quindi chiama la [**funzione PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la finestra di dialogo.

In questo esempio viene impostato il flag **\_ RETURNDC PD** nel **membro Flags** della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) In questo modo [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce un handle di contesto di dispositivo alla stampante selezionata nel **membro hDC.** È possibile usare l'handle per eseguire il rendering dell'output sulla stampante.

Nell'input, il codice di esempio imposta **i membri hDevMode** e **hDevNames** su **NULL.** Se la funzione restituisce **TRUE,** questi membri restituiscono handle alle [**strutture DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.


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



## <a name="using-the-print-property-sheet"></a>Utilizzo della finestra delle proprietà Stampa

Questo argomento descrive il codice di esempio che visualizza una **finestra** delle proprietà Stampa in modo che un utente possa selezionare le opzioni per la stampa di un documento. Il codice di esempio inizializza prima una [**struttura PRINTDLGEX,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) quindi chiama la [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra delle proprietà.

Il codice di esempio imposta il flag **\_ RETURNDC PD** nel **membro Flags** della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) In questo modo [**la funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) restituisce un handle di contesto di dispositivo alla stampante selezionata nel **membro hDC.**

Nell'input, il codice di esempio imposta i **membri hDevMode** e **hDevNames** su **NULL.** Se la funzione restituisce **S \_ OK**, questi membri restituiscono handle alle [**strutture DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenenti l'input dell'utente e le informazioni sulla stampante. È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.

Al termine dell'operazione di stampa, il codice di esempio libera i buffer [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) e chiama la [**funzione DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) per eliminare il contesto di dispositivo.


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



## <a name="setting-up-the-printed-page"></a>Configurazione della pagina stampata

In questo argomento viene descritto  il codice di esempio che visualizza una finestra di dialogo Imposta pagina in modo che un utente possa selezionare gli attributi della pagina stampata, ad esempio il tipo di carta, l'origine della carta, l'orientamento della pagina e i margini della pagina. Il codice di esempio inizializza prima di tutto una [**struttura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e quindi chiama la [**funzione PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) per visualizzare la finestra di dialogo.

In questo esempio viene impostato il flag **\_ MARGINS PSD** nel **membro Flags** e viene utilizzato il membro **rtMargin** per specificare i valori iniziali del margine. Imposta il flag **\_ PSD INTHOUSANDTHSOFINCHES** per garantire che la finestra di dialogo esprima le dimensioni del margine in migliaia di pollici.

Nell'input, il codice di esempio imposta i **membri hDevMode** e **hDevNames** su **NULL.** Se la funzione restituisce **TRUE,** la funzione usa questi membri per restituire handle alle [**strutture DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) contenenti l'input dell'utente e le informazioni sulla stampante. È possibile usare queste informazioni per preparare l'output da inviare alla stampante selezionata.

L'esempio seguente consente anche a una routine hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) di personalizzare il disegno del contenuto della pagina di esempio.


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



L'esempio seguente illustra una procedura hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) di esempio che disegna il rettangolo dei margini nell'area della pagina di esempio:


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

Questo argomento descrive il codice di  esempio che visualizza e gestisce una finestra di dialogo Trova in modo che l'utente possa specificare i parametri di un'operazione di ricerca. La finestra di dialogo invia messaggi alla routine della finestra in modo da poter eseguire l'operazione di ricerca.

Il codice per la visualizzazione e la gestione di una **finestra** di dialogo Sostituisci è simile, ad eccezione del fatto che usa la [**funzione ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) per visualizzare la finestra di dialogo. La **finestra** di dialogo Sostituisci invia anche messaggi in risposta ai clic dell'utente sui **pulsanti** Sostituisci **e** Sostituisci tutto.

Per usare la **finestra di** dialogo Trova **o** Sostituisci, è necessario eseguire tre attività distinte:

1.  Ottiene un identificatore di messaggio per il [**messaggio registrato FINDMSGSTRING.**](findmsgstring.md)
2.  Visualizzare la finestra di dialogo.
3.  Elaborare [**i messaggi FINDMSGSTRING**](findmsgstring.md) quando la finestra di dialogo è aperta.

Quando si inizializza l'applicazione, chiamare la [**funzione RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio per il [**messaggio registrato FINDMSGSTRING.**](findmsgstring.md)


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Per visualizzare una **finestra di** dialogo Trova, inizializzare prima una [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e quindi chiamare la [**funzione FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) Si noti che la struttura **FINDREPLACE** e il buffer per la stringa di ricerca devono essere una variabile globale o statica in modo che non ese termini dall'ambito prima della chiusura della finestra di dialogo. È necessario impostare il **membro hwndOwner** per specificare la finestra che riceve i messaggi registrati. Dopo aver creato la finestra di dialogo, è possibile spostarla o modificarla usando l'handle restituito.


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



Quando la finestra di dialogo è aperta, il ciclo di messaggi principale deve includere una chiamata alla [**funzione IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Passare un handle alla finestra di dialogo come parametro nella **chiamata IsDialogMessage.** In questo modo la finestra di dialogo elabora correttamente i messaggi della tastiera.

Per monitorare i messaggi inviati dalla finestra di dialogo, la routine della finestra deve verificare la presenza del messaggio registrato [**FINDMSGSTRING**](findmsgstring.md) ed elaborare i valori passati nella struttura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) come nell'esempio seguente.


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



 

 
