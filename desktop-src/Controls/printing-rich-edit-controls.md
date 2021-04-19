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
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Come stampare il contenuto dei controlli Rich Edit

Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-print-preview"></a>USA anteprima di stampa

Per formattare il testo in un controllo Rich Edit come verrà visualizzato in un dispositivo di destinazione (in genere la pagina stampata), inviare il messaggio [**em \_ SETTARGETDEVICE**](em-settargetdevice.md) , passando l'handle a un contesto di dispositivo (HDC) del dispositivo di destinazione e alla lunghezza di riga desiderata. In genere si otterrà la lunghezza della linea chiamando [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) per l'HDC di destinazione.

### <a name="format-print-for-a-specific-device"></a>Formattare la stampa per un dispositivo specifico

Per formattare parte del contenuto di un controllo Rich Edit per un dispositivo specifico, inviare il [**messaggio \_ FormatRange em**](em-formatrange.md) . La struttura [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) usata con questo messaggio specifica l'intervallo di testo da formattare e l'HDC per il dispositivo di destinazione. Facoltativamente, questo messaggio invia anche il testo alla stampante.

### <a name="use-banding"></a>USA bande

La banda è il processo mediante il quale viene generata una singola pagina di output utilizzando uno o più rettangoli o bande separate. Quando tutte le bande vengono posizionate nella pagina, viene generato un risultato di un'immagine completa. Questo approccio viene spesso usato dalle stampanti raster che non dispongono di memoria sufficiente o della possibilità di creare un'immagine di una pagina intera in una sola volta.

Per implementare il banding, usare il messaggio [**\_ DISPLAYBAND em**](em-displayband.md) per inviare al dispositivo parti successive del contenuto del controllo Rich Edit. Questo messaggio viene stampato sul dispositivo specificato in una precedente chiamata a [**em \_ FormatRange**](em-formatrange.md). Naturalmente, il parametro *wParam* del messaggio **\_ FormatRange em** deve essere zero, in modo che la stampa non venga avviata dal messaggio.

## <a name="printrtf-code-example"></a>Esempio di codice PrintRTF

Nell'esempio di codice seguente viene stampato il contenuto di un controllo Rich Edit sulla stampante specificata.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 