---
title: Tipi di pulsante
description: Sono disponibili diversi tipi di pulsanti e uno o più stili di pulsante per distinguere tra i pulsanti dello stesso tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682cc39ed2f88ce88f499757fbc4f902bfdceeea
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730599"
---
# <a name="button-types"></a>Tipi di pulsante

Sono disponibili diversi tipi di pulsanti e uno o più stili di pulsante per distinguere tra i pulsanti dello stesso tipo.

In questo documento vengono illustrati gli argomenti seguenti.

-   [Tipi e stili di pulsanti](#button-types-and-styles)
-   [Caselle di controllo](#check-boxes)
-   [Caselle di gruppo](#group-boxes)
-   [Pulsanti di push](#push-buttons)
-   [Pulsanti di opzione](#radio-buttons)
-   [Argomenti correlati](#related-topics)

## <a name="button-types-and-styles"></a>Tipi e stili di pulsanti

Un pulsante appartiene a un tipo e può avere stili aggiuntivi che ne influenzano l'aspetto e il comportamento. Per una tabella di stili di pulsante, vedere [stili dei pulsanti](button-styles.md).

Lo screenshot seguente mostra i diversi tipi di pulsanti.

![Screenshot di una finestra di dialogo che mostra esempi di otto tipi di pulsanti](images/buttontypes.png)

Lo screenshot mostra come possono apparire i pulsanti in Windows Vista. L'aspetto può variare in base alle diverse versioni del sistema operativo e in base al tema impostato dall'utente.

Si notino i punti seguenti sull'illustrazione:

-   La casella di controllo a tre stati viene visualizzata nello stato indeterminato. Se è selezionata o deselezionata, la casella di controllo è simile a una casella di controllo normale.
-   Il pulsante di push di grandi dimensioni è stato impostato sullo stato push a livello di codice (inviando il messaggio di [**\_ stato BM**](bm-setstate.md) ), in modo che mantenga l'aspetto anche quando non viene fatto clic su di esso.
-   Nello stile di visualizzazione visualizzato, lo sfondo del pulsante di push predefinito (o un altro pulsante di push con lo stato attivo per l'input) viene ciclito tra blu e grigio.

## <a name="check-boxes"></a>Caselle di controllo

Una *casella di controllo* è costituita da una casella quadrata e da un'etichetta, un'icona o una bitmap definita dall'applicazione che indica una scelta che l'utente può effettuare selezionando il pulsante. Le applicazioni in genere visualizzano le caselle di controllo per consentire all'utente di scegliere una o più opzioni che non si escludono a vicenda.

Una casella di controllo può essere costituita da uno dei quattro stili seguenti: standard, automatico, a tre Stati e automatico a tre stati, come definito [**dalla \_ casella**](button-styles.md)di controllo Constants BS, [**BS \_ AUTOCHECKBOX**](button-styles.md), [**BS \_ 3STATE**](button-styles.md)e [**BS \_ AUTO3STATE**](button-styles.md), rispettivamente. Ogni stile può assumere due stati di controllo: selezionati (un segno di spunta all'interno della casella) o deselezionati (nessun segno di spunta). Inoltre, una casella di controllo a tre stati può assumere uno stato indeterminato, ovvero una casella ombreggiata all'interno della casella di controllo, che potrebbe indicare che l'utente non ha scelto. Se si fa clic ripetutamente su una casella di controllo standard o automatico, questa viene disattivata e viceversa. Se si fa clic ripetutamente su una casella di controllo a tre stati, questa viene disattivata da checked a deselezionata, quindi il ciclo viene ripetuto.

Quando l'utente fa clic su una casella di controllo (di qualsiasi stile), la casella di controllo riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre della casella di controllo un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) contenente il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) . La finestra padre non deve gestire questo messaggio se deriva da una casella di controllo automatica o da una casella di controllo automatica a tre stati, perché il sistema imposta automaticamente lo stato di selezione per tali stili. La finestra padre, tuttavia, deve gestire il messaggio se deriva da una casella di controllo non automatica o a tre stati, perché la finestra padre è responsabile dell'impostazione dello stato di selezione per tali stili. Indipendentemente dallo stile della casella di controllo, il sistema ridisegna automaticamente la casella di controllo una volta modificato lo stato.

L'applicazione può verificare lo stato di una casella di controllo tramite la funzione [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="group-boxes"></a>Caselle di gruppo

Una *casella di gruppo* è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, con un'etichetta di testo definita dall'applicazione nell'angolo superiore sinistro. L'unico scopo di una casella di gruppo è organizzare i controlli correlati da uno scopo comune, generalmente indicato dall'etichetta. Per la casella di gruppo è presente un solo stile, definito dalla costante [**b \_ GroupBox**](button-styles.md). Poiché non è possibile selezionare una casella di gruppo, non è presente alcuno stato di controllo, stato attivo o stato push.

## <a name="push-buttons"></a>Pulsanti di push

Un *pulsante di push* è un rettangolo contenente un'etichetta di testo definita dall'applicazione, un'icona o una bitmap che indica il comportamento del pulsante quando viene selezionato dall'utente.

Un pulsante di push può essere uno dei due stili, standard o predefinito, come definito dal [**\_ pulsante BS**](button-styles.md) delle costanti e [**BS \_ DEFPUSHBUTTON**](button-styles.md). Un pulsante di push standard viene in genere usato per avviare un'operazione. Riceve lo stato attivo quando l'utente fa clic su di esso. Un pulsante di push predefinito viene in genere usato per indicare la scelta più comune o predefinita, ad esempio la chiusura della finestra di dialogo. Si tratta di un pulsante che l'utente può selezionare semplicemente premendo INVIO quando nessun altro pulsante di push nella finestra di dialogo ha lo stato attivo per l'input.

Quando l'utente fa clic su un pulsante di push, riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre del pulsante un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) che contiene il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) .

Il *pulsante di suddivisione* è un tipo speciale di pulsante di push introdotto in Windows Vista e nella [versione 6,00](common-control-versions.md). Un pulsante combinato è suddiviso in due parti. La parte principale funziona come un pulsante di push normale o predefinito. La seconda parte ha una freccia rivolta verso il basso. Viene in genere visualizzato un menu quando si fa clic sulla freccia.

Un pulsante di suddivisione ha lo stile [**BS \_ SPLITBUTTON**](button-styles.md) oppure lo stile [**BS \_ DEFSPLITBUTTON**](button-styles.md) se è il pulsante predefinito in una finestra di dialogo. È possibile modificare l'aspetto del pulsante usando il messaggio [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) o la macro [**\_ SETSPLITINFO Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) corrispondente.

Quando l'utente fa clic sulla parte principale del pulsante di suddivisione, invia una notifica [ \_ con clic su BN](bn-clicked.md) come un normale pulsante di push. Tuttavia, quando l'utente fa clic sulla freccia verso il basso, invia una notifica a [ \_ discesa BCN](bcn-dropdown.md) . È responsabilità dell'applicazione visualizzare un menu in risposta all'elenco a discesa BCN \_ .

Windows Vista e la [versione 6,00](common-control-versions.md) hanno introdotto anche un altro tipo di pulsante di push, il *collegamento del comando*. Visivamente, un collegamento del comando è molto diverso da un normale pulsante di push, ma ha la stessa funzionalità. Un collegamento al comando Visualizza in genere un'icona a freccia, una riga di testo e un testo aggiuntivo in un tipo di carattere più piccolo.

## <a name="radio-buttons"></a>Pulsanti di opzione

Un *pulsante* di opzione, denominato anche pulsante di opzione, è costituito da un pulsante rotondo e da un'etichetta, un'icona o una bitmap definita dall'applicazione che indica una scelta che l'utente può effettuare selezionando il pulsante. Un'applicazione usa in genere i pulsanti di opzione in una casella di gruppo per consentire all'utente di scegliere uno dei set di opzioni correlate che si escludono a vicenda.

Un pulsante di opzione può essere uno dei due stili seguenti: standard o automatico, in base a quanto definito dalle costanti di stile [**BS \_ RadioButton**](button-styles.md) e [**BS \_ AUTORADIOBUTTON**](button-styles.md). Ogni stile può assumere due stati di controllo: selezionato (un punto nel pulsante) o cancellato (nessun punto nel pulsante).

Quando l'utente seleziona uno stato, il pulsante di opzione riceve lo stato attivo della tastiera. Il sistema invia alla finestra padre del pulsante un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) contenente il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) . La finestra padre non deve gestire questo messaggio se deriva da un pulsante di opzione automatico, perché il sistema imposta automaticamente lo stato di selezione per lo stile. La finestra padre, tuttavia, deve gestire il messaggio se deriva da un pulsante di opzione non automatico, perché la finestra padre è responsabile dell'impostazione dello stato di selezione per lo stile. Indipendentemente dallo stile del pulsante di opzione, il sistema ridisegna automaticamente il pulsante come modifica dello stato.

I pulsanti di opzione sono disposti in gruppi ed è possibile controllare un solo pulsante del gruppo in qualsiasi momento. Se il flag [**WS \_ Group**](/windows/desktop/winmsg/window-styles) è impostato per qualsiasi pulsante di opzione, il pulsante è il primo pulsante in un gruppo e tutti i pulsanti che lo seguono immediatamente nell'ordine di tabulazione (ma non hanno il flag di **\_ gruppo WS** ) fanno parte del gruppo. Se nessun pulsante di opzione ha il flag di **\_ gruppo WS** , tutti i pulsanti di opzione nella finestra di dialogo vengono considerati come un singolo gruppo.

L'applicazione può verificare se un pulsante di opzione viene controllato tramite la funzione [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di pulsanti](using-buttons.md)
</dt> </dl>

 

 