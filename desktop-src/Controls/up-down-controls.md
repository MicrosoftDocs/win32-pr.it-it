---
title: Informazioni sui controlli Up-Down
description: Un controllo di scorrimento è una coppia di pulsanti freccia su cui l'utente può fare clic per incrementare o decrementare un valore, ad esempio una posizione di scorrimento o un numero visualizzato in un controllo complementare (chiamato finestra di Buddy).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc8dad15a8254b138cae4175cc16b1ef3111745
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730583"
---
# <a name="about-up-down-controls"></a>Informazioni sui controlli Up-Down

Un controllo di scorrimento è una coppia di pulsanti freccia su cui l'utente può fare clic per incrementare o decrementare un valore, ad esempio una posizione di scorrimento o un numero visualizzato in un controllo complementare (chiamato finestra di Buddy).

Per l'utente, un controllo di scorrimento e la relativa finestra di Buddy appaiono spesso come un unico controllo. È possibile specificare che un controllo di scorrimento si posiziona automaticamente accanto alla finestra Buddy e che imposta automaticamente la didascalia della finestra buddy sulla posizione corrente. Ad esempio, è possibile usare un controllo di scorrimento con un controllo di modifica per richiedere all'utente l'input numerico. Nella figura seguente viene illustrato un controllo di scorrimento con un controllo di modifica come finestra di contatto, una combinazione a volte definita controllo casella di selezione.

![screenshot che mostra un controllo rettangolare breve e largo con frecce su e giù sul bordo destro](images/updown.jpg)

In questa sezione vengono descritti gli argomenti seguenti.

-   [Stili di controllo di scorrimento](#up-down-control-styles)
-   [Posizione e accelerazione](#position-and-acceleration)
-   [Impostazione predefinita Up-Down controlla l'elaborazione dei messaggi](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Stili del controllo Up-Down

Utilizzando gli stili della finestra, è possibile modificare le caratteristiche di un controllo di scorrimento, ad esempio il modo in cui si posiziona in relazione alla relativa finestra di contatto, se viene impostato il testo della finestra Buddy e se vengono elaborati i tasti freccia su e freccia giù.

Un controllo di scorrimento con lo stile [**UDS \_ ALIGNLEFT**](up-down-control-styles.md) o [**UDS \_ ALIGNRIGHT**](up-down-control-styles.md) è allineato al bordo sinistro o destro della finestra di contatto. La larghezza della finestra di Buddy viene ridotta per adattarsi alla larghezza del controllo di scorrimento.

Un controllo di scorrimento con lo stile [**\_ SETBUDDYINT di UDS**](up-down-control-styles.md) imposta la didascalia della finestra di Buddy ogni volta che la posizione corrente viene modificata. Il controllo inserisce un separatore delle migliaia tra ogni tre cifre di una stringa decimale, a meno che non sia specificato lo stile [**\_ nomiles di UDS**](up-down-control-styles.md) . Se la finestra Buddy è una casella di riepilogo, un controllo di scorrimento ne imposta la selezione corrente anziché la didascalia.

È possibile specificare lo [**stile \_ ARROWKEYS di UDS**](up-down-control-styles.md) per fornire un'interfaccia della tastiera per un controllo di scorrimento. Se viene specificato questo stile, il controllo elabora i tasti freccia su e giù. Il controllo esegue anche la sottoclasse della finestra buddy per poter elaborare queste chiavi quando la finestra di Buddy ha lo stato attivo.

Se si usa un controllo di scorrimento per lo scorrimento orizzontale, è possibile specificare lo stile [**\_ orizzontalmente di UDS**](up-down-control-styles.md) . Con questo stile le frecce del controllo di scorrimento devono puntare verso sinistra e verso destra anziché verso l'alto e verso il basso.

Per impostazione predefinita, la posizione corrente non cambia se l'utente tenta di incrementarlo o di diminuirlo oltre il valore massimo o minimo. È possibile modificare questo comportamento usando lo stile [**di \_ incapsulamento di UDS**](up-down-control-styles.md) , quindi la posizione "esegue il wrapping" nell'estremo opposto. Ad esempio, l'incremento oltre il limite superiore consente di eseguire il wrapping della posizione fino al limite inferiore.

## <a name="position-and-acceleration"></a>Posizione e accelerazione

Dopo aver creato un controllo di scorrimento, è possibile modificare la posizione corrente del controllo, la posizione minima e la posizione massima inviando messaggi. È inoltre possibile modificare la base radice utilizzata per visualizzare la posizione corrente nella finestra di Buddy e la velocità di modifica della posizione corrente quando si fa clic sulla freccia verso l'alto o verso il basso.

Per recuperare la posizione corrente di un controllo di scorrimento, utilizzare il messaggio [**UDM \_ GETPOS**](udm-getpos.md) . Per un controllo di scorrimento con una finestra di Buddy, la posizione corrente è il numero nella didascalia della finestra buddy. Poiché la didascalia potrebbe essere stata modificata (ad esempio, l'utente potrebbe aver modificato il testo di un controllo di modifica), il controllo di scorrimento recupera la didascalia corrente e aggiorna la posizione corrente di conseguenza.

La didascalia della finestra Buddy può essere una stringa decimale o esadecimale, a seconda della base radice (ovvero la base 10 o 16) del controllo di scorrimento. È possibile impostare la base radice usando il messaggio [**di \_ base UDM**](udm-setbase.md) e recuperare la base radice usando il messaggio [**\_ getBase UDM**](udm-getbase.md) .

Il messaggio [**UDM \_ SETPOS**](udm-setpos.md) imposta la posizione corrente di una finestra di Buddy. Si noti che a differenza di una barra di scorrimento, un controllo di scorrimento modifica automaticamente la posizione corrente quando si fa clic sulle frecce verso l'alto e verso il basso. Non è quindi necessario che un'applicazione imposti la posizione corrente durante l'elaborazione del messaggio [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) .

È possibile modificare le posizioni minime e massime di un controllo di scorrimento usando il [**messaggio \_ SetRange UDM**](udm-setrange.md) . La posizione massima può essere minore del valore minimo e, in tal caso, fare clic sul pulsante freccia in su diminuisce la posizione corrente. Per inserirlo in un altro modo, significa spostandosi verso la posizione massima. Per recuperare le posizioni minime e massime per un controllo di scorrimento, usare il messaggio [**UDM \_ GetRange**](udm-getrange.md) .

È possibile controllare la velocità di modifica della posizione quando l'utente ha premuto un pulsante di freccia impostando l'accelerazione del controllo di scorrimento. L'accelerazione è definita da una matrice di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) . Ogni struttura specifica un intervallo di tempo e il numero di unità in base a cui incrementare o decrementare alla fine di tale intervallo. Per impostare l'accelerazione, utilizzare il messaggio [**UDM \_ SETACCEL**](udm-setaccel.md) . Per recuperare le informazioni sull'accelerazione, usare il messaggio [**UDM \_ GETACCEL**](udm-getaccel.md) .

## <a name="default-up-down-controls-message-processing"></a>Impostazione predefinita Up-Down controlla l'elaborazione dei messaggi

In questa sezione vengono descritti i messaggi Windows standard elaborati da un controllo di scorrimento.



| Message                                        | Elaborazione eseguita                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)             | Alloca e Inizializza una struttura di dati privata e salva il relativo indirizzo come dati della finestra.                                                                                                                     |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera i dati allocati durante l'elaborazione di [**WM \_ create**](/windows/desktop/winmsg/wm-create) .                                                                                                                                   |
| [**\_Abilitazione WM**](/windows/desktop/winmsg/wm-enable)             | Invalida la finestra.                                                                                                                                                                                      |
| [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)         | Modifica la posizione corrente nel caso di un tasto freccia su o freccia giù.                                                                                                                                   |
| [**KEYUP di WM \_**](/windows/desktop/inputdev/wm-keyup)             | Completa la modifica della posizione.                                                                                                                                                                               |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Acquisisce il mouse. Se la finestra Buddy è un controllo di modifica o una casella di riepilogo, imposta lo stato attivo sulla finestra buddy. Se il mouse si trova sul pulsante su o giù, inizia a modificare la posizione e imposta un timer. |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)     | Completa la modifica della posizione e rilascia l'acquisizione del mouse se il controllo di scorrimento ha acquisito il mouse. Se la finestra Buddy è un controllo di modifica, seleziona tutto il testo nel controllo di modifica.             |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                  | Disegna il controllo di scorrimento. Se il parametro *wParam* è diverso da null, il controllo presuppone che il valore sia un **HDC** e i colori che usano tale contesto di dispositivo.                                                    |
| [**\_timer WM**](/windows/desktop/winmsg/wm-timer)               | Modifica la posizione corrente se il mouse viene mantenuto su un pulsante e se è trascorso un intervallo sufficiente.                                                                                            |



 

 

 