---
title: Disegno della finestra
description: È stata creata la finestra. A questo punto si desidera visualizzare elementi al suo interno. Nella terminologia di Windows, questa operazione viene denominata disegno della finestra. Per combinare le metafore, una finestra è un'area di disegno vuota, in attesa del riempimento.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104565349"
---
# <a name="painting-the-window"></a>Disegno della finestra

È stata creata la finestra. A questo punto si desidera visualizzare elementi al suo interno. Nella terminologia di Windows, questa operazione viene denominata disegno della finestra. Per combinare le metafore, una finestra è un'area di disegno vuota, in attesa del riempimento.

In alcuni casi il programma avvierà il disegno per aggiornare l'aspetto della finestra. In altri casi, il sistema operativo invierà una notifica che indica che è necessario ridisegnare una parte della finestra. In tal caso, il sistema operativo invia alla finestra un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . La parte della finestra che deve essere disegnata è denominata *area di aggiornamento*.

La prima volta che viene visualizzata una finestra, è necessario disegnare l'intera area client della finestra. Pertanto, quando si visualizza una finestra, viene sempre visualizzato almeno un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .

![illustrazione che mostra l'area di aggiornamento di una finestra](images/painting01.png)

L'utente è responsabile solo del disegno dell'area client. Il frame circostante, inclusa la barra del titolo, viene automaticamente disegnato dal sistema operativo. Dopo aver completato il disegno dell'area client, deselezionare l'area di aggiornamento, che indica al sistema operativo che non è necessario inviare un altro messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) fino a quando qualcosa non cambia.

Si supponga ora che l'utente sposti un'altra finestra in modo che nasconda una parte della finestra. Quando la parte nascosta diventa nuovamente visibile, tale parte viene aggiunta all'area di aggiornamento e la finestra riceve un altro messaggio [**di \_ disegno WM**](/windows/desktop/gdi/wm-paint) .

![illustrazione che Mostra come cambia l'area di aggiornamento quando si sovrappongono due finestre](images/painting02.png)

L'area di aggiornamento cambia anche se l'utente allunga la finestra. Nel diagramma seguente l'utente allunga la finestra a destra. L'area appena esposta sul lato destro della finestra viene aggiunta all'area di aggiornamento:

![illustrazione che Mostra come cambia l'area di aggiornamento quando una finestra viene ridimensionata](images/painting03.png)

Nel primo programma di esempio, la routine di disegno è molto semplice. Riempie semplicemente l'intera area client con un colore a tinta unita. Questo esempio è ancora sufficiente per illustrare alcuni concetti importanti.

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

Avviare l'operazione di disegno chiamando la funzione [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) . Questa funzione compila la struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con le informazioni sulla richiesta di ridisegno. L'area di aggiornamento corrente viene specificata nel membro **rcPaint** di **PAINTSTRUCT**. Questa area di aggiornamento è definita in relazione all'area client:

![illustrazione che mostra l'origine dell'area client](images/painting04.png)

Nel codice di disegno sono disponibili due opzioni di base:

- Disegnare l'intera area client, indipendentemente dalle dimensioni dell'area di aggiornamento. Qualsiasi elemento che esula dall'area di aggiornamento viene troncato. Ovvero, il sistema operativo lo ignora.
- Ottimizzare disegnando solo la parte della finestra all'interno dell'area di aggiornamento.

Se si dipinge sempre l'intera area client, il codice sarà più semplice. Se la logica di disegno è complessa, tuttavia, può essere più efficiente ignorare le aree all'esterno dell'area di aggiornamento.

La riga di codice seguente riempie l'area di aggiornamento con un solo colore, usando il colore di sfondo della finestra definito dal sistema (**\_ finestra dei colori**). Il colore effettivo indicato dalla **\_ finestra colore** dipende dalla combinazione di colori corrente dell'utente.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

I dettagli di [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) non sono importanti per questo esempio, ma il secondo parametro fornisce le coordinate del rettangolo da riempire. In questo caso, viene passata l'intera area di aggiornamento (il membro **rcPaint** di [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Nel primo messaggio [**di \_ disegno WM**](/windows/desktop/gdi/wm-paint) , l'intera area client deve essere disegnata, quindi **rcPaint** conterrà l'intera area client. Nei successivi messaggi di **\_ disegno WM** , **rcPaint** potrebbe contenere un rettangolo più piccolo.

La funzione [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) fa parte del Graphics Device Interface (GDI), che ha alimentato la grafica di Windows per un lungo periodo di tempo. In Windows 7, Microsoft ha introdotto un nuovo motore di grafica, denominato Direct2D, che supporta operazioni grafiche a prestazioni elevate, ad esempio l'accelerazione hardware. Direct2D è inoltre disponibile per Windows Vista tramite l' [aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) e per windows Server 2008 tramite l'aggiornamento della piattaforma per windows Server 2008. GDI è ancora completamente supportato.

Al termine del disegno, chiamare la funzione [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) . Questa funzione Cancella l'area di aggiornamento, che segnala a Windows che la finestra ha completato il disegno.

## <a name="next"></a>Prossima

[Chiusura della finestra](closing-the-window.md)