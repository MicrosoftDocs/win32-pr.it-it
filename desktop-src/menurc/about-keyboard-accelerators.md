---
title: Informazioni sui tasti di scelta rapida
description: In questo argomento vengono illustrati i tasti di scelta rapida.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, tasti di scelta rapida
- input utente, tasti di scelta rapida
- acquisizione dell'input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- acceleratori
- Messaggio WM_COMMAND
- WM_SYS messaggio di comando
- tabelle dei tasti di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9c89301f58d7d76b5d9b28dd6835850c0674db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956379"
---
# <a name="about-keyboard-accelerators"></a>Informazioni sui tasti di scelta rapida

I tasti di scelta rapida sono strettamente correlati ai menu, entrambi consentono agli utenti di accedere al set di comandi di un'applicazione. In genere, gli utenti si basano sui menu di un'applicazione per apprendere il set di comandi e quindi passare all'utilizzo di acceleratori Man mano che diventano più abili con l'applicazione. Gli acceleratori forniscono un accesso più rapido e diretto ai comandi dei menu. Come minimo, un'applicazione deve fornire acceleratori per i comandi usati più di frequente. Anche se gli acceleratori generano in genere comandi che esistono come voci di menu, possono anche generare comandi senza voci di menu equivalenti.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Tabelle dei tasti di scelta rapida](#accelerator-tables)
-   [Creazione di tabelle di tasti di scelta rapida](#accelerator-table-creation)
-   [Assegnazioni tasti di scelta rapida](#accelerator-keystroke-assignments)
-   [Acceleratori e menu](#accelerators-and-menus)
-   [Stato dell'interfaccia utente](#ui-state)

## <a name="accelerator-tables"></a>Tabelle dei tasti di scelta rapida

Una tabella di tasti di scelta rapida è costituita da una matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) , ciascuna delle quali definisce un singolo acceleratore. Ogni struttura di **accelerazione** include le informazioni seguenti:

-   Combinazione di tasti di scelta rapida.
-   Identificatore dell'acceleratore.
-   Diversi flag. Questo include un valore che specifica se il sistema deve fornire commenti visivi evidenziando la voce di menu corrispondente, se presente, quando viene usato il tasto di scelta rapida

Per elaborare le sequenze di tasti di scelta rapida per un thread specificato, lo sviluppatore deve chiamare la funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) nel ciclo di messaggi associato alla coda di messaggi del thread. La funzione **TranslateAccelerator** monitora l'input da tastiera per la coda di messaggi, verificando la presenza di combinazioni di tasti corrispondenti a una voce nella tabella dei tasti di scelta rapida. Quando **TranslateAccelerator** trova una corrispondenza, traduce l'input da tastiera, ovvero i messaggi [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) , in un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) e quindi invia il messaggio alla routine della finestra specificata. Nella figura seguente viene illustrato il modo in cui vengono elaborati gli acceleratori.

![modello di elaborazione acceleratore tastiera](images/cskac-01.png)

Il messaggio del [**\_ comando WM**](wm-command.md) include l'identificatore del tasto di scelta rapida che ha causato la generazione del messaggio da parte di [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . La routine della finestra esamina l'identificatore per determinare l'origine del messaggio, quindi elabora il messaggio di conseguenza.

Le tabelle dei tasti di scelta rapida esistono a due livelli diversi. Il sistema mantiene un'unica tabella di tasti di scelta rapida a livello di sistema che si applica a tutte le applicazioni. Un'applicazione non può modificare la tabella dell'acceleratore di sistema. Per una descrizione degli acceleratori forniti dalla tabella acceleratore di sistema, vedere [assegnazioni di tasti di scelta rapida](#accelerator-keystroke-assignments).

Il sistema gestisce anche le tabelle di tasti di scelta rapida per ogni applicazione. Un'applicazione può definire un numero qualsiasi di tabelle di tasti di scelta rapida da usare con le proprie finestre. Un handle univoco a 32 bit (**haccel**) identifica ogni tabella. Tuttavia, è possibile attivarne una sola per volta per un thread specificato. L'handle alla tabella dei tasti di scelta rapida passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina quale tabella di tasti di scelta rapida è attiva per un thread. La tabella dei tasti di scelta rapida attiva può essere modificata in qualsiasi momento passando un handle della tabella Accelerator diverso a **TranslateAccelerator**.

## <a name="accelerator-table-creation"></a>Creazione Accelerator-Table

Sono necessari diversi passaggi per creare una tabella di tasti di scelta rapida per un'applicazione. Per prima cosa, viene usato un compilatore di risorse per creare risorse della tabella Accelerator e aggiungerle al file eseguibile dell'applicazione. In fase di esecuzione, la funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) viene utilizzata per caricare la tabella dei tasti di scelta rapida in memoria e recuperare l'handle alla tabella dei tasti di scelta rapida. Questo handle viene passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la tabella dei tasti di scelta rapida.

È anche possibile creare una tabella di tasti di scelta rapida per un'applicazione in fase di esecuzione passando una matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) alla funzione [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . Questo metodo supporta acceleratori definiti dall'utente nell'applicazione. Analogamente alla funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , **CreateAcceleratorTable** restituisce un handle della tabella dei tasti di scelta rapida che può essere passato a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la tabella dei tasti di scelta rapida.

Il sistema elimina automaticamente le tabelle dei tasti di scelta rapida caricate da [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) o create da [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Tuttavia, un'applicazione può liberare risorse mentre è in esecuzione distruggendo le tabelle dei tasti di scelta rapida non più necessarie chiamando la funzione [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

Una tabella di tasti di scelta rapida esistente può essere copiata e modificata. La tabella dei tasti di scelta rapida esistente viene copiata utilizzando la funzione [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) . Una volta modificata la copia, viene recuperato un handle per la nuova tabella di tasti di scelta rapida chiamando [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Infine, l'handle viene passato a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la nuova tabella.

## <a name="accelerator-keystroke-assignments"></a>Assegnazioni tasti di scelta rapida

Per definire il tasto di scelta rapida, è possibile usare un codice carattere ASCII o un codice di chiave virtuale. Un codice carattere ASCII rende la distinzione tra maiuscole e minuscole. Pertanto, l'utilizzo del carattere "C" ASCII definisce l'acceleratore come ALT + C anziché ALT + c. Tuttavia, gli acceleratori con distinzione tra maiuscole e minuscole possono creare confusione da usare. Ad esempio, l'acceleratore ALT + C verrà generato se il tasto BLOC MAIUSC è premuto o se il tasto MAIUSC è inattivo, ma non se entrambi sono inattivi.

In genere, gli acceleratori non devono fare distinzione tra maiuscole e minuscole, quindi la maggior parte delle applicazioni usa codici a chiave virtuale per acceleratori anziché codici di caratteri ASCII.

Evitare acceleratori che sono in conflitto con i tasti di scelta del menu di un'applicazione, perché il tasto di scelta rapida sostituisce il tasto di scelta, che può confondere l'utente. Per ulteriori informazioni sui tasti di scelta, vedere [menu](menus.md).

Se un'applicazione definisce un acceleratore definito anche nella tabella acceleratore sistema, l'acceleratore definito dall'applicazione esegue l'override di System Accelerator, ma solo all'interno del contesto dell'applicazione. Evitare questa procedura, tuttavia, perché impedisce all'acceleratore di sistema di eseguire il proprio ruolo standard nell'interfaccia utente. Gli acceleratori a livello di sistema sono descritti nell'elenco seguente:



|                  |                                                                                                       |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Passa all'applicazione successiva.                                                                     |
| ALT+F4           | Chiude un'applicazione o una finestra.                                                                    |
| ALT+segno meno       | Apre il menu **finestra** per una finestra del documento.                                                      |
| ALT + STAMP | Copia un'immagine nella finestra attiva negli Appunti.                                              |
| ALT+BARRA SPAZIATRICE     | Apre il menu **finestra** per la finestra principale dell'applicazione.                                          |
| ALT+TAB          | Passa all'applicazione successiva.                                                                     |
| CTRL + ESC         | Passa al menu **Start** .                                                                       |
| CTRL+F4          | Chiude il gruppo attivo o la finestra del documento.                                                           |
| F1               | Avvia il file della Guida dell'applicazione, se ne esiste uno.                                                    |
| SCHERMATA DI STAMPA     | Copia un'immagine sullo schermo negli Appunti.                                                     |
| MAIUSC + ALT + TAB    | Passa all'applicazione precedente. L'utente deve tenere premuto ALT + MAIUSC mentre si preme TAB. |



 

## <a name="accelerators-and-menus"></a>Acceleratori e menu

L'uso di un tasto di scelta rapida equivale alla scelta di una voce di menu: entrambe le azioni determinano l'invio di un [**\_ comando WM**](wm-command.md) o di un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) alla routine della finestra corrispondente. Il messaggio del **\_ comando WM** include un identificatore esaminato dalla routine della finestra per determinare l'origine del messaggio. Se un acceleratore ha generato il messaggio di **\_ comando WM** , l'identificatore è quello del tasto di scelta rapida. Analogamente, se una voce di menu ha generato il messaggio di **\_ comando WM** , l'identificatore è quello della voce di menu. Poiché un acceleratore fornisce un collegamento per la scelta di un comando da un menu, un'applicazione in genere assegna lo stesso identificatore all'acceleratore e alla voce di menu corrispondente.

Un'applicazione elabora un messaggio [**di \_ comando Accelerator WM**](wm-command.md) esattamente allo stesso modo della voce di menu corrispondente messaggio di **\_ comando WM** . Tuttavia, il messaggio di **\_ comando WM** contiene un flag che specifica se il messaggio proviene da un acceleratore o da una voce di menu, nel caso in cui gli acceleratori debbano essere elaborati in modo diverso rispetto alle voci di menu corrispondenti. Il messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) non contiene questo flag.

L'identificatore determina se un acceleratore genera [**un \_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Se l'identificatore ha lo stesso valore di una voce di menu nel menu di sistema, l'acceleratore genera un messaggio **WM \_ SYSCOMMAND** . In caso contrario, l'acceleratore genera un messaggio di **\_ comando WM** .

Se un acceleratore ha lo stesso identificatore di una voce di menu e la voce di menu è in grigio o è disabilitata, l'acceleratore viene disabilitato e non genera un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Inoltre, un tasto di scelta rapida non genera un messaggio di comando se la finestra corrispondente è ridotta a icona.

Quando l'utente utilizza un acceleratore che corrisponde a una voce di menu, la procedura della finestra riceve i messaggi [**WM \_ INITMENU**](wm-initmenu.md) e [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) come se l'utente avesse selezionato la voce di menu. Per informazioni su come elaborare questi messaggi, vedere [menu](menus.md).

Un acceleratore che corrisponde a una voce di menu deve essere incluso nel testo della voce di menu.

## <a name="ui-state"></a>Stato dell'interfaccia utente

Windows consente alle applicazioni di nascondere o visualizzare diverse funzionalità nell'interfaccia utente. Queste impostazioni sono note come stato dell'interfaccia utente. Lo stato dell'interfaccia utente include le impostazioni seguenti:

-   indicatori di stato attivo (ad esempio i rettangoli di attivazione sui pulsanti)
-   tasti di scelta rapida (indicati dalla sottolineatura nelle etichette dei controlli)

Una finestra può inviare messaggi per richiedere una modifica nello stato dell'interfaccia utente, può eseguire una query sullo stato dell'interfaccia utente o applicare un determinato stato per le finestre figlio. Questi messaggi sono i seguenti.



| Message                                       | Descrizione                                |
|-----------------------------------------------|--------------------------------------------|
| [**\_CHANGEUISTATE WM**](wm-changeuistate.md) | Indica che lo stato dell'interfaccia utente deve essere modificato. |
| [**\_QUERYUISTATE WM**](wm-queryuistate.md)   | Recupera lo stato dell'interfaccia utente per una finestra.       |
| [**\_UPDATEUISTATE WM**](wm-updateuistate.md) | Modifica lo stato dell'interfaccia utente.                      |



 

Per impostazione predefinita, tutte le finestre figlio di una finestra di primo livello vengono create con lo stesso stato dell'interfaccia utente dell'elemento padre.

Il sistema gestisce lo stato dell'interfaccia utente per i controlli nelle finestre di dialogo. Al momento della creazione della finestra di dialogo, il sistema Inizializza lo stato dell'interfaccia utente di conseguenza. Questo stato viene ereditato da tutti i controlli figlio. Dopo la creazione della finestra di dialogo, il sistema monitora le sequenze di tasti dell'utente. Se le impostazioni dello stato dell'interfaccia utente sono nascoste e l'utente si sposta con la tastiera, il sistema aggiorna lo stato dell'interfaccia utente. Ad esempio, se l'utente preme il tasto TAB per spostare lo stato attivo al controllo successivo, il sistema chiama [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) per rendere visibili gli indicatori di stato attivo. Se l'utente preme il tasto ALT, il sistema chiama **WM \_ CHANGEUISTATE** per rendere visibili gli acceleratori tastiera.

Se un controllo supporta la navigazione tra gli elementi dell'interfaccia utente che contiene, può aggiornare il proprio stato dell'interfaccia utente. Il controllo può chiamare [**WM \_ QUERYUISTATE**](wm-queryuistate.md) per recuperare e memorizzare nella cache lo stato iniziale dell'interfaccia utente. Ogni volta che il controllo riceve un messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) , può aggiornare lo stato dell'interfaccia utente e inviare un messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) al relativo elemento padre. Ogni finestra continuerà a inviare il messaggio al relativo padre fino a quando non raggiunge la finestra di primo livello. La finestra di primo livello invia il messaggio **WM \_ UPDATEUISTATE** a Windows nell'albero della finestra. Se una finestra non passa il messaggio **WM \_ CHANGEUISTATE** , non raggiungerà la finestra di primo livello e lo stato dell'interfaccia utente non verrà aggiornato.

 

 