---
title: Informazioni sui controlli indicatore di stato
description: Un indicatore di stato è una finestra che può essere utilizzata da un'applicazione per indicare lo stato di avanzamento di un'operazione di lunga durata. È costituito da un rettangolo che viene animato durante l'avanzamento di un'operazione.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730450"
---
# <a name="about-progress-bar-controls"></a>Informazioni sui controlli indicatore di stato

Un indicatore di stato è una finestra che può essere utilizzata da un'applicazione per indicare lo stato di avanzamento di un'operazione di lunga durata.

È costituito da un rettangolo che viene animato durante l'avanzamento di un'operazione.

La figura seguente mostra un indicatore di stato che non usa gli stili di visualizzazione.

![Screenshot di un indicatore di stato che aggiunge rettangoli in una riga per indicare lo stato di avanzamento](images/pb-oldstyle.png)

La figura seguente mostra un indicatore di stato con gli stili di visualizzazione. L'aspetto del controllo può variare a seconda del sistema operativo e del tema selezionato. Per altre informazioni, vedere [stili di visualizzazione](themes-overview.md).

![Screenshot di un indicatore di stato che allunga un rettangolo verde animato per indicare lo stato di avanzamento](images/pb-newstyle.png)

Altre informazioni sono contenute nelle intestazioni riportate di seguito.

-   [Uso delle barre di stato](#using-progress-bars)
    -   [Intervallo e posizione corrente](#range-and-current-position)
    -   [Elaborazione messaggio indicatore di stato predefinito](#default-progress-bar-message-processing)
    -   [Stile Marquee](#marquee-style)

## <a name="using-progress-bars"></a>Uso delle barre di stato

È possibile creare un indicatore di stato usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di [**avanzamento della \_ classe**](common-control-window-classes.md) . Questa classe della finestra viene registrata quando viene caricata la DLL dei controlli comuni. Per ulteriori informazioni, vedere [informazioni sui controlli comuni](common-controls-intro.md).

Il controllo è disponibile anche nella casella degli strumenti Microsoft Visual Studio, dove viene chiamato controllo dello stato di avanzamento.

### <a name="range-and-current-position"></a>Intervallo e posizione corrente

L' *intervallo* di un indicatore di stato rappresenta l'intera durata dell'operazione e la *posizione corrente* rappresenta lo stato di avanzamento dell'applicazione verso il completamento dell'operazione. La routine della finestra usa l'intervallo e la posizione corrente per determinare la percentuale dell'indicatore di stato da riempire con il colore di evidenziazione.

Se non si impostano i valori di intervallo, il sistema imposta il valore minimo su 0 e il valore massimo su 100. È possibile regolare l'intervallo con i valori integer pratici usando il messaggio di [**\_ SetRange PBM**](pbm-setrange.md) .

Un indicatore di stato fornisce diversi messaggi che è possibile utilizzare per impostare la posizione corrente. Il [**messaggio \_ SETPOS di PBM**](pbm-setpos.md) imposta la posizione su un valore specificato. Il [**messaggio \_ DELTAPOS di PBM**](pbm-deltapos.md) fa avanzare la posizione aggiungendo un valore specificato alla posizione corrente.

Il messaggio con estensione PBM consente di specificare un incremento del passaggio per un indicatore di stato. [**\_**](pbm-setstep.md) Successivamente, ogni volta che si invia il messaggio [**\_ STEPIT di PBM**](pbm-stepit.md) all'indicatore di stato, la posizione corrente avanza in base all'incremento specificato. Per impostazione predefinita, l'incremento del passaggio è impostato su 10.

### <a name="default-progress-bar-message-processing"></a>Elaborazione messaggio indicatore di stato predefinito

In questa sezione vengono descritti i messaggi gestiti dalla routine della finestra [**per \_ la classe Progress**](common-control-window-classes.md) .



| Message            | Elaborazione eseguita                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **creazione di WM \_**     | Alloca e Inizializza una struttura iniziale.                                                                                                                                    |
| **eliminazione di WM \_**    | Libera tutte le risorse associate all'indicatore di stato.                                                                                                                              |
| **\_ERASEBKGND WM** | Disegna lo sfondo e i bordi dell'indicatore di stato.                                                                                                                              |
| **\_tipo di carattere WM GetFont**    | Restituisce l'handle per il tipo di carattere corrente. Nell'indicatore di stato non viene attualmente disegnato il testo, quindi l'invio di questo messaggio non ha alcun effetto sul controllo.                                       |
| **\_disegno WM**      | Disegna l'indicatore di stato. Se il parametro *wParam* è diverso da **null**, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.                              |
| **\_tipo di carattere WM**    | Salva l'handle nel nuovo tipo di carattere e restituisce l'handle al tipo di carattere precedente. Nell'indicatore di stato non viene attualmente disegnato il testo, quindi l'invio di questo messaggio non ha alcun effetto sul controllo. |



 

### <a name="marquee-style"></a>Stile Marquee

Creando il controllo indicatore di stato con lo stile di [**\_ selezione PBS**](progress-bar-control-styles.md) , è possibile animarlo in modo che mostri l'attività, ma non indichi quale percentuale dell'attività è stata completata. La parte evidenziata dell'indicatore di stato viene spostata ripetutamente lungo la lunghezza della barra. È possibile avviare e arrestare l'animazione e controllarne la velocità inviando il messaggio di proprietà [**PBM \_**](pbm-setmarquee.md) . Gli indicatori di stato Marquee non hanno un intervallo o una posizione.

La figura seguente mostra un indicatore di stato in modalità marquee. La parte evidenziata si sposta sulla barra.

![Screenshot di un indicatore di stato che sposta un'evidenziazione verde in un rettangolo grigio per indicare lo stato di avanzamento](images/pb-marquee.png)

 

 