---
title: Come implementare le descrizioni In-Place comando
description: Le descrizioni comando sul posto vengono usate per visualizzare stringhe di testo per gli oggetti ritagliati. Per un'illustrazione, vedere Informazioni sui controlli descrizione comando.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd3b01d30a20b52cbb80121cc8c1d793965acf0ea3cf4f2be1ce4553f4ccb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671730"
---
# <a name="how-to-implement-in-place-tooltips"></a>Come implementare le descrizioni In-Place comando

Le descrizioni comando sul posto vengono usate per visualizzare stringhe di testo per gli oggetti ritagliati. Per un'illustrazione, vedere [Informazioni sui controlli descrizione comando.](tooltip-controls.md)

La differenza tra le descrizioni comando ordinarie e sul posto è il posizionamento. Per impostazione predefinita, quando il puntatore del mouse passa su un'area a cui è associata una descrizione comando, la descrizione comando viene visualizzata accanto all'area. Tuttavia, le descrizioni comando sono finestre e possono essere posizionate in qualsiasi punto scelto chiamando [**SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) La creazione di una descrizione comando sul posto è una questione di posizionamento della finestra della descrizione comando in modo da sovrapporre la stringa di testo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="positioning-an-in-place-tooltip"></a>Posizionamento di una descrizione In-Place comando

È necessario tenere traccia di tre rettangoli quando si posiziona una descrizione comando sul posto:

1.  Rettangolo che circonda il testo completo dell'etichetta.
2.  Rettangolo che circonda il testo della descrizione comando. Il testo della descrizione comando è identico al testo completo dell'etichetta e in genere ha le stesse dimensioni e lo stesso tipo di carattere. I due rettangoli di testo saranno quindi in genere delle stesse dimensioni.
3.  Rettangolo della finestra della descrizione comando. Questo rettangolo è leggermente più grande del rettangolo di testo della descrizione comando che racchiude.


I tre rettangoli sono illustrati schematicamente nella figura seguente. La parte nascosta del testo dell'etichetta è indicata da uno sfondo grigio.

![diagramma che mostra una stringa lunga, metà delle quali ha uno sfondo grigio, quindi la stessa stringa all'interno di un rettangolo più grande della finestra della descrizione comando](images/inplace.png)

Per creare una descrizione comando sul posto, è necessario posizionare il rettangolo di testo della descrizione comando in modo che si sovrappone al rettangolo di testo dell'etichetta. La procedura per allineare i due rettangoli è relativamente semplice:

1.  Definire il rettangolo di testo dell'etichetta.
2.  Posizionare la finestra della descrizione comando in modo che il rettangolo di testo della descrizione comando si sovrappone al rettangolo di testo dell'etichetta.


In pratica, è in genere sufficiente allineare l'angolo superiore sinistro dei due rettangoli di testo. Il tentativo di ridimensionare il rettangolo di testo della descrizione comando in modo che corrisponda esattamente al rettangolo di testo dell'etichetta può causare problemi con la visualizzazione della descrizione comando.

Il problema di questo semplice schema è che non è possibile posizionare direttamente il rettangolo di testo della descrizione comando. È invece necessario posizionare il rettangolo della finestra della descrizione comando appena sopra e a sinistra del rettangolo di testo dell'etichetta in modo che gli angoli dei due rettangoli di testo coincidano. In altre parole, è necessario conoscere l'offset tra il rettangolo della finestra della descrizione comando e il rettangolo di testo racchiuso. In generale, non esiste un modo semplice per determinare questo offset.

### <a name="implement-in-place-tooltips"></a>Implementare In-Place comando

Il frammento di codice seguente illustra come usare un messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) in un gestore [TTN \_ SHOW](ttn-show.md) per visualizzare una descrizione comando sul posto. L'applicazione indica che il testo dell'etichetta viene troncato impostando la variabile *privata fMyStringIsTruncated* su **TRUE.** Il gestore chiama una funzione definita dall'applicazione, **GetMyItemRect,** per recuperare il rettangolo di testo dell'etichetta. Questo rettangolo viene passato al controllo descrizione comando con **TTM \_ ADJUSTRECT,** che restituisce il rettangolo della finestra corrispondente. [**SetWindowPos viene quindi**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) chiamato per posizionare la descrizione comando sull'etichetta.


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



Questo esempio non modifica le dimensioni della descrizione comando, ma solo la posizione. I due rettangoli di testo sono allineati agli angoli superiore sinistro, ma non necessariamente con le stesse dimensioni. In pratica, la differenza è in genere ridotta e questo approccio è consigliato per la maggior parte degli scopi. Sebbene sia possibile, in linea di principio, usare [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per ridimensionare e riposizionare la descrizione comando, questa operazione potrebbe avere conseguenze imprevedibili.

## <a name="remarks"></a>Commenti

I controlli [comuni versione 5.80](common-control-versions.md) semplificano l'uso delle descrizioni comando sul posto grazie all'aggiunta di un nuovo messaggio, [**TTM \_ ADJUSTRECT.**](ttm-adjustrect.md) Inviare questo messaggio con le coordinate del rettangolo di testo dell'etichetta che si vuole sovrapporre alla descrizione comando e restituisce le coordinate di un rettangolo della finestra della descrizione comando posizionato in modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli descrizione comando](using-tooltip-contro.md)
</dt> </dl>

 

 