---
title: Come implementare le descrizioni comandi del fumetto
description: Le descrizioni comando a fumetti sono simili alle descrizioni comandi standard, ma vengono visualizzate in un fumetto \ 0034; Balloon \ 0034; con un gambo che punta allo strumento.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708668"
---
# <a name="how-to-implement-balloon-tooltips"></a>Come implementare le descrizioni comandi del fumetto

Le descrizioni comandi a fumetti sono simili alle descrizioni comandi standard, ma vengono visualizzate in un "fumetto" di tipo Cartoon con un gambo che punta allo strumento. Le descrizioni comando a fumetti possono essere a riga singola o a più righe. Vengono creati e gestiti in modo molto simile alle descrizioni comandi standard.

La posizione predefinita del gambo e del rettangolo è illustrata nella figura seguente. Se lo strumento è troppo vicino alla parte superiore dello schermo, la descrizione comando viene visualizzata sotto e a destra del rettangolo dello strumento. Se lo strumento è troppo vicino al lato destro dello schermo, vengono applicati principi simili, ma la descrizione comando viene visualizzata a sinistra del rettangolo dello strumento.

![Screenshot di una finestra di dialogo; una descrizione comando a fumetti con una riga di testo viene visualizzata sopra e a destra della destinazione](images/tt-balloon.png)

È possibile modificare il posizionamento predefinito impostando il **flag \_ CENTERTIP di ttf** nel membro **uFlags** della struttura della descrizione comando [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . In tal caso, il gambo punta normalmente al centro del bordo inferiore del rettangolo dello strumento e il rettangolo di testo viene visualizzato direttamente sotto lo strumento. Il gambo si connette al rettangolo di testo al centro del bordo superiore. Se lo strumento è troppo vicino alla parte inferiore dello schermo, il rettangolo di testo viene centrato sopra lo strumento e il gambo si connette al centro del bordo inferiore.

Nell'illustrazione seguente viene mostrata una descrizione comando centrata sullo strumento.

![Screenshot di una finestra di dialogo; una descrizione comando a fumetti con una riga di testo viene visualizzata al centro sotto la destinazione](images/tt-ballooncenter.png)

Se si vuole specificare dove si trova il punto di attacco, impostare il flag di **\_ traccia ttf** nel membro **UFlags** della struttura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Si specifica quindi la coordinata inviando un messaggio [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) con le coordinate x e y nel valore *lParam* . Se si imposta anche **ttf \_ CENTERTIP** , il gambo fa ancora riferimento alla posizione specificata dal **messaggio \_ TRACKPOSITION di TTM** .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="implement-balloon-tooltips"></a>Implementare le descrizioni comandi del fumetto

Nell'esempio di codice riportato di seguito viene illustrato come implementare una descrizione comando a fumetti centrata utilizzando lo stile del controllo ToolTip di **sintesi vocale \_** .


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> <dt>

[**Stili descrizione comando**](tooltip-styles.md)
</dt> </dl>

 

 




