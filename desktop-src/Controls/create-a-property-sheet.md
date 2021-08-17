---
title: Come creare una finestra delle proprietà
description: L'esempio in questa sezione crea una finestra delle proprietà che contiene due pagine \ 8212; una per l'impostazione delle proprietà del carattere di una cella in un foglio di calcolo e un'altra per l'impostazione delle proprietà del bordo della cella.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa99c3e678fa7d8e6aa70cd3f5c6e4c7bc514f94114c7bb7a411fa7df1caac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831847"
---
# <a name="how-to-create-a-property-sheet"></a>Come creare una finestra delle proprietà

Nell'esempio riportato in questa sezione viene creata una finestra delle proprietà contenente due pagine, una per l'impostazione delle proprietà del tipo di carattere di una cella in un foglio di calcolo e l'altra per l'impostazione delle proprietà del bordo della cella.

L'esempio definisce le pagine compilando una coppia di strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) e specificando l'indirizzo nella [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) passata alla [**funzione PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-property-sheet"></a>Creare una finestra delle proprietà

Nell'esempio di codice seguente viene illustrato come creare una finestra delle proprietà a due pagine.


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a>Commenti

I modelli di finestra di dialogo, le icone e le etichette per le pagine vengono caricati dalle risorse contenute nel file eseguibile dell'applicazione. L'icona per la finestra delle proprietà viene caricata anche dalle risorse dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Esempio di proprietà](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




