---
title: Come stampare il contenuto dei controlli Rich Edit
description: Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300536"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="3798e-103">Come stampare il contenuto dei controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="3798e-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="3798e-104">Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3798e-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3798e-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="3798e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3798e-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="3798e-106">Technologies</span></span>

-   [<span data-ttu-id="3798e-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="3798e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3798e-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3798e-108">Prerequisites</span></span>

-   <span data-ttu-id="3798e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="3798e-109">C/C++</span></span>
-   <span data-ttu-id="3798e-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="3798e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3798e-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="3798e-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="3798e-112">USA anteprima di stampa</span><span class="sxs-lookup"><span data-stu-id="3798e-112">Use Print Preview</span></span>

<span data-ttu-id="3798e-113">Per formattare il testo in un controllo Rich Edit come verrà visualizzato in un dispositivo di destinazione (in genere la pagina stampata), inviare il messaggio [**em \_ SETTARGETDEVICE**](em-settargetdevice.md) , passando l'handle a un contesto di dispositivo (HDC) del dispositivo di destinazione e alla lunghezza di riga desiderata.</span><span class="sxs-lookup"><span data-stu-id="3798e-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="3798e-114">In genere si otterrà la lunghezza della linea chiamando [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) per l'HDC di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3798e-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="3798e-115">Formattare la stampa per un dispositivo specifico</span><span class="sxs-lookup"><span data-stu-id="3798e-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="3798e-116">Per formattare parte del contenuto di un controllo Rich Edit per un dispositivo specifico, inviare il [**messaggio \_ FormatRange em**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="3798e-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="3798e-117">La struttura [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) usata con questo messaggio specifica l'intervallo di testo da formattare e l'HDC per il dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3798e-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="3798e-118">Facoltativamente, questo messaggio invia anche il testo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="3798e-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="3798e-119">USA bande</span><span class="sxs-lookup"><span data-stu-id="3798e-119">Use Banding</span></span>

<span data-ttu-id="3798e-120">La banda è il processo mediante il quale viene generata una singola pagina di output utilizzando uno o più rettangoli o bande separate.</span><span class="sxs-lookup"><span data-stu-id="3798e-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="3798e-121">Quando tutte le bande vengono posizionate nella pagina, viene generato un risultato di un'immagine completa.</span><span class="sxs-lookup"><span data-stu-id="3798e-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="3798e-122">Questo approccio viene spesso usato dalle stampanti raster che non dispongono di memoria sufficiente o della possibilità di creare un'immagine di una pagina intera in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="3798e-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="3798e-123">Per implementare il banding, usare il messaggio [**\_ DISPLAYBAND em**](em-displayband.md) per inviare al dispositivo parti successive del contenuto del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3798e-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="3798e-124">Questo messaggio viene stampato sul dispositivo specificato in una precedente chiamata a [**em \_ FormatRange**](em-formatrange.md).</span><span class="sxs-lookup"><span data-stu-id="3798e-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="3798e-125">Naturalmente, il parametro *wParam* del messaggio **\_ FormatRange em** deve essere zero, in modo che la stampa non venga avviata dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="3798e-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="3798e-126">Esempio di codice PrintRTF</span><span class="sxs-lookup"><span data-stu-id="3798e-126">PrintRTF Code Example</span></span>

<span data-ttu-id="3798e-127">Nell'esempio di codice seguente viene stampato il contenuto di un controllo Rich Edit sulla stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="3798e-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="3798e-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3798e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3798e-129">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="3798e-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="3798e-130">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3798e-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 