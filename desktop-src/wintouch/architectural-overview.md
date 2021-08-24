---
title: Panoramica dell'architettura
description: Questa panoramica dell'architettura fornisce il contesto per l'API Windows Touch per tablet e tecnologie di tocco e spiega come si inserisce nell'architettura Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Tocco, panoramica dell'architettura
- Windows Tocco, manipolazioni
- Windows Tocco, messaggi
- Windows Tocco, inerzia
- Windows Tocco, movimenti
- movimenti, informazioni
- manipolazioni, informazioni
- inerzia, informazioni
- processore di manipolazione, panoramica dell'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5ce003c88a66e96072fa9f96bc6ae73bd91cb39f53e03ab3748dd14a194d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448675"
---
# <a name="architectural-overview"></a>Panoramica dell'architettura

Questa panoramica dell'architettura fornisce il contesto per l'API Windows Touch per tablet e tecnologie di tocco e spiega come si inserisce nell'architettura Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Messaggi per Windows input tocco e movimenti

Le funzionalità di messaggistica Windows Touch vengono abilitate mediante l'ascolto e l'interpretazione dei messaggi durante l'esecuzione. Nella figura seguente viene illustrato come i messaggi vengono generati dall'hardware e inviati alle applicazioni Windows 7.

![illustrazione che mostra come Windows 7 invia messaggi dall'hardware multitocco a un'applicazione](images/wm-multitouch-messaging.png)

Nella colonna più a sinistra dell'illustrazione, l'hardware sensibile al tocco riceve l'input da un utente. Un driver comunica quindi tra l'hardware e il sistema operativo. Successivamente, il sistema operativo genera un [**messaggio WM \_ TOUCH**](wm-touchdown.md) o [**WM \_ GESTURE**](wm-gesture.md) che viene quindi inviato all'oggetto HWND di un'applicazione. L'applicazione aggiorna quindi l'interfaccia utente in base alle informazioni incapsulate nel messaggio.

Le applicazioni ricevono movimenti per impostazione predefinita. A meno che un'applicazione non si registri per i messaggi di input Windows Touch con la funzione [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) le notifiche per i movimenti (messaggi [**WM \_ GESTURE)**](wm-gesture.md) vengono create da Windows e inviate a tale finestra dell'applicazione. Se un'applicazione Window si registra per ricevere messaggi di tocco, le notifiche per l Windows input tocco (messaggi [**WM \_ TOUCH)**](wm-touchdown.md) vengono inviate a tale finestra dell'applicazione. Windows I messaggi di tocco e movimento sono greedy, nel senso che dopo che è stato effettuato un tocco o un movimento ha inizio in una finestra dell'applicazione, tutti i messaggi vengono inviati a tale applicazione fino al completamento del movimento o al completamento del tocco principale.

Per il supporto legacy, Windows interpreta i messaggi [**WM \_ GESTURE**](wm-gesture.md) se vengono visualizzati a bolle e quindi invia o PUBBLICA messaggi appropriati mappati al movimento. Per evitare di interrompere il supporto legacy, assicurarsi di inoltrare i messaggi WM \_ GESTURE usando [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Altre informazioni sul supporto legacy sono disponibili nella sezione Windows [Touch Gestures Overview](windows-touch-gestures-overview.md)( Panoramica dei movimenti tocco).

## <a name="manipulations-and-inertia"></a>Modifiche e inerzia

Windows I programmatori di tocco devono essere in grado di interpretare i movimenti da più origini in modo significativo per il movimento in corso. Microsoft fornisce l'API di manipolazione per eseguire questi calcoli. Le manipolazioni sono essenzialmente movimenti con valori associati che descrivono l'intero movimento. Dopo aver connesso i dati di input al processore di manipolazione, è possibile recuperare le informazioni pertinenti all'azione eseguita dall'utente sull'oggetto. La figura seguente illustra un modo per usare le modifiche.

![illustrazione che mostra i messaggi di tocco di Windows passati al processore di manipolazione di un oggetto, che gestisce gli eventi con \- l'interfaccia imanipulationevents](images/manipulation-arch.png)

In alto a sinistra nell'illustrazione l'utente ha toccato lo schermo, che crea messaggi di tocco. Questi messaggi contengono una coordinata x e una coordinata y utilizzate per determinare l'oggetto attivo. L'oggetto nello stato attivo contiene un processore di manipolazione. Successivamente, nel messaggio [**WM \_ TOUCH**](wm-touchdown.md) con il flag **TOUCHEVENTF \_ UP** viene selezionato l'oggetto nello stato attivo dell'utente, viene fatto riferimento al processore di manipolazione e il messaggio viene inviato al processore di manipolazione. I **successivi \_ messaggi WM TOUCH** associati a questo contatto vengono inviati al processore di manipolazione finché non viene ricevuto il messaggio WM **\_ TOUCH** con il flag **TOUCHEVENTF \_ UP** e non viene dereferenziato l'oggetto selezionato. Nella sezione inferiore destra dell'illustrazione viene usato un sink di evento di manipolazione che implementa l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) per gestire gli eventi di manipolazione, che vengono generati durante la creazione dei messaggi di tocco. Il sink di evento può eseguire aggiornamenti all'interfaccia in base agli eventi di manipolazione mentre si verificano.

Nelle Windows Touch è comune incorporare la fisica semplice in modo che gli oggetti si arrestino senza problemi, anziché arrestarsi improvvisamente quando non vengono più toccati. Microsoft fornisce l'API Inertia per eseguire i calcoli per questa semplice fisica in modo che l'applicazione possa comportarsi in modo simile ad altre applicazioni. Ciò consente anche di risparmiare il lavoro necessario per creare solide funzionalità fisiche. La figura seguente illustra come usare l'inerzia.

![illustrazione che mostra i messaggi di tocco di Windows passati all'interfaccia iinertiaprocessor di un oggetto, che genera eventi con \- l'interfaccia imanipulationevents](images/inertia-arch.png)

Si notino le analogie tra inerzia e manipolazione. L'unica differenza tra i due è che, in caso di inerzia, i messaggi interpretati vengono inviati a un processore di inerzia anziché a un processore di manipolazione e il processore di inerzia genera gli eventi. Nella parte superiore sinistra dell'illustrazione, nel messaggio [**WM \_ TOUCH**](wm-touchdown.md) con il flag **TOUCHEVENTF \_ UP,** i messaggi tocco vengono usati per identificare un oggetto nello stato attivo che contiene un processore di inerzia e un processore di manipolazione. I **messaggi WM TOUCH \_ successivi** vengono inviati al processore di manipolazione e il processore di manipolazione esegue gli aggiornamenti all'interfaccia utente dell'applicazione. Al termine della manipolazione, i valori di velocità della manipolazione vengono usati per configurare un processore di inerzia. Come illustrato nella colonna centrale, il metodo [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) o [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) viene chiamato sull'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) usando un timer o un altro ciclo in un thread separato fino a quando le chiamate non indicano che il processore ha terminato l'elaborazione. Mentre vengono effettuate queste chiamate, vengono generati eventi di manipolazione, che vengono gestiti da un sink di eventi di manipolazione basato [**\_ sull'interfaccia IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Nella sezione inferiore destra dell'illustrazione questo sink di evento esegue quindi gli aggiornamenti all'interfaccia utente dell'applicazione in base agli eventi di manipolazione quando si verificano tramite gestori eventi nel sink di evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 