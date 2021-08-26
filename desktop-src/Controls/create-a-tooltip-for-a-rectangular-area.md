---
title: Come creare una descrizione comando per un'area rettangolare
description: Nell'esempio seguente viene illustrato come creare un controllo descrizione comando standard per l'intera area client di una finestra.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9be19be187e8c09b3aeb618e1c3518c7c15ca66816cbbb751abe43aa0b9172a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920696"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Come creare una descrizione comando per un'area rettangolare

Nell'esempio seguente viene illustrato come creare un controllo descrizione comando standard per l'intera area client di una finestra.

La figura seguente mostra la descrizione comando visualizzata quando il puntatore del mouse si trova all'interno della finestra client di una finestra di dialogo. L'handle della finestra di dialogo è stato passato alla funzione illustrata nell'esempio precedente.

![screenshot di una finestra di dialogo; il puntatore del mouse si trova all'interno della finestra client ed è visibile una descrizione comando](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Creare una descrizione comando per un'area rettangolare

Nell'esempio seguente viene illustrato come creare un controllo descrizione comando standard per l'intera area client di una finestra.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli descrizione comando](using-tooltip-contro.md)
</dt> </dl>

 

 




