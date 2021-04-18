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
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="8974e-103">Procedura: recuperare un contesto di dispositivo stampante</span><span class="sxs-lookup"><span data-stu-id="8974e-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="8974e-104">In questo argomento viene descritto come recuperare un contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="8974e-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="8974e-105">È possibile recuperare un contesto di dispositivo stampante chiamando direttamente la funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) oppure può essere restituito da una finestra di dialogo **stampa** comune.</span><span class="sxs-lookup"><span data-stu-id="8974e-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="8974e-106">Quando si visualizza una finestra di dialogo **stampa** comune, un utente sarà in grado di selezionare la stampante, le pagine del documento e il numero di copie del documento che si desidera stampare.</span><span class="sxs-lookup"><span data-stu-id="8974e-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="8974e-107">La finestra di dialogo **stampa** comune restituisce queste selezioni in una struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="8974e-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="8974e-108">In questo argomento viene descritto come ottenere un contesto di dispositivo stampante utilizzando i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8974e-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="8974e-109">Chiama CreateDC</span><span class="sxs-lookup"><span data-stu-id="8974e-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="8974e-110">Visualizza una finestra di dialogo Stampa comune</span><span class="sxs-lookup"><span data-stu-id="8974e-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="8974e-111">Uso della funzione PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="8974e-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="8974e-112">Uso della funzione PrintDlg</span><span class="sxs-lookup"><span data-stu-id="8974e-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="8974e-113">Chiama CreateDC</span><span class="sxs-lookup"><span data-stu-id="8974e-113">Call CreateDC</span></span>

<span data-ttu-id="8974e-114">Se si conosce il dispositivo in cui si desidera stampare, è possibile chiamare [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) e passare le informazioni direttamente alla funzione.</span><span class="sxs-lookup"><span data-stu-id="8974e-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="8974e-115">**CreateDC** restituisce un contesto di dispositivo in cui è possibile eseguire il rendering del contenuto da stampare.</span><span class="sxs-lookup"><span data-stu-id="8974e-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="8974e-116">La chiamata più semplice per recuperare un contesto di dispositivo è illustrata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="8974e-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="8974e-117">Il codice in questo esempio recupera un contesto di dispositivo sul dispositivo di visualizzazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="8974e-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="8974e-118">Per eseguire il rendering in una stampante specifica, è necessario specificare "WINSPOOL" come dispositivo e passare il nome corretto della stampante a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="8974e-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="8974e-119">È anche possibile passare una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nella chiamata a **CreateDC** se si desidera fornire dati di inizializzazione specifici del dispositivo per il driver di dispositivo quando si crea il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8974e-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="8974e-120">Nell'esempio seguente viene illustrata una chiamata a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in cui è selezionato il driver "winspool" e il nome della stampante viene specificato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="8974e-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="8974e-121">È possibile ottenere la stringa del nome esatto della stampante da passare a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) chiamando la funzione [**EnumPrinters**](enumprinters.md) .</span><span class="sxs-lookup"><span data-stu-id="8974e-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="8974e-122">Nell'esempio di codice seguente viene illustrato come chiamare **EnumPrinters** e ottenere i nomi delle stampanti locali e connesse localmente.</span><span class="sxs-lookup"><span data-stu-id="8974e-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="8974e-123">Poiché le dimensioni del buffer richiesto non sono note in anticipo, il **EnumPrinters** viene chiamato due volte.</span><span class="sxs-lookup"><span data-stu-id="8974e-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="8974e-124">La prima chiamata restituisce la dimensione del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="8974e-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="8974e-125">Tali informazioni vengono utilizzate per allocare un buffer della dimensione richiesta e la seconda chiamata a **EnumPrinters** restituisce i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="8974e-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


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



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="8974e-126">Visualizza una finestra di dialogo Stampa comune</span><span class="sxs-lookup"><span data-stu-id="8974e-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="8974e-127">È possibile scegliere tra due finestre di dialogo comuni di **stampa** per visualizzare un utente; la finestra di dialogo più recente, che può essere visualizzata chiamando la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e la finestra di dialogo stile precedente, che è possibile visualizzare chiamando la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8974e-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="8974e-128">Nelle sezioni seguenti viene descritto come chiamare ogni finestra di dialogo da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8974e-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="8974e-129">Uso della funzione PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="8974e-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="8974e-130">Chiamare la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra delle proprietà di **stampa** .</span><span class="sxs-lookup"><span data-stu-id="8974e-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="8974e-131">Utilizzando la finestra delle proprietà, l'utente può specificare le informazioni sul processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8974e-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="8974e-132">Ad esempio, l'utente può selezionare un intervallo di pagine da stampare, il numero di copie e così via.</span><span class="sxs-lookup"><span data-stu-id="8974e-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="8974e-133">Il **PRINTDLGEX** può anche recuperare un handle per un contesto di dispositivo per la stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="8974e-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="8974e-134">È possibile utilizzare l'handle per eseguire il rendering dell'output sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="8974e-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="8974e-135">Per il codice di esempio che illustra l'uso di [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per recuperare un contesto di dispositivo stampante, vedere l'argomento relativo all'uso della finestra delle proprietà di stampa in [uso di finestre di dialogo comuni](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="8974e-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="8974e-136">Uso della funzione PrintDlg</span><span class="sxs-lookup"><span data-stu-id="8974e-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="8974e-137">Se l'applicazione deve essere eseguita in un sistema che non supporta la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , ad esempio in un sistema che esegue una versione di Windows precedente a Windows 2000 o non richiede la funzionalità aggiuntiva fornita dalla funzione **PRINTDLGEX** , utilizzare la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8974e-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="8974e-138">Nei passaggi seguenti viene descritto come visualizzare la finestra di dialogo comune **stampa** di stile precedente.</span><span class="sxs-lookup"><span data-stu-id="8974e-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="8974e-139">Inizializza la struttura dei dati [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="8974e-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="8974e-140">Chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la finestra di dialogo **stampa** comune per l'utente.</span><span class="sxs-lookup"><span data-stu-id="8974e-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="8974e-141">Se la chiamata [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **true**, bloccare la memoria della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita.</span><span class="sxs-lookup"><span data-stu-id="8974e-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="8974e-142">Se la chiamata **PrintDlg** restituisce **false**, l'utente ha premuto il pulsante **Annulla** nella finestra di dialogo **stampa** comune in modo che non vi sia altro da elaborare.</span><span class="sxs-lookup"><span data-stu-id="8974e-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="8974e-143">Allocare un buffer di memoria locale sufficientemente grande da contenere una copia della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="8974e-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="8974e-144">Copiare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita in quella allocata localmente.</span><span class="sxs-lookup"><span data-stu-id="8974e-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="8974e-145">Salvare altre informazioni restituite nella struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e che sarà necessario elaborare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8974e-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="8974e-146">Liberare il [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e i buffer di memoria a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="8974e-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="8974e-147">Nell'esempio di codice seguente viene illustrato come utilizzare la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per ottenere il contesto di dispositivo e il nome della stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="8974e-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


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



<span data-ttu-id="8974e-148">Per ulteriori informazioni sulla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , vedere "visualizzazione della finestra di dialogo Stampa" in utilizzo di finestre di [dialogo comuni](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="8974e-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
