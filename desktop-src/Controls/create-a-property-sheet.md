---
title: Come creare una finestra delle proprietà
description: Nell'esempio riportato in questa sezione viene creata una finestra delle proprietà che contiene due pagine \ 8212, una per l'impostazione delle proprietà del tipo di carattere di una cella in un foglio di calcolo e un'altra per l'impostazione delle proprietà del bordo della cella.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323816"
---
# <a name="how-to-create-a-property-sheet"></a>Come creare una finestra delle proprietà

Nell'esempio riportato in questa sezione viene creata una finestra delle proprietà che contiene due pagine, una per l'impostazione delle proprietà del tipo di carattere di una cella in un foglio di calcolo e un'altra per l'impostazione delle proprietà del bordo della cella.

Nell'esempio vengono definite le pagine compilando una coppia di strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) e specificando l'indirizzo nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) che viene passato alla funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-property-sheet"></a>Crea una finestra delle proprietà

Nell'esempio di codice riportato di seguito viene illustrato come creare una finestra delle proprietà a due pagine.


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

I modelli, le icone e le etichette della finestra di dialogo per le pagine vengono caricati dalle risorse contenute nel file eseguibile dell'applicazione. Anche l'icona per la finestra delle proprietà viene caricata dalle risorse dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Esempio di proprietà](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




