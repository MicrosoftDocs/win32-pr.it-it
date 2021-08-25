---
title: Risposta ai clic del mouse
description: Risposta ai clic del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947b50726e79fbf29c4f013d4ac0a449c009c1817b74b1a8063e63a68c4dd6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897211"
---
# <a name="responding-to-mouse-clicks"></a>Risposta ai clic del mouse

Se l'utente fa clic su un pulsante del mouse mentre il cursore è posizionato sull'area client di una finestra, la finestra riceve uno dei messaggi seguenti.



| Messaggio                                        | Significato                   |
|------------------------------------------------|---------------------------|
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Pulsante sinistro verso il basso          |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | Pulsante sinistro in alto            |
| [**WM \_ MBUTTONDOWN**](/windows/desktop/inputdev/wm-mbuttondown) | Pulsante centrale in basso        |
| [**WM \_ MBUTTONUP**](/windows/desktop/inputdev/wm-mbuttonup)     | Pulsante centrale in alto          |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown) | Pulsante destro verso il basso         |
| [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)     | Pulsante destro in alto           |
| [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 o XBUTTON2 in basso |
| [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 o XBUTTON2 up   |



 

Ricordare che l'area client è la parte della finestra che esclude il frame. Per altre informazioni sulle aree client, vedere [Che cos'è una finestra?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordinate del mouse

In tutti questi messaggi il parametro *lParam* contiene le coordinate x e y del puntatore del mouse. I 16 bit più bassi di *lParam* contengono la coordinata x e i 16 bit successivi contengono la coordinata y. Usare le macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per decomprimere le coordinate da *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Queste macro sono definite nel file di intestazione WindowsX.h.

In caso di errore Windows a 64 bit, *lParam* è un valore a 64 bit. I 32 bit superiori di *lParam* non vengono usati. La documentazione MSDN cita la "parola di ordine basso" e la "parola di ordine superiore" di *lParam*. Nel caso a 64 bit, ciò significa le parole di ordine inferiore e superiore dei 32 bit inferiori. Le macro estraggono i valori appropriati, quindi se li si usa, si sarà sicuri.

Le coordinate del mouse sono espresse in pixel, non in DIP (Device Independent Pixel) e vengono misurate in relazione all'area client della finestra. Le coordinate sono valori con segno. Le posizioni sopra e a sinistra dell'area client hanno coordinate negative, aspetto importante se si tiene traccia della posizione del mouse all'esterno della finestra. Questa operazione verrà illustrata in un argomento successivo, Acquisizione dello spostamento [del mouse all'esterno della finestra.](mouse-movement.md)

### <a name="additional-flags"></a>Flag aggiuntivi

Il *parametro wParam* contiene **un'operazione OR** bit per bit di flag, che indica lo stato degli altri pulsanti del mouse più i tasti MAIUSC e CTRL.



| Contrassegno             | Significato                          |
|------------------|----------------------------------|
| **CONTROLLO \_ MK**  | Il tasto CTRL è premuto.            |
| **MK \_ LBUTTON**  | Il pulsante sinistro del mouse è in basso.   |
| **MK \_ MBUTTON**  | Il pulsante centrale del mouse è in basso. |
| **MK \_ RBUTTON**  | Il pulsante destro del mouse è in basso.  |
| **MK \_ SHIFT**    | Il tasto MAIUSC è premuto.           |
| **MK \_ XBUTTON1** | Il pulsante XBUTTON1 non è disponibile.     |
| **MK \_ XBUTTON2** | Il pulsante XBUTTON2 è in basso.     |



 

L'assenza di un flag indica che il pulsante o il tasto corrispondente non è stato premuto. Ad esempio, per verificare se il tasto CTRL è premuto:


```C++
if (wParam & MK_CONTROL) { ...
```



Se è necessario trovare lo stato di altri tasti oltre a CTRL e MAIUSC, usare la [**funzione GetKeyState,**](/windows/desktop/api/winuser/nf-winuser-getkeystate) descritta in [Input da tastiera.](keyboard-input.md)

I [**messaggi della finestra WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) e [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) si applicano sia a XBUTTON1 che a XBUTTON2. Il *parametro wParam* indica il pulsante su cui è stato fatto clic.


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

Per impostazione predefinita, una finestra non riceve notifiche con doppio clic. Per ricevere i doppio clic, impostare il flag **\_ CS DBLCLKS** nella [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) quando si registra la classe della finestra.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Se si imposta il flag **\_ CS DBLCLKS** come illustrato, la finestra riceverà notifiche con doppio clic. Un doppio clic è indicato da un messaggio della finestra con "DBLCLK" nel nome. Ad esempio, un doppio clic sul pulsante sinistro del mouse produce la sequenza di messaggi seguente:

<dl>

[**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
[**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

In effetti, il secondo [**messaggio \_ LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) che normalmente verrebbe generato diventa un [**messaggio WM \_ LBUTTONDBLCLK.**](/windows/desktop/inputdev/wm-lbuttondblclk) I messaggi equivalenti sono definiti per i pulsanti destro, centrale e XBUTTON.

Fino a quando non viene visualizzato il messaggio di doppio clic, non è possibile indicare che il primo clic del mouse è l'inizio di un doppio clic. Pertanto, un'azione con doppio clic deve continuare un'azione che inizia con il primo clic del mouse. Ad esempio, nella shell Windows, un singolo clic seleziona una cartella, mentre un doppio clic apre la cartella.

## <a name="non-client-mouse-messages"></a>Messaggi del mouse non client

Viene definito un set separato di messaggi per gli eventi del mouse che si verificano all'interno dell'area non client della finestra. Questi messaggi hanno le lettere "NC" nel nome. Ad esempio, [**WM \_ NCLBUTTONDOWN è**](/windows/desktop/inputdev/wm-nclbuttondown) l'equivalente non client di WM [**\_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown) Un'applicazione tipica non intercetterà questi messaggi, perché la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gestisce correttamente questi messaggi. Tuttavia, possono essere utili per determinate funzioni avanzate. Ad esempio, è possibile usare questi messaggi per implementare il comportamento personalizzato nella barra del titolo. Se si gestiscono questi messaggi, in genere è consigliabile passarli a **DefWindowProc in un secondo** momento. In caso contrario, l'applicazione interromperà le funzionalità standard, ad esempio il trascinamento o la riduzione a icona della finestra.

## <a name="next"></a>Prossima

[Spostamento del mouse](mouse-movement.md)

 

 