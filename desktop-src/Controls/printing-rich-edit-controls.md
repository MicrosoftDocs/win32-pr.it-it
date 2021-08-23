---
title: Come stampare il contenuto dei controlli Rich Edit
description: Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00c7a7287fc86e47e085cfacd7757a7e24b4a91a3a513e75dc4610b51606b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575551"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Come stampare il contenuto dei controlli Rich Edit

Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-print-preview"></a>Usare l'anteprima di stampa

Per formattare il testo in un controllo Rich Edit così come verrà visualizzato in un dispositivo di destinazione (in genere la pagina stampata), inviare il messaggio [**EM \_ SETTARGETDEVICE,**](em-settargetdevice.md) passando l'handle a un contesto di dispositivo (HDC) del dispositivo di destinazione e alla larghezza della riga desiderata. In genere si ottiene lo spessore della linea chiamando [**GetDeviceCaps per**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) l'HDC di destinazione.

### <a name="format-print-for-a-specific-device"></a>Formattare la stampa per un dispositivo specifico

Per formattare parte del contenuto di un controllo Rich Edit per un dispositivo specifico, inviare il [**messaggio EM \_ FORMATRANGE.**](em-formatrange.md) La [**struttura FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) usata con questo messaggio specifica l'intervallo di testo da formattare, nonché l'HDC per il dispositivo di destinazione. Facoltativamente, questo messaggio invia anche il testo alla stampante.

### <a name="use-banding"></a>Usare l'uso di bande

L'applicazione di bande è il processo tramite il quale viene generata una singola pagina di output usando uno o più rettangoli separati o bande. Quando tutte le bande vengono posizionate nella pagina, viene restituita un'immagine completa. Questo approccio viene spesso usato dalle stampanti raster che non hanno memoria sufficiente o non hanno la possibilità di creare un'immagine di una pagina intera contemporaneamente.

Per implementare il banding, usare il messaggio [**EM \_ DISPLAYBAND**](em-displayband.md) per inviare parti successive del contenuto del controllo Rich Edit al dispositivo. Questo messaggio viene stampato sul dispositivo specificato in una chiamata precedente a [**EM \_ FORMATRANGE**](em-formatrange.md). Naturalmente, il *parametro wParam* del messaggio **EM \_ FORMATRANGE** deve essere zero, in modo che la stampa non sia avviata da tale messaggio.

## <a name="printrtf-code-example"></a>Esempio di codice PrintRTF

Il codice di esempio seguente stampa il contenuto di un controllo Rich Edit nella stampante specificata.


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

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 