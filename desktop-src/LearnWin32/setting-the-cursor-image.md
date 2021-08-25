---
title: Impostazione dell'immagine del cursore
description: Impostazione dell'immagine del cursore
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4723289155bc7898f6f49e188ad972ca152332c82994b57c79af493c8fe6b572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896911"
---
# <a name="setting-the-cursor-image"></a>Impostazione dell'immagine del cursore

Il *cursore* è l'immagine piccola che mostra la posizione del mouse o di un altro dispositivo di puntamento. Molte applicazioni modificano l'immagine del cursore per inviare commenti e suggerimenti all'utente. Anche se non è obbligatorio, aggiunge un po' di smalto all'applicazione.

Windows fornisce un set di immagini di cursori standard, denominate *cursori di sistema.* Questi includono la freccia, la mano, il raggio a I, la clessidra (che ora è un cerchio rotante) e altri. Questa sezione descrive come usare i cursori di sistema. Per attività più avanzate, ad esempio la creazione di cursori personalizzati, vedere [Cursori](/windows/desktop/menurc/cursors).

È possibile associare un cursore a una classe finestra impostando il membro **hCursor** della [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) [**o WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) In caso contrario, il cursore predefinito è la freccia. Quando il mouse viene spostato su una finestra, la finestra riceve un [**messaggio WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) (a meno che il mouse non sia stato acquisito da un'altra finestra). A questo punto, si verifica uno degli eventi seguenti:

-   L'applicazione imposta il cursore e la routine della finestra restituisce **TRUE.**
-   L'applicazione non esegue alcuna operazione e [**passa WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Per impostare il cursore, un programma esegue le operazioni seguenti:

1.  Chiama [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) per caricare il cursore in memoria. Questa funzione restituisce un handle per il cursore.
2.  Chiama [**SetCursor e**](/windows/desktop/api/winuser/nf-winuser-setcursor) passa l'handle del cursore.

In caso contrario, se l'applicazione passa [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la **funzione DefWindowProc** usa l'algoritmo seguente per impostare l'immagine del cursore:

1.  Se la finestra ha un elemento padre, inoltrare il [**messaggio WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) all'elemento padre da gestire.
2.  In caso contrario, se la finestra include un cursore di classe, impostare il cursore sul cursore della classe.
3.  Se non è presente alcun cursore di classe, impostare il cursore sul cursore a freccia.

La [**funzione LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) può caricare un cursore personalizzato da una risorsa o uno dei cursori di sistema. Nell'esempio seguente viene illustrato come impostare il cursore sul cursore della mano di sistema.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Se si modifica il cursore, l'immagine del cursore viene reimpostata al successivo spostamento del mouse, a meno che non si intercetti il messaggio [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) e si imposta di nuovo il cursore. Il codice seguente illustra come gestire **WM \_ SETCURSOR**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Questo codice controlla innanzitutto i 16 bit inferiori di *lParam*. Se `LOWORD(lParam)` è uguale a **HTCLIENT,** significa che il cursore si trova sull'area client della finestra. In caso contrario, il cursore si trova sull'area non client. In genere, è consigliabile impostare solo il cursore per l'area client e Windows impostare il cursore per l'area non client.

## <a name="next"></a>Prossima

[Input utente: esempio esteso](user-input--extended-example.md)

 

 