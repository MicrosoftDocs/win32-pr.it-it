---
title: Disegno della finestra
description: La finestra è stata creata. A questo punto si vuole mostrare qualcosa al suo interno. Nella Windows terminologia, questa operazione è detta disegno della finestra. Per combinare metafore, una finestra è un'area di disegno vuota, in attesa di riempirla.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: 93d0cb0234975b61ee7ffc05a680b5e1e6b1e01b9d4de7235fc4239ec5573f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897019"
---
# <a name="painting-the-window"></a>Disegno della finestra

La finestra è stata creata. A questo punto si vuole mostrare qualcosa al suo interno. Nella Windows terminologia, questa operazione è detta disegno della finestra. Per combinare metafore, una finestra è un'area di disegno vuota, in attesa di riempirla.

A volte il programma avvierà il disegno per aggiornare l'aspetto della finestra. In altri casi, il sistema operativo invierà una notifica che è necessario ridisegnare una parte della finestra. In questo caso, il sistema operativo invia alla finestra un [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) La parte della finestra che deve essere disegnata è denominata *area di aggiornamento*.

La prima volta che viene visualizzata una finestra, è necessario disegnare l'intera area client della finestra. Pertanto, si riceverà sempre almeno un [**messaggio WM \_ PAINT**](/windows/desktop/gdi/wm-paint) quando si visualizza una finestra.

![Figura che mostra l'area di aggiornamento di una finestra](images/painting01.png)

L'utente è responsabile solo del disegno dell'area client. La cornice circostante, inclusa la barra del titolo, viene disegnata automaticamente dal sistema operativo. Dopo aver completato il disegno dell'area client, si cancella l'area di aggiornamento, che indica al sistema operativo che non è necessario inviare un altro messaggio [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) fino a quando non cambia qualcosa.

Si supponga ora che l'utente smuova un'altra finestra in modo da nascondere una parte della finestra. Quando la parte nascosta diventa nuovamente visibile, tale parte viene aggiunta all'area di aggiornamento e la finestra riceve un altro [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)

![Figura che mostra come cambia l'area di aggiornamento quando due finestre si sovrappongono](images/painting02.png)

L'area di aggiornamento cambia anche se l'utente estende la finestra. Nel diagramma seguente l'utente estende la finestra a destra. L'area appena esposta sul lato destro della finestra viene aggiunta all'area di aggiornamento:

![Figura che mostra come cambia l'area di aggiornamento quando viene ridimensionata una finestra](images/painting03.png)

Nel primo programma di esempio la routine di disegno è molto semplice. Riempie solo l'intera area client con un colore a tinta unita. Questo esempio è tuttavia sufficiente per illustrare alcuni dei concetti importanti.

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

Avviare l'operazione di disegno chiamando la [**funzione BeginPaint.**](/windows/desktop/api/winuser/nf-winuser-beginpaint) Questa funzione riempie la struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con informazioni sulla richiesta di ridisegno. L'area di aggiornamento corrente è specificata nel membro **rcPaint** di **PAINTSTRUCT.** Questa area di aggiornamento è definita in relazione all'area client:

![Figura che mostra l'origine dell'area client](images/painting04.png)

Nel codice di disegno sono disponibili due opzioni di base:

- Paint'intera area client, indipendentemente dalle dimensioni dell'area di aggiornamento. Tutto ciò che non rientra nell'area di aggiornamento viene ritagliato. Ciò significa che il sistema operativo lo ignora.
- Ottimizzare disegnando solo la parte della finestra all'interno dell'area di aggiornamento.

Se si disegna sempre l'intera area client, il codice sarà più semplice. Se si dispone di una logica di disegno complessa, tuttavia, può essere più efficiente ignorare le aree esterne all'area di aggiornamento.

La riga di codice seguente riempie l'area di aggiornamento con un solo colore, usando il colore di sfondo della finestra definito dal sistema (**COLOR \_ WINDOW**). Il colore effettivo indicato da **COLOR \_ WINDOW** dipende dalla combinazione di colori corrente dell'utente.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

I dettagli di [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) non sono importanti per questo esempio, ma il secondo parametro fornisce le coordinate del rettangolo da riempire. In questo caso, viene passata l'intera area di aggiornamento (il membro **rcPaint** di [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Nel primo [**messaggio WM \_ PAINT**](/windows/desktop/gdi/wm-paint) è necessario disegnare l'intera area client, quindi **rcPaint** conterrà l'intera area client. Nei messaggi **WM \_ PAINT** successivi, **rcPaint** potrebbe contenere un rettangolo più piccolo.

La [**funzione FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) fa parte del Graphics Device Interface (GDI), che ha alimentato Windows grafica per molto tempo. In Windows 7 Microsoft ha introdotto un nuovo motore di grafica, denominato Direct2D, che supporta operazioni grafiche ad alte prestazioni, ad esempio l'accelerazione hardware. Direct2D è disponibile anche per Windows Vista tramite l'aggiornamento della piattaforma [per Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) e per Windows Server 2008 tramite l'aggiornamento della piattaforma per Windows Server 2008. GDI è ancora completamente supportato.

Al termine del disegno, chiamare la [**funzione EndPaint.**](/windows/desktop/api/winuser/nf-winuser-endpaint) Questa funzione cancella l'area di aggiornamento, che segnala Windows che la finestra ha completato il disegno stesso.

## <a name="next"></a>Prossima

[Chiusura della finestra](closing-the-window.md)