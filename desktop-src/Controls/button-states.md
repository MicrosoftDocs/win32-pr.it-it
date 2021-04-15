---
title: Stati del pulsante
description: Questa sezione illustra in che modo la selezione di un pulsante modifica lo stato e il modo in cui l'applicazione deve rispondere.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474446"
---
# <a name="button-states"></a>Stati del pulsante

Questa sezione illustra in che modo la selezione di un pulsante modifica lo stato e il modo in cui l'applicazione deve rispondere.

La sezione è costituita dagli argomenti seguenti:

-   [Selezione pulsante](#button-selection)
-   [Elementi dello stato di un pulsante](#elements-of-a-button-state)
    -   [Stato attivo](#focus-state)
    -   [Stato push](#push-state)
    -   [Controlla stato](#check-state)
-   [Modifiche allo stato di un pulsante](#changes-to-a-button-state)

## <a name="button-selection"></a>Selezione pulsante

L'utente può selezionare un pulsante in tre modi: facendo clic su di esso con il mouse, eseguendo una tabulazione e premendo il tasto INVIO oppure, se il pulsante fa parte di un gruppo definito dallo stile del [**\_ gruppo WS**](/windows/desktop/winmsg/window-styles) , tramite la tabulazione al pulsante selezionato nel gruppo e utilizzando i tasti di direzione per spostarsi all'interno di tale gruppo. I due metodi di tabulazione fanno parte dell'interfaccia della tastiera predefinita fornita dal sistema. Per una descrizione completa di questa interfaccia, vedere finestre di [dialogo](/windows/desktop/dlgbox/dialog-boxes).

La selezione di un pulsante causa in genere gli eventi seguenti:

-   Il sistema assegna al pulsante lo stato attivo della tastiera.
-   Il pulsante Invia alla finestra padre un messaggio per notificare la selezione.
-   La finestra padre (o il sistema) Invia al pulsante un messaggio per modificarne lo stato.
-   La finestra padre (o il sistema) ridisegna il pulsante in modo da riflettere il nuovo stato.

## <a name="elements-of-a-button-state"></a>Elementi dello stato di un pulsante

Lo stato di un pulsante può essere caratterizzato dallo stato attivo, dallo stato di push e dallo stato di selezione.

-   [Stato attivo](#focus-state)
-   [Stato push](#push-state)
-   [Controlla stato](#check-state)

### <a name="focus-state"></a>Stato attivo

Lo stato attivo si applica a una casella di controllo, un pulsante di opzione, un pulsante di push o un pulsante creato dal proprietario. Un pulsante riceve lo stato attivo quando l'utente lo seleziona e perde lo stato attivo quando l'utente seleziona un altro controllo. Un solo controllo può avere lo stato attivo della tastiera alla volta.

Quando un pulsante ha lo stato attivo della tastiera, in genere il sistema evidenzia il testo, l'icona o la bitmap di un pulsante, che lo circonda con una linea tratteggiata. Inoltre, un pulsante di push ha un bordo scuro intenso quando ha lo stato attivo. Il sistema modifica automaticamente l'evidenziazione per un pulsante automatico, ma l'applicazione deve modificare l'evidenziazione per un pulsante non automatico inviando messaggi.

### <a name="push-state"></a>Stato push

Lo stato push si applica a un pulsante di comando, una casella di controllo, un pulsante di opzione o una casella di controllo a tre stati, ma non si applica ad altri pulsanti. Lo stato di push di un pulsante può essere inserito o meno. Quando viene eseguito il push di un pulsante di push (o di qualsiasi pulsante con lo stile [**BS \_ PUSHLIKE**](button-styles.md) ), il pulsante viene disegnato come pulsante incassato. Quando non viene eseguito il push, viene disegnato come pulsante in rilievo. Quando si fa clic su una casella di controllo, un pulsante di opzione o una casella di controllo a tre stati, lo sfondo del pulsante è disattivato. Quando non viene eseguito il push, lo sfondo del pulsante non è grigio.

### <a name="check-state"></a>Controlla stato

Lo stato di controllo si applica a una casella di controllo, un pulsante di opzione o una casella di controllo a tre stati, ma non si applica ad altri pulsanti. Lo stato può essere selezionato, cancellato o (per le caselle di controllo a tre stati) indeterminato. Una casella di controllo viene selezionata quando contiene un segno di spunta e viene deselezionata in caso contrario. Un pulsante di opzione viene selezionato quando contiene un punto nero; viene cancellato in caso contrario. Una casella di controllo a tre stati viene verificata quando contiene un segno di spunta, viene deselezionata quando non è presente ed è indeterminata quando contiene una casella in grigio. Il sistema modifica automaticamente lo stato di selezione di un pulsante automatico, ma l'applicazione deve modificare lo stato di selezione di un pulsante non automatico.

## <a name="changes-to-a-button-state"></a>Modifiche allo stato di un pulsante

Quando l'utente seleziona un pulsante, è in genere necessario modificare uno o più elementi di stato del pulsante. Il sistema modifica automaticamente lo stato attivo per tutti i tipi di pulsante, lo stato di push per i pulsanti o i pulsanti di push con lo stile [**BS \_ PUSHLIKE**](button-styles.md) e lo stato di selezione per tutti i pulsanti automatici. L'applicazione deve apportare tutte le altre modifiche di stato, prendendo in considerazione il tipo, lo stile e lo stato corrente del pulsante. L'elenco seguente Mostra gli elementi di stato che devono essere modificati per ogni tipo di pulsante:

-   Una casella di controllo deve modificare lo stato di selezione.
-   Un pulsante di opzione deve modificare lo stato di selezione. Potrebbe anche essere necessario modificare lo stato di selezione di altri pulsanti di opzione nello stesso gruppo per assicurarsi che la natura reciprocamente esclusiva dei pulsanti di opzione.
-   Poiché lo stato di un pulsante creato dal proprietario è dipendente dall'applicazione, le modifiche apportate dall'applicazione nel pulsante possono variare. Non è necessario modificare gli elementi di una casella di gruppo perché gli utenti non possono selezionare le caselle di gruppo.

Un'applicazione può determinare lo stato di un pulsante inviando un [**messaggio \_ BM GetCheck**](bm-getcheck.md) o [**BM \_ GetState**](bm-getstate.md) . l'applicazione può impostare lo stato di un pulsante inviando un messaggio [**BM \_ secheck**](bm-setcheck.md) o [**BM \_ sestate**](bm-setstate.md) Message.

 

 