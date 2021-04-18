---
title: Barre di stato (controlli Windows)
description: Una barra di stato è una finestra orizzontale nella parte inferiore di una finestra padre in cui un'applicazione può visualizzare vari tipi di informazioni sullo stato.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300737"
---
# <a name="status-bars-windows-controls"></a>Barre di stato (controlli Windows)

Una *barra di stato* è una finestra orizzontale nella parte inferiore di una finestra padre in cui un'applicazione può visualizzare vari tipi di informazioni sullo stato. La barra di stato può essere divisa in parti per visualizzare più di un tipo di informazioni. Lo screenshot seguente mostra la barra di stato nell'applicazione Microsoft Windows Paint. In questo caso, la barra di stato contiene il testo "per la guida, scegliere argomenti della guida dal menu?". La barra di stato è l'area nella parte inferiore della finestra che contiene il testo della guida e le informazioni sulla coordinata.

![screenshot dell'applicazione Paint, con una barra di stato che contiene suggerimenti sulla Guida in linea](images/sb-paint.png)

Questa sezione include gli argomenti seguenti.

-   [Tipi e stili](#types-and-styles)
-   [Dimensioni e altezza](#size-and-height)
-   [Barre di stato in più parti](#multiple-part-status-bars)
-   [Operazioni di testo della barra di stato](#status-bar-text-operations)
-   [Barre di stato create dal proprietario](#owner-drawn-status-bars)
-   [Barre di stato modalità semplice](#simple-mode-status-bars)
-   [Elaborazione dei messaggi della barra di stato predefinita](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Tipi e stili

La posizione predefinita di una barra di stato si trova lungo la parte inferiore della finestra padre, ma è possibile specificare lo stile di [**\_ primo livello CCS**](common-control-styles.md) per visualizzarlo nella parte superiore dell'area client della finestra padre.

È possibile specificare lo stile [**SBARS \_ SIZEGRIP**](status-bar-styles.md) per includere un riquadro di ridimensionamento all'estremità destra della barra di stato.

> [!Note]  
> La combinazione degli stili [**CCS \_ Top**](common-control-styles.md) e [**SBARS \_ SIZEGRIP**](status-bar-styles.md) non è consigliata perché il riquadro di ridimensionamento risultante non è funzionante.

 

## <a name="size-and-height"></a>Dimensioni e altezza

La routine della finestra per la barra di stato imposta automaticamente le dimensioni e la posizione iniziali della finestra, ignorando i valori specificati nella funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . La larghezza corrisponde a quella dell'area client della finestra padre. L'altezza si basa sulle metriche del tipo di carattere attualmente selezionato nel contesto di dispositivo della barra di stato e sulla larghezza dei bordi della finestra.

La routine della finestra regola automaticamente le dimensioni della barra di stato ogni volta che viene ricevuto un messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) . In genere, quando viene modificata la dimensione della finestra padre, l'elemento padre invia un messaggio di **\_ dimensioni WM** alla barra di stato.

Un'applicazione può impostare l'altezza minima dell'area di disegno di una barra di stato inviando la finestra un messaggio [**SB \_ SETMINHEIGHT**](sb-setminheight.md) , specificando l'altezza minima, in pixel. L'area di disegno non include i bordi della finestra. Un'altezza minima è utile per il disegno in una barra di stato disegnata dal proprietario. Per ulteriori informazioni, vedere [barre di stato create dal proprietario](#owner-drawn-status-bars) più avanti in questo capitolo.

Per recuperare le larghezze dei bordi di una barra di stato, è necessario inviare alla finestra un messaggio [**SB \_ GetBorders**](sb-getborders.md) . Il messaggio include l'indirizzo di una matrice a tre elementi che riceve le larghezze.

## <a name="multiple-part-status-bars"></a>Barre di stato Multiple-Part

Una barra di stato può avere diverse parti, ognuna delle quali Visualizza una riga di testo diversa. Per dividere una barra di stato in parti, inviare la finestra di un messaggio [**SB \_ separts**](sb-setparts.md) , specificando il numero di parti da creare e l'indirizzo di una matrice di interi. La matrice contiene un elemento per ogni parte e ogni elemento specifica la coordinata client del bordo destro di una parte.

Una barra di stato può avere un massimo di 256 parti, sebbene le applicazioni utilizzino in genere un numero molto inferiore. Si recupera un conteggio delle parti in una barra di stato, nonché la coordinata del bordo destro di ogni parte, inviando la finestra un messaggio [**SB \_ GetParts**](sb-getparts.md) .

## <a name="status-bar-text-operations"></a>Operazioni di testo della barra di stato

È possibile impostare il testo di qualsiasi parte di una barra di stato inviando il messaggio di [**\_ testo SB**](sb-settext.md) , specificando l'indice in base zero di una parte, un indirizzo della stringa da disegnare nella parte e la tecnica per disegnare la stringa. La tecnica di disegno determina se il testo dispone di un bordo e, in tal caso, dello stile del bordo. Determina inoltre se la finestra padre è responsabile del disegno del testo. Per ulteriori informazioni, vedere la sezione [barre di stato create dal proprietario](#owner-drawn-status-bars) di seguito.

Per impostazione predefinita, il testo è allineato a sinistra all'interno della parte specificata di una barra di stato. È possibile incorporare i caratteri di tabulazione ( \\ t) nel testo da allineare al centro o a destra. Il testo a destra di un singolo carattere di tabulazione viene centrato e il testo a destra di un secondo carattere di tabulazione è allineato a destra.

Per recuperare testo da una barra di stato, usare i messaggi [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) e [**SB \_ gettext**](sb-gettext.md) .

Se l'applicazione usa una barra di stato con una sola parte, è possibile usare i [**messaggi \_ WM**](/windows/desktop/winmsg/wm-settext), [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)e [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) per eseguire operazioni di testo. Questi messaggi riguardano solo la parte che ha un indice pari a zero, consentendo di considerare la barra di stato in modo molto simile a un controllo testo statico.

Per visualizzare una riga di stato senza creare una barra di stato, utilizzare la funzione [**DrawStatusText**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) . La funzione usa le stesse tecniche per creare lo stato come routine della finestra per la barra di stato, ma non imposta automaticamente le dimensioni e la posizione delle informazioni sullo stato. Quando si chiama la funzione, è necessario specificare le dimensioni e la posizione delle informazioni sullo stato, nonché il contesto di dispositivo della finestra in cui viene disegnato.

## <a name="owner-drawn-status-bars"></a>Barre di stato Owner-Drawn

È possibile definire le singole parti di una barra di stato in modo che siano parti create dal proprietario. L'uso di questa tecnica offre un maggiore controllo rispetto all'aspetto della parte della finestra. Ad esempio, è possibile visualizzare una bitmap anziché un testo o creare un testo utilizzando un tipo di carattere diverso.

Per definire una parte della finestra come creata dal proprietario, inviare il messaggio di [**\_ testo SB**](sb-settext.md) alla barra di stato, specificando la parte e la \_ tecnica di disegno SBT OWNERDRAW. Quando \_ si specifica SBT OWNERDRAW, il parametro *lParam* è un valore definito dall'applicazione a 32 bit che può essere utilizzato dall'applicazione durante il disegno della parte. Ad esempio, è possibile specificare un handle del tipo di carattere, un handle bitmap, un indirizzo di una stringa e così via.

Quando una barra di stato deve disegnare una parte creata dal proprietario, invia il messaggio di [**WM \_ DrawItem**](wm-drawitem.md) alla finestra padre. Il parametro *wParam* del messaggio è l'identificatore della finestra figlio della barra di stato e il parametro *lParam* è l'indirizzo di una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La finestra padre utilizza le informazioni della struttura per creare la parte. Per una parte creata dal proprietario di una barra di stato, **DRAWITEMSTRUCT** contiene le informazioni seguenti.



| Membro         | Descrizione                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | Non definito Non usare.                                                                                                 |
| **CtlID**      | Identificatore della finestra figlio della barra di stato.                                                                             |
| **ID elemento**     | Indice in base zero della parte da disegnare.                                                                              |
| **itemAction** | Non definito Non usare.                                                                                                 |
| **itemState**  | Non definito Non usare.                                                                                                 |
| **hwndItem**   | Handle per la barra di stato.                                                                                              |
| **hDC**        | Handle per il contesto di dispositivo della barra di stato.                                                                        |
| **rcItem**     | Coordinate della parte della finestra da disegnare. Le coordinate sono relative all'angolo superiore sinistro della barra di stato.   |
| **itemData**   | Valore 32 bit definito dall'applicazione specificato nel parametro *lParam* del messaggio di [**\_ testo SB**](sb-settext.md) . |



 

## <a name="simple-mode-status-bars"></a>Barre di stato modalità semplice

Si inserisce una barra di stato in "modalità semplice" inviando un messaggio [**SB \_ semplice**](sb-simple.md) . Una barra di stato in modalità semplice Visualizza solo una parte. Quando viene impostato il testo della finestra, la finestra viene invalidata, ma non viene ridisegnata fino al [**\_ disegno WM**](/windows/desktop/gdi/wm-paint)successivo. L'attesa del messaggio riduce lo sfarfallio dello schermo, riducendo al minimo il numero di volte in cui la finestra viene ridisegnato. Una barra di stato in modalità semplice è utile per visualizzare il testo della Guida per le voci di menu mentre l'utente scorre il menu.

La stringa visualizzata nella barra di stato in modalità semplice viene gestita separatamente dalle stringhe visualizzate in modalità non semplice. Ciò significa che è possibile attivare la finestra in modalità semplice, impostarne il testo e tornare alla modalità non semplice senza modificare il testo della modalità non semplice.

Quando si imposta il testo di una barra di stato in modalità semplice, è possibile specificare qualsiasi tecnica di disegno eccetto SBT \_ OWNERDRAW. Una barra di stato in modalità semplice non supporta il disegno del proprietario.

## <a name="default-status-bar-message-processing"></a>Elaborazione dei messaggi della barra di stato predefinita

In questa sezione vengono descritti i messaggi gestiti dalla routine della finestra per la classe [**STATUSCLASSNAME**](common-control-window-classes.md) predefinita.



| Message               | Elaborazione predefinita                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **creazione di WM \_**        | Inizializza la barra di stato.                                                                                                                                                                                                                                              |
| **eliminazione di WM \_**       | Libera le risorse allocate per la barra di stato.                                                                                                                                                                                                                            |
| **\_tipo di carattere WM GetFont**       | Restituisce l'handle per il tipo di carattere corrente con cui la barra di stato disegna il testo.                                                                                                                                                                                         |
| **WM \_ GETtext**       | Copia il testo dalla prima parte di una barra di stato in un buffer. Restituisce un valore a 32 bit che specifica la lunghezza, in caratteri, del testo e la tecnica utilizzata per creare il testo.                                                                                |
| **\_GETTEXTLENGTH WM** | Restituisce un valore a 32 bit che specifica la lunghezza, in caratteri, del testo nella prima parte di una barra di stato e la tecnica utilizzata per creare il testo.                                                                                                                  |
| **\_NCHITTEST WM**     | Restituisce il valore HTBOTTOMRIGHT se il cursore del mouse si trova nel riquadro di ridimensionamento, facendo in modo che il sistema visualizzi il cursore di ridimensionamento. Se il cursore del mouse non si trova nel riquadro di ridimensionamento, la barra di stato passa questo messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . |
| **\_disegno WM**         | Disegna l'area non valida della barra di stato. Se il parametro *wParam* è diverso da **null**, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.                                                                                               |
| **\_tipo di carattere WM**       | Seleziona l'handle del tipo di carattere nel contesto di dispositivo per la barra di stato.                                                                                                                                                                                                      |
| **\_testo WM**       | Copia il testo specificato nella prima parte di una barra di stato usando l'operazione di disegno predefinita (specificata come zero). Restituisce **true** se ha esito positivo o **false** in caso contrario.                                                                                       |
| **\_dimensioni WM**          | Ridimensiona la barra di stato in base alla larghezza corrente dell'area client della finestra padre e all'altezza del tipo di carattere corrente della barra di stato.                                                                                                                               |



 

 

 
