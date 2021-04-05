---
title: Come creare una descrizione comando per un'area rettangolare
description: Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708653"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Come creare una descrizione comando per un'area rettangolare

Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.

Nella figura seguente viene illustrata la descrizione comando visualizzata quando il puntatore del mouse si trova all'interno della finestra client di una finestra di dialogo. L'handle della finestra di dialogo è stato passato alla funzione illustrata nell'esempio precedente.

![Screenshot di una finestra di dialogo; il puntatore del mouse si trova all'interno della finestra client e una descrizione comando è visibile](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Creare una descrizione comando per un'area rettangolare

Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.


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

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




