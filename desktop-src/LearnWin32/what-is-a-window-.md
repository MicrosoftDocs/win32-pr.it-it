---
title: Che cos'è una finestra
description: Che cos'è una finestra?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8494738e3985f78930549f313cb2868b79b34f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103849"
---
# <a name="what-is-a-window"></a>Che cos'è una finestra?

## <a name="what-is-a-window"></a>Che cos'è una finestra?

Ovviamente, le finestre sono centrali per Windows. Sono così importanti che hanno denominato il sistema operativo dopo di essi. Ma che cos'è una finestra? Quando si pensa a una finestra, è probabile che si pensi a una finestra simile alla seguente:

![Screenshot di una finestra dell'applicazione](images/window01.png)

Questo tipo di finestra è denominato finestra *dell'applicazione o* *finestra principale.* In genere ha un frame con una barra del titolo, **pulsanti Riduci** a icona e **Ingrandisci** e altri elementi standard dell'interfaccia utente. Il frame è denominato *area non client* della finestra, così chiamata perché il sistema operativo gestisce tale parte della finestra. L'area all'interno del frame è *l'area client*. Questa è la parte della finestra che il programma gestisce.

Ecco un altro tipo di finestra:

![Screenshot di una finestra di controllo](images/window02.png)

Se non si ha esperienza con la programmazione di Windows, può essere sorprendente che i controlli dell'interfaccia utente, ad esempio pulsanti e caselle di modifica, siano finestre. La differenza principale tra un controllo dell'interfaccia utente e una finestra dell'applicazione è che un controllo non esiste da solo. Al contrario, il controllo viene posizionato rispetto alla finestra dell'applicazione. Quando si trascina la finestra dell'applicazione, il controllo si sposta con essa, come previsto. Inoltre, il controllo e la finestra dell'applicazione possono comunicare tra loro. Ad esempio, la finestra dell'applicazione riceve le notifiche click da un pulsante.

Pertanto, quando si pensa alla *finestra*, non si pensa semplicemente alla *finestra dell'applicazione*. Si pensi invece a una finestra come a un costrutto di programmazione che:

-   Occupa una determinata parte dello schermo.
-   Può o meno essere visibile in un determinato momento.
-   Sa come disegnare se stesso.
-   Risponde agli eventi dell'utente o del sistema operativo.

## <a name="parent-windows-and-owner-windows"></a>Finestre padre e finestre proprietarie

Nel caso di un controllo dell'interfaccia utente, la finestra del controllo è *l'elemento figlio* della finestra dell'applicazione. La finestra dell'applicazione *è l'elemento* padre della finestra di controllo. La finestra padre fornisce il sistema di coordinate utilizzato per il posizionamento di una finestra figlio. La presenza di una finestra padre influisce sugli aspetti dell'aspetto di una finestra; Ad esempio, una finestra figlio viene ritagliata in modo che nessuna parte della finestra figlio possa essere visualizzata all'esterno dei bordi della finestra padre.

Un'altra relazione è la relazione tra una finestra dell'applicazione e una finestra di dialogo modale. Quando un'applicazione visualizza una finestra di dialogo modale, la finestra dell'applicazione è *la* finestra proprietaria e la finestra è una *finestra di* proprietà. Una finestra di proprietà viene sempre visualizzata davanti alla finestra proprietaria. Viene nascosta quando il proprietario è ridotto a icona e viene eliminato contemporaneamente al proprietario.

L'immagine seguente mostra un'applicazione che visualizza una finestra di dialogo con due pulsanti:

![Screenshot di un'applicazione con una finestra di dialogo](images/window03.png)

La finestra dell'applicazione è proprietaria della finestra di dialogo e la finestra di dialogo è l'elemento padre di entrambe le finestre dei pulsanti. Il diagramma seguente illustra queste relazioni:

![Illustrazione che mostra relazioni padre/figlio e proprietario/proprietà](images/window04.png)

## <a name="window-handles"></a>Handle di finestra

Windows è un oggetto, hanno sia codice che dati, ma non sono classi C++. Un programma fa invece riferimento a una finestra usando un valore denominato *handle*. Un handle è un tipo opaco. In sostanza, è solo un numero che il sistema operativo usa per identificare un oggetto. È possibile creare un'immagine di Windows con una grande tabella di tutte le finestre create. Usa questa tabella per cercare le finestre in base ai relativi handle. Non è importante sapere se funziona esattamente come funziona internamente. Il tipo di dati per gli handle di finestra **è HWND,** che in genere è pronunciato come "aitch-wind". Gli handle di finestra vengono restituiti dalle funzioni che creano finestre: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) e [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

Per eseguire un'operazione su una finestra, in genere si chiamerà una funzione che accetta un **valore HWND** come parametro. Ad esempio, per riposizionare una finestra sullo schermo, chiamare la [**funzione MoveWindow:**](/windows/desktop/api/winuser/nf-winuser-movewindow)


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Il primo parametro è l'handle per la finestra che si vuole spostare. Gli altri parametri specificano la nuova posizione della finestra e specificano se la finestra deve essere ridisegnata.

Tenere presente che gli handle non sono puntatori. Se *hwnd è* una variabile che contiene un handle, il tentativo di dereferenziare l'handle scrivendo `*hwnd` è un errore.

## <a name="screen-and-window-coordinates"></a>Coordinate dello schermo e della finestra

Le coordinate vengono misurate in pixel indipendenti dal dispositivo. Per informazioni sulla parte indipendente  dal dispositivo  dei pixel indipendenti dal dispositivo, si parlerà della grafica.

A seconda dell'attività, è possibile misurare le coordinate relative alla schermata, rispetto a una finestra (inclusa la cornice) o all'area client di una finestra. Ad esempio, si posiziona una finestra sullo schermo usando le coordinate dello schermo, ma si disegna all'interno di una finestra usando le coordinate client. In ogni caso, l'origine (0, 0) è sempre l'angolo superiore sinistro dell'area.

![illustrazione che mostra le coordinate di schermata, finestra e client](images/coordinates01.png)

## <a name="next"></a>Prossima

[WinMain: punto di ingresso dell'applicazione](winmain--the-application-entry-point.md)

 

 
