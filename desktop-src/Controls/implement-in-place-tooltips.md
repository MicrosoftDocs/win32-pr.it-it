---
title: Come implementare In-Place descrizioni comandi
description: Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati. Per un'illustrazione, vedere informazioni sui controlli ToolTip.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047622"
---
# <a name="how-to-implement-in-place-tooltips"></a>Come implementare In-Place descrizioni comandi

Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati. Per un'illustrazione, vedere [informazioni sui controlli ToolTip](tooltip-controls.md).

La differenza tra le descrizioni comandi ordinarie e quelle sul posto è il posizionamento. Per impostazione predefinita, quando il puntatore del mouse viene posizionato su un'area a cui è associata una descrizione comando, la descrizione comando viene visualizzata accanto all'area. Tuttavia, le descrizioni comandi sono finestre e possono essere posizionate in qualsiasi punto in cui si sceglie chiamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). La creazione di una descrizione comando sul posto consiste nel posizionare la finestra della descrizione comando in modo da sovrapporre la stringa di testo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="positioning-an-in-place-tooltip"></a>Posizionamento di una descrizione comando In-Place

È necessario tenere traccia di tre rettangoli quando si posiziona una descrizione comando sul posto:

1.  Rettangolo che racchiude il testo completo dell'etichetta.
2.  Rettangolo che racchiude il testo della descrizione comando. Il testo della descrizione comando è identico al testo dell'etichetta completo e, in genere, ha le stesse dimensioni e il tipo di carattere. In genere, i due rettangoli di testo hanno le stesse dimensioni.
3.  Rettangolo della finestra della descrizione comando. Questo rettangolo è leggermente più grande del rettangolo di testo della descrizione comando che racchiude.


I tre rettangoli vengono visualizzati schematicamente nella figura seguente. La parte nascosta del testo dell'etichetta è indicata da uno sfondo grigio.

![diagramma che mostra una stringa lunga, metà delle quali ha uno sfondo grigio, quindi la stessa stringa all'interno di un rettangolo della finestra della descrizione comando più grande](images/inplace.png)

Per creare una descrizione comando sul posto, è necessario posizionare il rettangolo del testo della descrizione comando in modo che sovrimpressione il rettangolo del testo dell'etichetta. La procedura per allineare i due rettangoli è relativamente semplice:

1.  Definire il rettangolo del testo dell'etichetta.
2.  Posizionare la finestra della descrizione comando in modo che il rettangolo del testo della descrizione comandi sovrapposto al rettangolo del testo dell'etichetta.


In pratica, è in genere sufficiente allineare l'angolo superiore sinistro dei due rettangoli di testo. Il tentativo di ridimensionare il rettangolo testo della descrizione comando in modo che corrisponda esattamente al rettangolo del testo dell'etichetta può causare problemi con la visualizzazione della descrizione comando.

Il problema con questo semplice schema è che non è possibile posizionare direttamente il rettangolo del testo della descrizione comando. Al contrario, è necessario posizionare il rettangolo della finestra della descrizione comando abbastanza a lungo e a sinistra del rettangolo di testo dell'etichetta in modo che gli angoli dei due rettangoli di testo coincidano. In altre parole, è necessario essere a conoscenza dell'offset tra il rettangolo della finestra della descrizione comando e il rettangolo del testo racchiuso. In generale, non esiste un modo semplice per determinare questo offset.

### <a name="implement-in-place-tooltips"></a>Implementare descrizioni comando In-Place

Il frammento di codice seguente illustra come usare un messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) in un gestore di visualizzazione [TTN \_](ttn-show.md) per visualizzare una descrizione comando sul posto. L'applicazione indica che il testo dell'etichetta viene troncato impostando la variabile *fMyStringIsTruncated* privata su **true**. Il gestore chiama una funzione definita dall'applicazione, **GetMyItemRect**, per recuperare il rettangolo del testo dell'etichetta. Questo rettangolo viene passato al controllo ToolTip con **TTM \_ ADJUSTRECT**, che restituisce il rettangolo della finestra corrispondente. [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) viene quindi chiamato per posizionare la descrizione comando sull'etichetta.


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



In questo esempio non viene modificata la dimensione della descrizione comando, bensì solo la relativa posizione. I due rettangoli di testo sono allineati negli angoli in alto a sinistra, ma non necessariamente con le stesse dimensioni. In pratica, la differenza è di solito ridotta e questo approccio è consigliato per la maggior parte degli scopi. Sebbene sia possibile, in linea di principio, usare [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per ridimensionare e riposizionare la descrizione comando, in questo modo potrebbe avere conseguenze imprevedibili.

## <a name="remarks"></a>Commenti

Controlli comuni [versione 5,80](common-control-versions.md) semplifica l'uso di descrizioni comando sul posto mediante l'aggiunta di un nuovo messaggio, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md). Inviare questo messaggio con le coordinate del rettangolo di testo dell'etichetta che si desidera sovrapporre alla descrizione comando e restituisce le coordinate di un rettangolo della finestra di descrizione comando posizionato in modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 