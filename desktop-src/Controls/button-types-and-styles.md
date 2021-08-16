---
title: Tipi di pulsante
description: Esistono diversi tipi di pulsanti e uno o più stili di pulsante per distinguere i pulsanti dello stesso tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c3614f90c36d5a81603153ec7c8612d61e73e2e98c7f668cb53a6ad2bb584b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832497"
---
# <a name="button-types"></a>Tipi di pulsante

Esistono diversi tipi di pulsanti e uno o più stili di pulsante per distinguere i pulsanti dello stesso tipo.

Questo documento illustra gli argomenti seguenti.

-   [Tipi e stili dei pulsanti](#button-types-and-styles)
-   [Caselle](#check-boxes)
-   [Caselle di gruppo](#group-boxes)
-   [Pulsanti](#push-buttons)
-   [Pulsanti](#radio-buttons)
-   [Argomenti correlati](#related-topics)

## <a name="button-types-and-styles"></a>Tipi e stili dei pulsanti

Un pulsante appartiene a un tipo e può avere stili aggiuntivi che ne influiscono sull'aspetto e sul comportamento. Per una tabella degli stili dei pulsanti, vedere [Stili dei pulsanti.](button-styles.md)

Lo screenshot seguente mostra i diversi tipi di pulsanti.

![Screenshot di una finestra di dialogo che mostra esempi di otto tipi di pulsanti](images/buttontypes.png)

Lo screenshot mostra come possono essere visualizzati i pulsanti in Windows Vista. L'aspetto varia in base alle diverse versioni del sistema operativo e in base al tema impostato dall'utente.

Si notino i punti seguenti sull'illustrazione:

-   La casella di controllo a tre stati viene visualizzata nello stato indeterminato. Se selezionata o deselezionata, ha l'aspetto di una normale casella di controllo.
-   Il pulsante push di grandi dimensioni è stato impostato sullo stato push a livello di codice (inviando il messaggio [**BM \_ SETSTATE),**](bm-setstate.md) in modo che manteni l'aspetto anche quando non viene fatto clic su di esso.
-   Nello stile di visualizzazione visualizzato, lo sfondo del pulsante di pressione predefinito (o di un altro pulsante con lo stato attivo per l'input) scorre tra blu e grigio.

## <a name="check-boxes"></a>Caselle

Una *casella di controllo* è costituita da una casella quadrata e da un'etichetta, un'icona o una bitmap definita dall'applicazione che indica una scelta che l'utente può effettuare selezionando il pulsante . Le applicazioni visualizzano in genere caselle di controllo per consentire all'utente di scegliere una o più opzioni che non si escludono a vicenda.

Una casella di controllo può essere uno dei quattro stili standard, automatico, a tre stati e automatico a tre stati, come definito dalle costanti [**BS \_ CHECKBOX,**](button-styles.md) [**BS \_ AUTOCHECKBOX,**](button-styles.md) [**BS \_ 3STATE**](button-styles.md)e [**BS \_ AUTO3STATE,**](button-styles.md)rispettivamente. Ogni stile può presupporre due stati di controllo: selezionato (un segno di spunta all'interno della casella) o deselezionato (nessun segno di spunta). Inoltre, una casella di controllo a tre stati può presupporre uno stato indeterminato (una casella ombreggiata all'interno della casella di controllo), che potrebbe indicare che l'utente non ha fatto una scelta. Facendo ripetutamente clic su una casella di controllo standard o automatica, la casella di controllo passa da selezionata a deselezionata e di nuovo indietro. Facendo ripetutamente clic su una casella di controllo a tre stati, la casella di controllo passa da selezionata a deselezionata a indeterminata e quindi ripete il ciclo.

Quando l'utente fa clic su una casella di controllo (di qualsiasi stile), la casella di controllo riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre della casella di controllo un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contenente il [codice di notifica BN \_ CLICKED.](bn-clicked.md) La finestra padre non deve gestire questo messaggio se proviene da una casella di controllo automatica o da una casella di controllo automatica a tre stati, perché il sistema imposta automaticamente lo stato di controllo per tali stili. Tuttavia, la finestra padre deve gestire il messaggio se proviene da una casella di controllo non automatica o da una casella di controllo a tre stati, perché la finestra padre è responsabile dell'impostazione dello stato di controllo per tali stili. Indipendentemente dallo stile della casella di controllo, il sistema ridisegna automaticamente la casella di controllo dopo la modifica dello stato.

L'applicazione può determinare lo stato di una casella di controllo usando la [**funzione IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="group-boxes"></a>Caselle di gruppo

Una *casella di gruppo* è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, con un'etichetta di testo definita dall'applicazione nell'angolo superiore sinistro. L'unico scopo di una casella di gruppo è organizzare i controlli correlati in base a uno scopo comune (in genere indicato dall'etichetta). La casella di gruppo ha un solo stile, definito dalla costante [**BS \_ GROUPBOX**](button-styles.md). Poiché una casella di gruppo non può essere selezionata, non ha stato di controllo, stato attivo o stato push.

## <a name="push-buttons"></a>Pulsanti

Un *pulsante di pressione* è un rettangolo contenente un'etichetta di testo definita dall'applicazione, un'icona o una bitmap che indica le effetti del pulsante quando l'utente lo seleziona.

Un pulsante push può essere uno dei due stili standard o predefiniti, come definito dalle costanti [**BS \_ PUSHBUTTON**](button-styles.md) e [**BS \_ DEFPUSHBUTTON**](button-styles.md). Un pulsante push standard viene in genere usato per avviare un'operazione. Riceve lo stato attivo della tastiera quando l'utente fa clic su di esso. Un pulsante di pressione predefinito viene in genere usato per indicare la scelta più comune o predefinita, ad esempio la chiusura della finestra di dialogo. Si tratta di un pulsante che l'utente può selezionare semplicemente premendo INVIO quando nessun altro pulsante push nella finestra di dialogo ha lo stato attivo per l'input.

Quando l'utente fa clic su un pulsante push, riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre del pulsante un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contenente il codice di notifica [BN \_ CLICKED.](bn-clicked.md)

Il *pulsante di divisione* è un tipo speciale di pulsante push introdotto in Windows Vista e versione [6.00.](common-control-versions.md) Un pulsante di divisione è suddiviso in due parti. La parte principale funziona come un pulsante normale o predefinito. La seconda parte ha una freccia che punta verso il basso. In genere viene visualizzato un menu quando si fa clic sulla freccia.

Un pulsante di divisione ha lo [**stile \_ BS SPLITBUTTON**](button-styles.md) o lo stile [**\_ BS DEFSPLITBUTTON**](button-styles.md) se è il pulsante predefinito in una finestra di dialogo. È possibile modificare l'aspetto del pulsante usando il [**messaggio \_ BCM SETSPLITINFO**](bcm-setsplitinfo.md) o la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) corrispondente.

Quando l'utente fa clic sulla parte principale del pulsante di divisione, invia una notifica [BN \_ CLICKED](bn-clicked.md) proprio come un normale pulsante push. Tuttavia, quando l'utente fa clic sulla freccia giù, invia una [notifica BCN \_ DROPDOWN.](bcn-dropdown.md) È responsabilità dell'applicazione visualizzare un menu in risposta a BCN \_ DROPDOWN.

Windows Vista e [la versione 6.00](common-control-versions.md) hanno anche introdotto un altro tipo di pulsante push, il *collegamento al comando*. Visivamente, un collegamento di comando è molto diverso da un normale pulsante di push, ma ha la stessa funzionalità. Un collegamento di comando visualizza in genere un'icona a forma di freccia, una riga di testo e testo aggiuntivo con un tipo di carattere più piccolo.

## <a name="radio-buttons"></a>Pulsanti

Un *pulsante di* opzione (detto anche pulsante di opzione) è costituito da un pulsante arrotondato e da un'etichetta, un'icona o una bitmap definita dall'applicazione che indica una scelta che l'utente può effettuare selezionando il pulsante. Un'applicazione usa in genere i pulsanti di opzione in una casella di gruppo per consentire all'utente di scegliere una delle opzioni correlate ma che si escludono a vicenda.

Un pulsante di opzione può essere uno dei due stili seguenti: standard o automatico, come definito dalle costanti di stile [**BS \_ RADIOBUTTON**](button-styles.md) e [**BS \_ AUTORADIOBUTTON**](button-styles.md). Ogni stile può presupporre due stati di controllo: selezionato (un punto nel pulsante) o deselezionato (nessun punto nel pulsante).

Quando l'utente seleziona uno stato, il pulsante di opzione riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre del pulsante un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contenente il [codice di notifica BN \_ CLICKED.](bn-clicked.md) La finestra padre non deve gestire questo messaggio se proviene da un pulsante di opzione automatico, perché il sistema imposta automaticamente lo stato del controllo per tale stile. Tuttavia, la finestra padre deve gestire il messaggio se proviene da un pulsante di opzione non automatico, perché la finestra padre è responsabile dell'impostazione dello stato del controllo per tale stile. Indipendentemente dallo stile del pulsante di opzione, il sistema ridisegna automaticamente il pulsante quando cambia lo stato.

I pulsanti di opzione sono disposti in gruppi e un solo pulsante nel gruppo può essere selezionato in qualsiasi momento. Se il flag [**WS \_ GROUP**](/windows/desktop/winmsg/window-styles) è impostato per qualsiasi pulsante di opzione, tale pulsante è il primo pulsante di un gruppo e tutti i pulsanti che lo seguono immediatamente nell'ordine di tabulazione (ma non hanno il flag **WS \_ GROUP)** fanno parte del gruppo. Se nessun pulsante di opzione ha il flag **WS \_ GROUP,** tutti i pulsanti di opzione nella finestra di dialogo vengono considerati come un singolo gruppo.

L'applicazione può verificare se un pulsante di opzione è selezionato usando la [**funzione IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso dei pulsanti](using-buttons.md)
</dt> </dl>

 

 