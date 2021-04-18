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
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="caa61-105">Uso di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="caa61-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="caa61-106">In questa sezione vengono descritte le attività che richiamano le finestre di dialogo comuni:</span><span class="sxs-lookup"><span data-stu-id="caa61-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="caa61-107">Scelta di un colore</span><span class="sxs-lookup"><span data-stu-id="caa61-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="caa61-108">Scelta di un tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="caa61-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="caa61-109">Apertura di un file</span><span class="sxs-lookup"><span data-stu-id="caa61-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="caa61-110">Visualizzazione della finestra di dialogo Stampa</span><span class="sxs-lookup"><span data-stu-id="caa61-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="caa61-111">Uso della finestra delle proprietà di stampa</span><span class="sxs-lookup"><span data-stu-id="caa61-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="caa61-112">Impostazione della pagina stampata</span><span class="sxs-lookup"><span data-stu-id="caa61-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="caa61-113">Ricerca di testo</span><span class="sxs-lookup"><span data-stu-id="caa61-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="caa61-114">Scelta di un colore</span><span class="sxs-lookup"><span data-stu-id="caa61-114">Choosing a Color</span></span>

<span data-ttu-id="caa61-115">In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **colore** che consente a un utente di selezionare un colore.</span><span class="sxs-lookup"><span data-stu-id="caa61-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="caa61-116">Il codice di esempio inizializza prima di tutto una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , quindi chiama la funzione [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="caa61-117">Se la funzione restituisce **true**, a indicare che l'utente ha selezionato un colore, il codice di esempio usa il colore selezionato per creare un nuovo pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="caa61-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="caa61-118">Questo esempio usa la struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) per inizializzare la finestra di dialogo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="caa61-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="caa61-119">Inizializza il membro **lpCustColors** con un puntatore a una matrice statica di valori.</span><span class="sxs-lookup"><span data-stu-id="caa61-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="caa61-120">I colori nella matrice sono inizialmente neri, ma la matrice statica conserva i colori personalizzati creati dall'utente per le successive chiamate [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="caa61-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="caa61-121">Imposta il **flag \_ RGBINIT di CC** e inizializza il membro **rgbResult** per specificare il colore inizialmente selezionato all'apertura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="caa61-122">Se non è specificato, la selezione iniziale è nera.</span><span class="sxs-lookup"><span data-stu-id="caa61-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="caa61-123">Nell'esempio viene utilizzata la variabile statica *rgbCurrent* per mantenere il valore selezionato tra le chiamate a [**le CHOOSECOLOR.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="caa61-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="caa61-124">Imposta il flag **CC \_ FULLOPEN** in modo che l'estensione colori personalizzati della finestra di dialogo sia sempre visualizzata.</span><span class="sxs-lookup"><span data-stu-id="caa61-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="caa61-125">Scelta di un tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="caa61-125">Choosing a Font</span></span>

<span data-ttu-id="caa61-126">In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **tipo di carattere** in modo che un utente possa scegliere gli attributi di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="caa61-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="caa61-127">Il codice di esempio inizializza prima di tutto una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , quindi chiama la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="caa61-128">In questo esempio viene impostato il flag **CF \_ SCREENFONTS** per specificare che nella finestra di dialogo devono essere visualizzati solo i tipi di carattere dello schermo.</span><span class="sxs-lookup"><span data-stu-id="caa61-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="caa61-129">Imposta il flag **di \_ effetti CF** per visualizzare i controlli che consentono all'utente di selezionare le opzioni per l'attacco, la sottolineatura e il colore.</span><span class="sxs-lookup"><span data-stu-id="caa61-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="caa61-130">Se [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) restituisce **true**, a indicare che l'utente ha fatto clic sul pulsante **OK** , la struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contiene informazioni che descrivono gli attributi del tipo di carattere e del tipo di carattere selezionati dall'utente, inclusi i membri della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a cui punta il membro **LPLOGFONT** .</span><span class="sxs-lookup"><span data-stu-id="caa61-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="caa61-131">Il membro **rgbColors** contiene il colore del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="caa61-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="caa61-132">Il codice di esempio usa queste informazioni per impostare il colore del tipo di carattere e del testo per il contesto di dispositivo associato alla finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="caa61-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="caa61-133">Apertura di un file</span><span class="sxs-lookup"><span data-stu-id="caa61-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="caa61-134">A partire da Windows Vista, la finestra di dialogo file comune è stata sostituita dalla finestra di dialogo elemento comune quando viene usata per aprire un file.</span><span class="sxs-lookup"><span data-stu-id="caa61-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="caa61-135">Si consiglia di usare l'API della finestra di dialogo elemento comune anziché l'API della finestra di dialogo file comune.</span><span class="sxs-lookup"><span data-stu-id="caa61-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="caa61-136">Per altre informazioni, vedere [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="caa61-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="caa61-137">In questo argomento viene descritto il codice di esempio che consente di visualizzare una finestra di dialogo **aperta** , in modo che un utente possa specificare l'unità, la directory e il nome di un file da aprire.</span><span class="sxs-lookup"><span data-stu-id="caa61-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="caa61-138">Il codice di esempio inizializza prima di tutto una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , quindi chiama la funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="caa61-139">In questo esempio, il membro **lpstrFilter** è un puntatore a un buffer che specifica due filtri per i nomi di file che l'utente può selezionare per limitare i nomi di file visualizzati.</span><span class="sxs-lookup"><span data-stu-id="caa61-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="caa61-140">Il buffer contiene una matrice di stringhe con terminazione null doppia in cui ogni coppia di stringhe specifica un filtro.</span><span class="sxs-lookup"><span data-stu-id="caa61-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="caa61-141">Il membro **nFilterIndex** specifica che viene utilizzato il primo modello quando viene creata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="caa61-142">In questo esempio vengono impostati i flag **OFN \_ PATHMUSTEXIST** e **OFN \_ FILEMUSTEXIST** nel membro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="caa61-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="caa61-143">Questi flag provocano la verifica da parte della finestra di dialogo, prima che venga restituito, che il percorso e il nome file specificati dall'utente esistano effettivamente.</span><span class="sxs-lookup"><span data-stu-id="caa61-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="caa61-144">La funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) restituisce **true** se l'utente fa clic sul pulsante **OK** e il percorso e il nome file specificati esistono.</span><span class="sxs-lookup"><span data-stu-id="caa61-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="caa61-145">In questo caso, il buffer a cui punta il membro **lpstrFile** contiene il percorso e il nome del file.</span><span class="sxs-lookup"><span data-stu-id="caa61-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="caa61-146">Il codice di esempio usa queste informazioni in una chiamata alla funzione per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="caa61-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="caa61-147">Anche se in questo esempio non viene impostato il flag **OFN \_ Explorer** , viene comunque visualizzata la finestra di dialogo di **apertura** predefinita in stile Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="caa61-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="caa61-148">Tuttavia, se si vuole fornire una routine hook o un modello personalizzato e si vuole usare l'interfaccia utente di Explorer, è necessario impostare il flag **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="caa61-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="caa61-149">Nel linguaggio di programmazione C, una stringa racchiusa tra virgolette è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="caa61-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="caa61-150">Visualizzazione della finestra di dialogo Stampa</span><span class="sxs-lookup"><span data-stu-id="caa61-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="caa61-151">In questo argomento viene descritto il codice di esempio in cui viene visualizzata una finestra di dialogo **stampa** in cui un utente può selezionare le opzioni per la stampa di un documento.</span><span class="sxs-lookup"><span data-stu-id="caa61-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="caa61-152">Il codice di esempio inizializza prima di tutto una struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , quindi chiama la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="caa61-153">In questo esempio viene impostato il flag **PD \_ RETURNDC** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="caa61-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="caa61-154">Questo fa in modo che [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisca un handle di contesto di dispositivo alla stampante selezionata nel membro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="caa61-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="caa61-155">È possibile utilizzare l'handle per eseguire il rendering dell'output sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="caa61-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="caa61-156">In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**.</span><span class="sxs-lookup"><span data-stu-id="caa61-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="caa61-157">Se la funzione restituisce **true**, questi membri restituiscono handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="caa61-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="caa61-158">È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="caa61-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="caa61-159">Uso della finestra delle proprietà di stampa</span><span class="sxs-lookup"><span data-stu-id="caa61-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="caa61-160">In questo argomento viene descritto il codice di esempio che visualizza una finestra delle proprietà di **stampa** in modo che un utente possa selezionare le opzioni per la stampa di un documento.</span><span class="sxs-lookup"><span data-stu-id="caa61-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="caa61-161">Il codice di esempio inizializza prima di tutto una struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , quindi chiama la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="caa61-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="caa61-162">Il codice di esempio imposta il flag **PD \_ RETURNDC** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="caa61-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="caa61-163">In questo modo, la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) restituisce un handle di contesto di dispositivo alla stampante selezionata nel membro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="caa61-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="caa61-164">In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**.</span><span class="sxs-lookup"><span data-stu-id="caa61-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="caa61-165">Se la funzione restituisce **S \_ OK**, questi membri restituiscono handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="caa61-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="caa61-166">È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="caa61-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="caa61-167">Al termine dell'operazione di stampa, il codice di esempio libera i buffer [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) e chiama la funzione [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) per eliminare il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="caa61-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="caa61-168">Impostazione della pagina stampata</span><span class="sxs-lookup"><span data-stu-id="caa61-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="caa61-169">In questo argomento viene descritto il codice di esempio che visualizza una finestra di dialogo **Imposta pagina** in modo che un utente possa selezionare gli attributi della pagina stampata, ad esempio il tipo di carta, l'origine della carta, l'orientamento e i margini della pagina.</span><span class="sxs-lookup"><span data-stu-id="caa61-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="caa61-170">Il codice di esempio inizializza prima di tutto una struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , quindi chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="caa61-171">Questo esempio imposta il flag dei **\_ margini PSD** nel membro **Flags** e usa il membro **rtMargin** per specificare i valori dei margini iniziali.</span><span class="sxs-lookup"><span data-stu-id="caa61-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="caa61-172">Imposta il flag **\_ INTHOUSANDTHSOFINCHES di PSD** per assicurarsi che la finestra di dialogo esprima le dimensioni dei margini in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="caa61-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="caa61-173">In input, il codice di esempio imposta i membri **hDevMode** e **hDevNames** su **null**.</span><span class="sxs-lookup"><span data-stu-id="caa61-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="caa61-174">Se la funzione restituisce **true**, la funzione utilizza tali membri per restituire handle alle strutture [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) che contengono l'input dell'utente e le informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="caa61-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="caa61-175">È possibile utilizzare queste informazioni per preparare l'output da inviare alla stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="caa61-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="caa61-176">Nell'esempio seguente viene anche abilitata una procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook per personalizzare il disegno del contenuto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="caa61-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="caa61-177">Nell'esempio seguente viene illustrata una procedura di hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) di esempio che disegna il rettangolo dei margini nell'area della pagina di esempio:</span><span class="sxs-lookup"><span data-stu-id="caa61-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="caa61-178">Ricerca di testo</span><span class="sxs-lookup"><span data-stu-id="caa61-178">Finding Text</span></span>

<span data-ttu-id="caa61-179">In questo argomento viene descritto il codice di esempio che consente di visualizzare e gestire una finestra di dialogo **trova** in modo che l'utente possa specificare i parametri di un'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="caa61-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="caa61-180">La finestra di dialogo Invia messaggi alla routine della finestra in modo che sia possibile eseguire l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="caa61-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="caa61-181">Il codice per la visualizzazione e la gestione di una finestra di dialogo di **sostituzione** è simile, ad eccezione del fatto che usa la funzione [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="caa61-182">La finestra di dialogo **Sostituisci** invia anche messaggi in risposta ai clic dell'utente sui pulsanti **Sostituisci** e **Sostituisci tutto** .</span><span class="sxs-lookup"><span data-stu-id="caa61-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="caa61-183">Per utilizzare la finestra di dialogo **trova** o **Sostituisci** , è necessario eseguire tre attività separate:</span><span class="sxs-lookup"><span data-stu-id="caa61-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="caa61-184">Ottiene un identificatore di messaggio per il messaggio registrato [**FINDMSGSTRING**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="caa61-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="caa61-185">Visualizza la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="caa61-186">Elabora i messaggi [**FINDMSGSTRING**](findmsgstring.md) quando la finestra di dialogo è aperta.</span><span class="sxs-lookup"><span data-stu-id="caa61-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="caa61-187">Quando si inizializza l'applicazione, chiamare la funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio per il messaggio [**FINDMSGSTRING**](findmsgstring.md) registrato.</span><span class="sxs-lookup"><span data-stu-id="caa61-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="caa61-188">Per visualizzare una finestra di dialogo **trova** , prima di tutto inizializzare una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , quindi chiamare la funzione [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="caa61-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="caa61-189">Si noti che la struttura **FindReplace** e il buffer per la stringa di ricerca devono essere una variabile globale o statica, in modo che non esca dall'ambito prima della chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="caa61-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="caa61-190">È necessario impostare il membro **hwndOwner** per specificare la finestra che riceve i messaggi registrati.</span><span class="sxs-lookup"><span data-stu-id="caa61-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="caa61-191">Dopo aver creato la finestra di dialogo, è possibile spostarla o modificarla usando l'handle restituito.</span><span class="sxs-lookup"><span data-stu-id="caa61-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="caa61-192">Quando la finestra di dialogo è aperta, il ciclo di messaggi principale deve includere una chiamata alla funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) .</span><span class="sxs-lookup"><span data-stu-id="caa61-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="caa61-193">Passare un handle alla finestra di dialogo come parametro nella chiamata **IsDialogMessage** .</span><span class="sxs-lookup"><span data-stu-id="caa61-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="caa61-194">Ciò garantisce che la finestra di dialogo elabori correttamente i messaggi della tastiera.</span><span class="sxs-lookup"><span data-stu-id="caa61-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="caa61-195">Per monitorare i messaggi inviati dalla finestra di dialogo, la routine della finestra deve verificare la presenza del messaggio registrato [**FINDMSGSTRING**](findmsgstring.md) ed elaborare i valori passati nella struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="caa61-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
