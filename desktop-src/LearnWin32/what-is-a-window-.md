---
title: Che cos'è una finestra
description: .
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fcbba817e3e4c9059340d0a67c7170f4583270c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398914"
---
# <a name="what-is-a-window"></a>Che cos'è una finestra?

## <a name="what-is-a-window"></a>Che cos'è una finestra?

Ovviamente, Windows è fondamentale per Windows. Sono così importanti che hanno denominato il sistema operativo dopo di essi. Ma che cos'è una finestra? Quando si pensa a una finestra, è probabile che si pensi a qualcosa di simile al seguente:

![screenshot della finestra di un'applicazione](images/window01.png)

Questo tipo di finestra viene chiamato finestra *dell'applicazione* o *finestra principale*. Include in genere un frame con una barra del titolo, i pulsanti **Riduci a icona** e **Ingrandisci** e altri elementi dell'interfaccia utente standard. Il frame viene chiamato *area non client* della finestra, quindi viene chiamato perché il sistema operativo gestisce la parte della finestra. L'area all'interno del frame è l' *area client*. Si tratta della parte della finestra gestita dal programma.

Di seguito è riportato un altro tipo di finestra:

![Screenshot di una finestra di controllo](images/window02.png)

Se non si ha familiarità con la programmazione Windows, è possibile che i controlli dell'interfaccia utente, ad esempio i pulsanti e le caselle di modifica, siano a loro volta Windows. La differenza principale tra un controllo dell'interfaccia utente e una finestra dell'applicazione è che un controllo non esiste autonomamente. Il controllo viene invece posizionato in relazione alla finestra dell'applicazione. Quando si trascina la finestra dell'applicazione, il controllo viene spostato, come previsto. Inoltre, il controllo e la finestra dell'applicazione possono comunicare tra loro. Ad esempio, la finestra dell'applicazione riceve notifiche di clic da un pulsante.

Pertanto, quando si pensa alla *finestra*, non è sufficiente pensare alla *finestra dell'applicazione*. Si pensi invece a una finestra come costrutto di programmazione che:

-   Occupa una determinata parte dello schermo.
-   Potrebbe non essere visibile in un determinato momento.
-   Sa come creare se stesso.
-   Risponde agli eventi dell'utente o del sistema operativo.

## <a name="parent-windows-and-owner-windows"></a>Finestre padre e finestre proprietarie

Nel caso di un controllo dell'interfaccia utente, la finestra di controllo è detta *figlio* della finestra dell'applicazione. La finestra dell'applicazione è l' *elemento padre* della finestra del controllo. La finestra padre fornisce il sistema di coordinate usato per il posizionamento di una finestra figlio. La presenza di una finestra padre influiscono sugli aspetti dell'aspetto di una finestra; ad esempio, una finestra figlio viene ritagliata in modo che nessuna parte della finestra figlio possa apparire all'esterno dei bordi della finestra padre.

Un'altra relazione è la relazione tra una finestra dell'applicazione e una finestra di dialogo modale. Quando in un'applicazione viene visualizzata una finestra di dialogo modale, la finestra dell'applicazione è la finestra *proprietaria* e la finestra di dialogo è una finestra di *Proprietà* . Una finestra di proprietà viene sempre visualizzata davanti alla finestra proprietaria. Viene nascosta quando il proprietario è ridotto a icona e viene eliminato allo stesso tempo del proprietario.

Nell'immagine seguente viene illustrata un'applicazione che visualizza una finestra di dialogo con due pulsanti:

![Screenshot di un'applicazione con una finestra di dialogo](images/window03.png)

La finestra dell'applicazione è proprietaria della finestra di dialogo e la finestra di dialogo è l'elemento padre di entrambe le finestre dei pulsanti. Il diagramma seguente illustra le relazioni seguenti:

![illustrazione che Mostra relazioni padre/figlio e proprietario/proprietà](images/window04.png)

## <a name="window-handles"></a>Handle di finestra

Windows sono oggetti, che hanno sia codice che dati, ma non sono classi C++. Al contrario, un programma fa riferimento a una finestra usando un valore denominato *handle*. Un handle è un tipo opaco. Essenzialmente, si tratta semplicemente di un numero usato dal sistema operativo per identificare un oggetto. È possibile immaginare le finestre con una tabella di grandi dimensioni di tutte le finestre create. Usa questa tabella per cercare Windows in base ai relativi handle. Se è esattamente il modo in cui funziona internamente non è importante. Il tipo di dati per gli handle di finestra è **HWND**, che in genere si pronuncia "Alf-Wind". Gli handle di finestra vengono restituiti dalle funzioni che creano Windows: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) e [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

Per eseguire un'operazione in una finestra, in genere viene chiamata una funzione che accetta un valore **HWND** come parametro. Ad esempio, per riposizionare una finestra sullo schermo, chiamare la funzione [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) :


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Il primo parametro è l'handle della finestra che si desidera spostare. Gli altri parametri specificano il nuovo percorso della finestra e indica se la finestra deve essere ridisegnato.

Tenere presente che gli handle non sono puntatori. Se *HWND* è una variabile che contiene un handle, il tentativo di dereferenziare l'handle scrivendo `*hwnd` è un errore.

## <a name="screen-and-window-coordinates"></a>Coordinate dello schermo e della finestra

Le coordinate sono misurate in pixel indipendenti dal dispositivo. Verranno fornite altre informazioni sulla parte indipendente dal *dispositivo* dei *pixel indipendenti dal dispositivo* quando si discute la grafica.

A seconda dell'attività, è possibile misurare le coordinate relative allo schermo rispetto a una finestra (incluso il frame) o relativa all'area client di una finestra. È ad esempio possibile posizionare una finestra sullo schermo usando le coordinate dello schermo, ma è possibile creare una finestra usando le coordinate client. In ogni caso, l'origine (0, 0) è sempre l'angolo superiore sinistro dell'area.

![illustrazione che mostra le coordinate dello schermo, della finestra e del client](images/coordinates01.png)

## <a name="next"></a>Prossima

[WinMain: punto di ingresso dell'applicazione](winmain--the-application-entry-point.md)

 

 