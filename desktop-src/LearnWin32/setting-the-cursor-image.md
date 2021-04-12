---
title: Impostazione dell'immagine del cursore
description: Impostazione dell'immagine del cursore
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472894"
---
# <a name="setting-the-cursor-image"></a>Impostazione dell'immagine del cursore

Il *cursore* è l'immagine piccola che mostra la posizione del mouse o di un altro dispositivo di puntamento. Molte applicazioni modificano l'immagine del cursore per fornire commenti e suggerimenti all'utente. Sebbene non sia obbligatorio, aggiunge un bel po' di smalto all'applicazione.

Windows fornisce un set di immagini di cursore standard, denominate *cursori di sistema*. Sono inclusi la freccia, la mano, l'i-Beam, la clessidra (che è ora un cerchio rotante) e altre. In questa sezione viene descritto come utilizzare i cursori di sistema. Per attività più avanzate, ad esempio la creazione di cursori personalizzati, vedere [cursori](/windows/desktop/menurc/cursors).

È possibile associare un cursore a una classe della finestra impostando il membro **hCursor** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . In caso contrario, il cursore predefinito è la freccia. Quando il mouse viene spostato su una finestra, la finestra riceve un messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) (a meno che un'altra finestra non abbia acquisito il mouse). A questo punto si verifica uno degli eventi seguenti:

-   L'applicazione imposta il cursore e la routine della finestra restituisce **true**.
-   L'applicazione non esegue alcuna operazione e passa il [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Per impostare il cursore, un programma esegue le operazioni seguenti:

1.  Chiama [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) per caricare il cursore in memoria. Questa funzione restituisce un handle per il cursore.
2.  Chiama il [**cursore**](/windows/desktop/api/winuser/nf-winuser-setcursor) e passa l'handle del cursore.

In caso contrario, se l'applicazione passa il [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la funzione **DefWindowProc** usa l'algoritmo seguente per impostare l'immagine del cursore:

1.  Se la finestra dispone di un elemento padre, inviare il messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) al padre da gestire.
2.  In caso contrario, se la finestra dispone di un cursore della classe, impostare il cursore sul cursore della classe.
3.  Se non è presente alcun cursore della classe, impostare il cursore sul cursore a freccia.

La funzione [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) può caricare un cursore personalizzato da una risorsa o uno dei cursori di sistema. Nell'esempio seguente viene illustrato come impostare il cursore sul cursore della mano di sistema.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Se si modifica il cursore, l'immagine del cursore viene reimpostata al successivo spostamento del mouse, a meno che non venga intercettato il messaggio del cursore [**WM \_**](/windows/desktop/menurc/wm-setcursor) e il cursore non venga impostato di nuovo. Nel codice seguente viene illustrato come gestire **il \_ secursore WM**.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Questo codice controlla prima di tutto i 16 bit inferiori di *lParam*. Se è `LOWORD(lParam)` uguale a **HTCLIENT**, significa che il cursore si trova sull'area client della finestra. In caso contrario, il cursore si trova sull'area non client. In genere, è consigliabile impostare solo il cursore per l'area client e lasciare che Windows imposti il cursore per l'area non client.

## <a name="next"></a>Prossima

[Input utente: esempio esteso](user-input--extended-example.md)

 

 