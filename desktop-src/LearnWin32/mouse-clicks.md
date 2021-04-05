---
title: Risposta ai clic del mouse
description: Risposta ai clic del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117730"
---
# <a name="responding-to-mouse-clicks"></a>Risposta ai clic del mouse

Se l'utente fa clic su un pulsante del mouse mentre il cursore si trova sull'area client di una finestra, la finestra riceve uno dei messaggi seguenti.



| Messaggio                                        | Significato                   |
|------------------------------------------------|---------------------------|
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Pulsante sinistro          |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)     | Pulsante a sinistra in alto            |
| [**\_MBUTTONDOWN WM**](/windows/desktop/inputdev/wm-mbuttondown) | Pulsante centrale verso il basso        |
| [**\_MBUTTONUP WM**](/windows/desktop/inputdev/wm-mbuttonup)     | Pulsante centrale          |
| [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown) | Pulsante destro verso il basso         |
| [**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)     | Pulsante destro su           |
| [**\_XBUTTONDOWN WM**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 o XBUTTON2 |
| [**\_XBUTTONUP WM**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 o XBUTTON2   |



 

Si ricordi che l'area client è la parte della finestra che esclude il frame. Per ulteriori informazioni sulle aree client, vedere [che cos'è una finestra?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordinate del mouse

In tutti questi messaggi, il parametro *lParam* contiene le coordinate x e y del puntatore del mouse. I 16 bit più bassi di *lParam* contengono la coordinata x e i successivi 16 bit contengono la coordinata y. Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per decomprimere le coordinate da *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Queste macro sono definite nel file di intestazione WindowsX. h.

In Windows a 64 bit, *lParam* è un valore a 64 bit. Non vengono usati i bit 32 superiori di *lParam* . Nella documentazione di MSDN sono menzionati la "parola di basso livello" e la "parola più ordinata" di *lParam*. Nel caso di 64 bit, ciò significa che le parole di ordine inferiore e superiore dei 32 bit inferiori. Le macro estraggono i valori corretti, quindi se vengono usati, si sarà sicuri.

Le coordinate del mouse sono espresse in pixel, non in pixel indipendenti dal dispositivo (DIP) e vengono misurate in relazione all'area client della finestra. Le coordinate sono valori con segno. Le posizioni sopra e a sinistra dell'area client presentano coordinate negative, che è importante se si tiene traccia della posizione del mouse all'esterno della finestra. Si vedrà come eseguire questa operazione in un argomento successivo, [acquisendo lo spostamento del mouse all'esterno della finestra](mouse-movement.md).

### <a name="additional-flags"></a>Flag aggiuntivi

Il parametro *wParam* contiene un operatore OR bit per bit di flag, che indica lo stato degli altri **pulsanti del mouse** oltre ai tasti MAIUSC e CTRL.



| Contrassegno             | Significato                          |
|------------------|----------------------------------|
| **MK ( \_ controllo)**  | Il tasto CTRL è premuto.            |
| **\_LBUTTON MK**  | Il pulsante sinistro del mouse è premuto.   |
| **\_MBUTTON MK**  | Il pulsante centrale del mouse è inattivo. |
| **\_RBUTTON MK**  | Il pulsante destro del mouse è inattivo.  |
| **\_turno MK**    | Il tasto MAIUSC è premuto.           |
| **\_XBUTTON1 MK** | Il pulsante XBUTTON1 è inattivo.     |
| **\_XBUTTON2 MK** | Il pulsante XBUTTON2 è inattivo.     |



 

L'assenza di un flag indica che non è stato premuto il pulsante o la chiave corrispondente. Ad esempio, per verificare se il tasto CTRL è inattivo:


```C++
if (wParam & MK_CONTROL) { ...
```



Se è necessario trovare lo stato di altre chiavi oltre a CTRL e MAIUSC, usare la funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , descritta in input da [tastiera](keyboard-input.md).

I messaggi della finestra [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) e [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) si applicano sia a XBUTTON1 che a XBUTTON2. Il parametro *wParam* indica il pulsante su cui è stato fatto clic.


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>Doppio clic

Per impostazione predefinita, una finestra non riceve notifiche di doppio clic. Per ricevere i doppi clic, impostare il flag **cs \_ DBLCLKS** nella struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) quando si registra la classe Window.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Se si imposta il flag **cs \_ DBLCLKS** come illustrato, la finestra riceverà le notifiche di doppio clic. Un doppio clic è indicato da un messaggio della finestra con "DBLCLK" nel nome. Ad esempio, un doppio clic sul pulsante sinistro del mouse produce la seguente sequenza di messaggi:

<dl>

[**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)  
[**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)  
[**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

In effetti, il secondo messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) che verrebbe normalmente generato diventa un messaggio [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) . I messaggi equivalenti vengono definiti per i pulsanti right, Middle e XBUTTON.

Fino a quando non si riceve il messaggio di doppio clic, non esiste alcun modo per indicare che il primo clic del mouse è l'inizio di un doppio clic. Pertanto, un'azione di doppio clic deve continuare un'azione che inizia con il primo clic del mouse. Nella shell di Windows, ad esempio, un singolo clic Seleziona una cartella, mentre un doppio clic apre la cartella.

## <a name="non-client-mouse-messages"></a>Messaggi del mouse non client

Per gli eventi del mouse che si verificano all'interno dell'area non client della finestra viene definito un set separato di messaggi. Questi messaggi contengono le lettere "NC" nel nome. Ad esempio, [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) è l'equivalente non client di [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Una tipica applicazione non intercetta questi messaggi perché la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gestisce correttamente questi messaggi. Tuttavia, possono essere utili per alcune funzioni avanzate. Ad esempio, è possibile usare questi messaggi per implementare un comportamento personalizzato nella barra del titolo. Se si gestiscono questi messaggi, è in genere necessario passarli a **DefWindowProc** in seguito. In caso contrario, l'applicazione interrompe le funzionalità standard, ad esempio il trascinamento o la riduzione a icona della finestra.

## <a name="next"></a>Prossima

[Spostamento del mouse](mouse-movement.md)

 

 