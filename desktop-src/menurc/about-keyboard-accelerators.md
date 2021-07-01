---
title: Informazioni sui tasti di scelta rapida
description: Questo argomento illustra i tasti di scelta rapida.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,tasti di scelta rapida
- input utente, tasti di scelta rapida
- acquisizione dell'input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- Acceleratori
- WM_COMMAND messaggio
- WM_SYS comando di comando
- tabelle dei tasti di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e97f0b4997d15d55601e571270276e7d7a3bd4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120376"
---
# <a name="about-keyboard-accelerators"></a>Informazioni sui tasti di scelta rapida

Gli acceleratori sono strettamente correlati ai menu, entrambi consentono all'utente di accedere al set di comandi di un'applicazione. In genere, gli utenti si basano sui menu di un'applicazione per apprendere il set di comandi e quindi passare all'uso di acceleratori non appena diventano più esperti con l'applicazione. Gli acceleratori offrono un accesso più rapido e diretto ai comandi rispetto ai menu. Come minimo, un'applicazione deve fornire acceleratori per i comandi usati più di frequente. Anche se i tasti di scelta rapida in genere generano comandi che esistono come voci di menu, possono anche generare comandi che non hanno voci di menu equivalenti.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Tabelle dei tasti di scelta rapida](#accelerator-tables)
-   [Creazione di una tabella di tasti di scelta rapida](#accelerator-table-creation)
-   [Assegnazioni di tasti di scelta rapida](#accelerator-keystroke-assignments)
-   [Tasti di scelta rapida e menu](#accelerators-and-menus)
-   [Stato dell'interfaccia utente](#ui-state)

## <a name="accelerator-tables"></a>Tabelle dei tasti di scelta rapida

Una tabella dei tasti di scelta rapida è costituita da una matrice [**di strutture ACCEL,**](/windows/win32/api/winuser/ns-winuser-accel) ognuna delle quali definisce un singolo acceleratore. Ogni **struttura ACCEL** include le informazioni seguenti:

-   Combinazione di tasti del tasto di scelta rapida.
-   Identificatore del tasto di scelta rapida.
-   Vari flag. Ne è inclusa una che specifica se il sistema deve fornire feedback visivo evidenziando la voce di menu corrispondente, se presente, quando viene usato l'acceleratore

Per elaborare le sequenze di tasti di scelta rapida per un thread specificato, lo sviluppatore deve chiamare la funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) nel ciclo di messaggi associato alla coda di messaggi del thread. La **funzione TranslateAccelerator** monitora l'input della tastiera nella coda di messaggi, verificando la presenza di combinazioni di tasti corrispondenti a una voce nella tabella dei tasti di scelta rapida. Quando **TranslateAccelerator** trova una corrispondenza, converte l'input da tastiera (ovvero i messaggi [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KEYDOWN)**](/windows/desktop/inputdev/wm-keydown) in un messaggio [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) e quindi invia il messaggio alla routine della finestra della finestra specificata. Nella figura seguente viene illustrato come vengono elaborati i tasti di scelta rapida.

![modello di elaborazione dei tasti di scelta rapida](images/cskac-01.png)

Il [**messaggio WM \_ COMMAND**](wm-command.md) include l'identificatore dell'acceleratore che ha causato la generazione del messaggio da parte di [**TranslateAccelerator.**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) La routine della finestra esamina l'identificatore per determinare l'origine del messaggio e quindi elabora il messaggio di conseguenza.

Le tabelle dei tasti di scelta rapida esistono a due livelli diversi. Il sistema gestisce una singola tabella dei tasti di scelta rapida a livello di sistema che si applica a tutte le applicazioni. Un'applicazione non può modificare la tabella dei tasti di scelta rapida di sistema. Per una descrizione dei tasti di scelta rapida forniti dalla tabella dei tasti di scelta rapida di sistema, vedere [Assegnazioni di tasti di scelta rapida.](#accelerator-keystroke-assignments)

Il sistema gestisce anche le tabelle dei tasti di scelta rapida per ogni applicazione. Un'applicazione può definire un numero qualsiasi di tabelle dei tasti di scelta rapida da usare con le proprie finestre. Un handle univoco a 32 bit (**HACCEL**) identifica ogni tabella. Tuttavia, per un thread specificato può essere attiva una sola tabella dei tasti di scelta rapida alla volta. L'handle per la tabella dei tasti di scelta rapida passata alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina quale tabella dei tasti di scelta rapida è attiva per un thread. La tabella dei tasti di scelta rapida attiva può essere modificata in qualsiasi momento passando un handle di tabella di tasti di scelta rapida diverso **a TranslateAccelerator.**

## <a name="accelerator-table-creation"></a>Accelerator-Table creazione

Per creare una tabella dei tasti di scelta rapida per un'applicazione sono necessari diversi passaggi. In primo luogo, viene usato un compilatore di risorse per creare risorse accelerator-table e aggiungerle al file eseguibile dell'applicazione. In fase di esecuzione, la [**funzione LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) viene usata per caricare la tabella dei tasti di scelta rapida in memoria e recuperare l'handle per la tabella dei tasti di scelta rapida. Questo handle viene passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la tabella dei tasti di scelta rapida.

È anche possibile creare una tabella dei tasti di scelta rapida per un'applicazione in fase di esecuzione passando una matrice di strutture [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) alla [**funzione CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Questo metodo supporta gli acceleratori definiti dall'utente nell'applicazione. Analogamente alla [**funzione LoadAccelerators,**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) **CreateAcceleratorTable** restituisce un handle di tabella dei tasti di scelta rapida che può essere passato a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la tabella dei tasti di scelta rapida.

Il sistema elimina automaticamente le tabelle dei tasti di scelta rapida caricate da [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) o create da [**CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Tuttavia, un'applicazione può liberare risorse mentre è in esecuzione, eliminando le tabelle dei tasti di scelta rapida non più necessarie chiamando la [**funzione DestroyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)

Una tabella dei tasti di scelta rapida esistente può essere copiata e modificata. La tabella dei tasti di scelta rapida esistente viene copiata tramite [**la funzione CopyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) Dopo la modifica della copia, viene recuperato un handle per la nuova tabella dei tasti di scelta rapida chiamando [**CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Infine, l'handle viene passato [**a TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) per attivare la nuova tabella.

## <a name="accelerator-keystroke-assignments"></a>Assegnazioni di tasti di scelta rapida

È possibile usare un codice carattere ASCII o un codice tasto virtuale per definire l'acceleratore. Un codice carattere ASCII fa distinzione tra maiuscole e minuscole per l'acceleratore. Pertanto, l'uso del carattere ASCII "C" definisce l'acceleratore come ALT+C anziché ALT+C. Tuttavia, gli acceleratori con distinzione tra maiuscole e minuscole possono generare confusione nell'uso. Ad esempio, l'acceleratore ALT+C verrà generato se il tasto BLOC MAIUSC è premuto o se maiusc è premuto, ma non se entrambi sono in giù.

In genere, gli acceleratori non devono fare distinzione tra maiuscole e minuscole, quindi la maggior parte delle applicazioni usa codici di tasti virtuali per i tasti di scelta rapida anziché codici di carattere ASCII.

Evitare i tasti di scelta rapida che sono in conflitto con i tasti di scelta rapida di un'applicazione, perché l'acceleratore esegue l'override del tasto di scelta rapida, confondendo l'utente. Per altre informazioni sui menu, vedere [Menu.](menus.md)

Se un'applicazione definisce un acceleratore definito anche nella tabella dei tasti di scelta rapida di sistema, l'acceleratore definito dall'applicazione esegue l'override dell'acceleratore di sistema, ma solo all'interno del contesto dell'applicazione. Evitare questa procedura, tuttavia, perché impedisce all'acceleratore di sistema di eseguire il proprio ruolo standard nell'interfaccia utente. Gli acceleratori a livello di sistema sono descritti nell'elenco seguente:



| Acceleratore                 | Descrizione                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Passa all'applicazione successiva.                                                                     |
| ALT+F4           | Chiude un'applicazione o una finestra.                                                                    |
| ALT+segno meno       | Apre il menu **Finestra** per una finestra del documento.                                                      |
| ALT+STAMPA SCHERMATA | Copia un'immagine nella finestra attiva negli Appunti.                                              |
| ALT+BARRA SPAZIATRICE     | Apre il menu **Finestra** per la finestra principale dell'applicazione.                                          |
| ALT+TAB          | Passa all'applicazione successiva.                                                                     |
| CTRL+ESC         | Passa al menu **Start.**                                                                       |
| CTRL+F4          | Chiude la finestra del documento o del gruppo attivo.                                                           |
| F1               | Avvia il file della Guida dell'applicazione, se esistente.                                                    |
| SCHERMATA DI STAMPA     | Copia un'immagine sullo schermo negli Appunti.                                                     |
| MAIUSC+ALT+TAB    | Passa all'applicazione precedente. L'utente deve tenere premuto ALT+MAIUSC mentre preme TAB. |



 

## <a name="accelerators-and-menus"></a>Tasti di scelta rapida e menu

L'uso di un tasto di scelta rapida è uguale alla scelta di una voce di menu: entrambe le azioni determinano l'invio di un messaggio [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) alla routine della finestra corrispondente. Il **messaggio WM \_ COMMAND** include un identificatore esaminato dalla routine della finestra per determinare l'origine del messaggio. Se un tasto di scelta rapida ha **generato il messaggio WM \_ COMMAND,** l'identificatore è quello dell'acceleratore. Analogamente, se una voce di menu ha generato il **messaggio WM \_ COMMAND,** l'identificatore è quello della voce di menu. Poiché un tasto di scelta rapida fornisce un tasto di scelta rapida per la scelta di un comando da un menu, un'applicazione assegna in genere lo stesso identificatore al tasto di scelta rapida e alla voce di menu corrispondente.

Un'applicazione elabora un messaggio [**WM \_ COMMAND dell'acceleratore**](wm-command.md) esattamente come il messaggio **WM \_ COMMAND** della voce di menu corrispondente. Tuttavia, il messaggio **WM \_ COMMAND** contiene un flag che specifica se il messaggio ha avuto origine da un tasto di scelta rapida o da una voce di menu, nel caso in cui i tasti di scelta rapida devono essere elaborati in modo diverso dalle voci di menu corrispondenti. Il [**messaggio \_ SYSCOMMAND WM**](wm-syscommand.md) non contiene questo flag.

L'identificatore determina se un tasto di scelta rapida genera [**un messaggio WM \_ COMMAND**](wm-command.md) [**o WM \_ SYSCOMMAND.**](wm-syscommand.md) Se l'identificatore ha lo stesso valore di una voce di menu nel menu Sistema, l'acceleratore genera un **messaggio \_ SYSCOMMAND WM.** In caso contrario, l'acceleratore genera **un messaggio WM \_ COMMAND.**

Se un tasto di scelta rapida ha lo stesso identificatore di una voce di menu e la voce di menu è disattivata o disabilitata, l'acceleratore è disabilitato e non genera un messaggio [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND.**](wm-syscommand.md) Inoltre, un tasto di scelta rapida non genera un messaggio di comando se la finestra corrispondente è ridotta a icona.

Quando l'utente usa un tasto di scelta rapida che corrisponde a una voce di menu, la routine della finestra riceve i messaggi [**\_ WM INITMENU**](wm-initmenu.md) e [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) come se l'utente avesse selezionato la voce di menu. Per informazioni su come elaborare questi messaggi, vedere [Menu.](menus.md)

Un tasto di scelta rapida che corrisponde a una voce di menu deve essere incluso nel testo della voce di menu.

## <a name="ui-state"></a>Stato dell'interfaccia utente

Windows consente alle applicazioni di nascondere o visualizzare varie funzionalità nell'interfaccia utente. Queste impostazioni sono note come stato dell'interfaccia utente. Lo stato dell'interfaccia utente include le impostazioni seguenti:

-   indicatori di stato attivo (ad esempio rettangoli di attivazione sui pulsanti)
-   tasti di scelta rapida (indicati da sottolineature nelle etichette dei controlli)

Una finestra può inviare messaggi per richiedere una modifica dello stato dell'interfaccia utente, eseguire query sullo stato dell'interfaccia utente o applicare un determinato stato per le finestre figlio. Questi messaggi sono i seguenti.



| Message                                       | Descrizione                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Indica che lo stato dell'interfaccia utente deve cambiare. |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Recupera lo stato dell'interfaccia utente per una finestra.       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Modifica lo stato dell'interfaccia utente.                      |



 

Per impostazione predefinita, tutte le finestre figlio di una finestra di primo livello vengono create con lo stesso stato dell'interfaccia utente dell'elemento padre.

Il sistema gestisce lo stato dell'interfaccia utente per i controlli nelle finestre di dialogo. Al momento della creazione della finestra di dialogo, il sistema inizializza lo stato dell'interfaccia utente di conseguenza. Tutti i controlli figlio ereditano questo stato. Dopo aver creato la finestra di dialogo, il sistema monitora le sequenze di tasti dell'utente. Se le impostazioni dello stato dell'interfaccia utente sono nascoste e l'utente si sposta usando la tastiera, il sistema aggiorna lo stato dell'interfaccia utente. Ad esempio, se l'utente preme TAB per spostare lo stato attivo sul controllo successivo, il sistema chiama [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) per rendere visibili gli indicatori dello stato attivo. Se l'utente preme alt, il sistema chiama **WM \_ CHANGEUISTATE** per rendere visibili i tasti di scelta rapida.

Se un controllo supporta lo spostamento tra gli elementi dell'interfaccia utente che contiene, può aggiornare il proprio stato dell'interfaccia utente. Il controllo può chiamare [**WM \_ QUERYUISTATE per**](wm-queryuistate.md) recuperare e memorizzare nella cache lo stato iniziale dell'interfaccia utente. Ogni volta che il controllo riceve un [**messaggio WM \_ UPDATEUISTATE,**](wm-updateuistate.md) può aggiornare lo stato dell'interfaccia utente e inviare un messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) al relativo elemento padre. Ogni finestra continuerà a inviare il messaggio al relativo elemento padre fino a raggiungere la finestra di primo livello. La finestra di primo livello invia il **messaggio \_ WM UPDATEUISTATE** alle finestre nell'albero della finestra. Se una finestra non passa il messaggio **WM \_ CHANGEUISTATE,** non raggiungerà la finestra di primo livello e lo stato dell'interfaccia utente non verrà aggiornato.

 

 