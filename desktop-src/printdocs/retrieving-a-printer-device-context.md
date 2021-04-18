---
description: In questo argomento viene descritto come recuperare un contesto di dispositivo stampante.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Procedura: recuperare un contesto di dispositivo stampante'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314988"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Procedura: recuperare un contesto di dispositivo stampante

In questo argomento viene descritto come recuperare un contesto di dispositivo stampante. È possibile recuperare un contesto di dispositivo stampante chiamando direttamente la funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oppure può essere restituito da una finestra di dialogo **stampa** comune.

Quando si visualizza una finestra di dialogo **stampa** comune, un utente sarà in grado di selezionare la stampante, le pagine del documento e il numero di copie del documento che si desidera stampare. La finestra di dialogo **stampa** comune restituisce queste selezioni in una struttura di dati.

In questo argomento viene descritto come ottenere un contesto di dispositivo stampante utilizzando i metodi seguenti.

-   [Chiama CreateDC](#call-createdc)
-   [Visualizza una finestra di dialogo Stampa comune](#display-a-print-common-dialog-box)
    -   [Uso della funzione PrintDlgEx](#using-the-printdlgex-function)
    -   [Uso della funzione PrintDlg](#using-the-printdlg-function)

## <a name="call-createdc"></a>Chiama CreateDC

Se si conosce il dispositivo in cui si desidera stampare, è possibile chiamare [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) e passare le informazioni direttamente alla funzione. **CreateDC** restituisce un contesto di dispositivo in cui è possibile eseguire il rendering del contenuto da stampare.

La chiamata più semplice per recuperare un contesto di dispositivo è illustrata nell'esempio di codice seguente. Il codice in questo esempio recupera un contesto di dispositivo sul dispositivo di visualizzazione predefinito.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Per eseguire il rendering in una stampante specifica, è necessario specificare "WINSPOOL" come dispositivo e passare il nome corretto della stampante a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). È anche possibile passare una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nella chiamata a **CreateDC** se si desidera fornire dati di inizializzazione specifici del dispositivo per il driver di dispositivo quando si crea il contesto di dispositivo.

Nell'esempio seguente viene illustrata una chiamata a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in cui è selezionato il driver "winspool" e il nome della stampante viene specificato in base al nome.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



È possibile ottenere la stringa del nome esatto della stampante da passare a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) chiamando la funzione [**EnumPrinters**](enumprinters.md) . Nell'esempio di codice seguente viene illustrato come chiamare **EnumPrinters** e ottenere i nomi delle stampanti locali e connesse localmente. Poiché le dimensioni del buffer richiesto non sono note in anticipo, il **EnumPrinters** viene chiamato due volte. La prima chiamata restituisce la dimensione del buffer richiesto. Tali informazioni vengono utilizzate per allocare un buffer della dimensione richiesta e la seconda chiamata a **EnumPrinters** restituisce i dati desiderati.


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



## <a name="display-a-print-common-dialog-box"></a>Visualizza una finestra di dialogo Stampa comune

È possibile scegliere tra due finestre di dialogo comuni di **stampa** per visualizzare un utente; la finestra di dialogo più recente, che può essere visualizzata chiamando la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e la finestra di dialogo stile precedente, che è possibile visualizzare chiamando la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Nelle sezioni seguenti viene descritto come chiamare ogni finestra di dialogo da un'applicazione.

### <a name="using-the-printdlgex-function"></a>Uso della funzione PrintDlgEx

Chiamare la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra delle proprietà di **stampa** . Utilizzando la finestra delle proprietà, l'utente può specificare le informazioni sul processo di stampa. Ad esempio, l'utente può selezionare un intervallo di pagine da stampare, il numero di copie e così via. Il **PRINTDLGEX** può anche recuperare un handle per un contesto di dispositivo per la stampante selezionata. È possibile utilizzare l'handle per eseguire il rendering dell'output sulla stampante.

Per il codice di esempio che illustra l'uso di [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per recuperare un contesto di dispositivo stampante, vedere l'argomento relativo all'uso della finestra delle proprietà di stampa in [uso di finestre di dialogo comuni](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Uso della funzione PrintDlg

Se l'applicazione deve essere eseguita in un sistema che non supporta la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , ad esempio in un sistema che esegue una versione di Windows precedente a Windows 2000 o non richiede la funzionalità aggiuntiva fornita dalla funzione **PRINTDLGEX** , utilizzare la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Nei passaggi seguenti viene descritto come visualizzare la finestra di dialogo comune **stampa** di stile precedente.

1.  Inizializza la struttura dei dati [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la finestra di dialogo **stampa** comune per l'utente.
3.  Se la chiamata [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **true**, bloccare la memoria della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita. Se la chiamata **PrintDlg** restituisce **false**, l'utente ha premuto il pulsante **Annulla** nella finestra di dialogo **stampa** comune in modo che non vi sia altro da elaborare.
4.  Allocare un buffer di memoria locale sufficientemente grande da contenere una copia della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .
5.  Copiare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita in quella allocata localmente.
6.  Salvare altre informazioni restituite nella struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e che sarà necessario elaborare il processo di stampa.
7.  Liberare il [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e i buffer di memoria a cui fa riferimento.

Nell'esempio di codice seguente viene illustrato come utilizzare la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per ottenere il contesto di dispositivo e il nome della stampante selezionata.


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



Per ulteriori informazioni sulla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , vedere "visualizzazione della finestra di dialogo Stampa" in utilizzo di finestre di [dialogo comuni](../dlgbox/using-common-dialog-boxes.md).

 

 
