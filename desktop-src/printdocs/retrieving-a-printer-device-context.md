---
description: Questo argomento descrive come recuperare un contesto di dispositivo della stampante.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Procedura: Recuperare un contesto di dispositivo della stampante'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f723ece0e00d58ed684029e0eb3202d637443bd7f0e9d8878024346b9d79ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600561"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Procedura: Recuperare un contesto di dispositivo della stampante

Questo argomento descrive come recuperare un contesto di dispositivo della stampante. È possibile recuperare un contesto di dispositivo della stampante chiamando direttamente la [**funzione CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oppure può essere restituito da una **finestra di** dialogo stampa comune.

Quando si visualizza una **finestra** di dialogo Stampa comune, un utente sarà in grado di selezionare la stampante, le pagine del documento e il numero di copie del documento da stampare. La **finestra di** dialogo Stampa comune restituisce queste selezioni in una struttura di dati.

Questo argomento descrive come ottenere un contesto di dispositivo della stampante usando i metodi seguenti.

-   [Chiamare CreateDC](#call-createdc)
-   [Visualizzare una finestra di dialogo Stampa comune](#display-a-print-common-dialog-box)
    -   [Uso della funzione PrintDlgEx](#using-the-printdlgex-function)
    -   [Uso della funzione PrintDlg](#using-the-printdlg-function)

## <a name="call-createdc"></a>Chiamare CreateDC

Se si conosce il dispositivo a cui si vuole stampare, è possibile chiamare [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) e passare le informazioni direttamente alla funzione. **CreateDC** restituisce un contesto di dispositivo in cui è possibile eseguire il rendering del contenuto da stampare.

La chiamata più semplice per recuperare un contesto di dispositivo è illustrata nell'esempio di codice seguente. Il codice in questo esempio recupera un contesto di dispositivo per il dispositivo di visualizzazione predefinito.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Per eseguire il rendering a una stampante specifica, è necessario specificare "WINSPOOL" come dispositivo e passare il nome corretto della stampante a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). È anche possibile passare una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nella chiamata a **CreateDC** se si vogliono fornire dati di inizializzazione specifici del dispositivo per il driver di dispositivo quando si crea il contesto di dispositivo.

Nell'esempio seguente viene illustrata una chiamata a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in cui è selezionato il driver "WINSPOOL" e il nome della stampante viene specificato in base al nome.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



È possibile ottenere la stringa esatta del nome della stampante da passare a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) chiamando la [**funzione EnumPrinters.**](enumprinters.md) Nell'esempio di codice seguente viene illustrato come chiamare **EnumPrinters** e ottenere i nomi delle stampanti locali e connesse in locale. Poiché le dimensioni del buffer richiesto non possono essere note in anticipo, **EnumPrinters** viene chiamato due volte. La prima chiamata restituisce le dimensioni del buffer richiesto. Queste informazioni vengono usate per allocare un buffer delle dimensioni richieste e la seconda chiamata a **EnumPrinters** restituisce i dati desiderati.


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a>Visualizzare una finestra di dialogo Stampa comune

È possibile scegliere tra due **finestre di** dialogo comuni di stampa da visualizzare a un utente. la finestra di dialogo più recente, che è possibile visualizzare chiamando la funzione [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e la finestra di dialogo di stile precedente, che è possibile visualizzare chiamando la [**funzione PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Le sezioni seguenti descrivono come chiamare ogni finestra di dialogo da un'applicazione.

### <a name="using-the-printdlgex-function"></a>Uso della funzione PrintDlgEx

Chiamare la [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra **delle proprietà** Stampa. Usando la finestra delle proprietà, l'utente può specificare informazioni sul processo di stampa. Ad esempio, l'utente può selezionare un intervallo di pagine da stampare, il numero di copie e così via. **PrintDlgEx** può anche recuperare un handle per un contesto di dispositivo per la stampante selezionata. È possibile usare l'handle per eseguire il rendering dell'output sulla stampante.

Per il codice di esempio che illustra l'uso di [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per recuperare un contesto di dispositivo della stampante, vedere "Uso della finestra delle proprietà Di stampa" in [Uso di finestre di dialogo comuni](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Uso della funzione PrintDlg

Se l'applicazione deve essere eseguita in un sistema che non supporta la funzione [**PrintDlgEx,**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) ad esempio in un sistema che esegue una versione di Windows precedente a Windows 2000 o non richiede la funzionalità aggiuntiva fornita dalla funzione **PrintDlgEx,** usare la [**funzione PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) La procedura seguente descrive come visualizzare la finestra di dialogo **Stampa** comune di stile precedente.

1.  Inizializzare [**la struttura dei dati PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
2.  Chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la **finestra di** dialogo Stampa comune all'utente.
3.  Se la [**chiamata PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **TRUE,** bloccare la memoria della [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita. Se la **chiamata PrintDlg** restituisce  **FALSE,** l'utente ha premuto il pulsante **Annulla** nella finestra di dialogo Stampa comune in modo che non ci siano altri elementi da elaborare.
4.  Allocare un buffer di memoria locale sufficientemente grande da contenere una copia della [**struttura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
5.  Copiare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita nella struttura allocata in locale.
6.  Salvare altre informazioni restituite nella [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e che sarà necessario elaborare il processo di stampa.
7.  Liberare [**PRINTDLG e**](/windows/win32/api/commdlg/ns-commdlg-printdlga) i buffer di memoria a cui fa riferimento.

Il codice di esempio seguente illustra come usare la [**funzione PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per ottenere il contesto di dispositivo e il nome della stampante selezionata.


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



Per altre informazioni sulla [**funzione PrintDlg,**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) vedere "Visualizzazione della finestra di dialogo Stampa" in [Uso di finestre di dialogo comuni](../dlgbox/using-common-dialog-boxes.md).

 

 
