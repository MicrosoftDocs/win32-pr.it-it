---
title: Panoramica dell'architettura
description: Questa panoramica dell'architettura fornisce il contesto per l'API Windows Touch per tablet e touch Technologies e spiega come si inserisce nella più ampia architettura di Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch, panoramica dell'architettura
- Windows Touch, modifiche
- Windows Touch, messaggi
- Windows Touch, inerzia
- Windows Touch, movimenti
- movimenti, informazioni
- modifiche, informazioni
- inerzia, informazioni
- processore di manipolazione, panoramica dell'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807113211d77f0aad0ed01fc24570d033063474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963099"
---
# <a name="architectural-overview"></a>Panoramica dell'architettura

Questa panoramica dell'architettura fornisce il contesto per l'API Windows Touch per tablet e touch Technologies e spiega come si inserisce nella più ampia architettura di Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Messaggi per l'input e i movimenti di Windows Touch

Le funzionalità di messaggistica per Windows Touch sono abilitate tramite l'ascolto e l'interpretazione dei messaggi durante l'esecuzione. Nella figura seguente viene illustrato come i messaggi vengono generati dall'hardware e inviati alle applicazioni da Windows 7.

![illustrazione che illustra in che modo Windows 7 Invia messaggi dall'hardware multitouch a un'applicazione](images/wm-multitouch-messaging.png)

Nella colonna più a sinistra dell'illustrazione, l'hardware sensibile al tocco riceve l'input da un utente. Un driver comunica quindi tra l'hardware e il sistema operativo. Successivamente, il sistema operativo genera un messaggio [**WM \_ touch**](wm-touchdown.md) o [**WM \_ gesture**](wm-gesture.md) che viene quindi inviato a HWND di un'applicazione. L'applicazione aggiorna quindi l'interfaccia utente in base alle informazioni incapsulate nel messaggio.

Per impostazione predefinita, le applicazioni ricevono movimenti. A meno che un'applicazione non venga registrata per i messaggi di input Windows Touch con la funzione [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , le notifiche per i movimenti (messaggi con [**\_ movimento WM**](wm-gesture.md) ) vengono create da Windows e inviate alla finestra dell'applicazione. Se una finestra dell'applicazione si registra per ricevere i messaggi di tocco, le notifiche per l'input di Windows Touch (messaggi [**WM \_ touch**](wm-touchdown.md) ) vengono inviate alla finestra dell'applicazione. I messaggi di Windows Touch e gesture sono greedy nel senso che dopo il tocco o un movimento inizia in una finestra dell'applicazione, tutti i messaggi vengono inviati a tale applicazione fino al completamento del movimento o al completamento del tocco principale.

Per il supporto legacy, Windows interpreta i messaggi di [**\_ movimento WM**](wm-gesture.md) se vengono propagati, quindi INVIeranno o pubblicheranno messaggi appropriati che eseguono il mapping al movimento. Per evitare di suddividere il supporto legacy, assicurarsi di eseguire il rollforward \_ dei messaggi con movimento WM usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Altre informazioni sul supporto legacy sono disponibili nella sezione Panoramica dei [movimenti tocco di Windows](windows-touch-gestures-overview.md).

## <a name="manipulations-and-inertia"></a>Modifiche e inerzia

I programmatori Windows Touch devono essere in grado di interpretare i movimenti da più origini in modo significativo per il movimento. Microsoft fornisce l'API di manipolazione per eseguire questi calcoli. Le modifiche sono essenzialmente movimenti con i valori associati che descrivono l'intero movimento. Dopo aver connesso i dati di input al processore di manipolazione, è possibile recuperare informazioni pertinenti all'azione che l'utente esegue sull'oggetto. Nella figura seguente viene illustrato un modo in cui è possibile utilizzare le modifiche.

![illustrazione che mostra i messaggi di Windows Touch passati al processore di manipolazione di un oggetto, che gestisce gli eventi con l' \- interfaccia IManipulationEvents](images/manipulation-arch.png)

Nell'angolo in alto a sinistra dell'illustrazione, l'utente ha toccato la schermata, che consente di creare messaggi di tocco. Questi messaggi contengono una coordinata x e una coordinata y che vengono usati per determinare l'oggetto attivo. L'oggetto in stato attivo contiene un processore di manipolazione. Successivamente, nel messaggio [**WM \_ touch**](wm-touchdown.md) con il flag **TOUCHEVENTF \_ up** , l'oggetto nello stato attivo dell'utente è selezionato, viene fatto riferimento al processore di manipolazione e il messaggio viene inviato al processore di manipolazione. I successivi messaggi **WM \_ touch** associati al contatto vengono inviati al processore di manipolazione fino a quando non viene ricevuto il messaggio **WM \_ touch** con il flag **TOUCHEVENTF \_ up** e l'oggetto selezionato viene dereferenziato. Nella sezione inferiore destra dell'illustrazione, un sink di evento di manipolazione che implementa l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) viene utilizzato per gestire gli eventi di manipolazione, che vengono generati durante la creazione dei messaggi di tocco. Il sink di evento può eseguire aggiornamenti all'interfaccia in base agli eventi di manipolazione mentre si verificano.

Nelle applicazioni Windows Touch, è comune incorporare una fisica semplice, in modo che gli oggetti si arrestino senza interruzioni, anziché arrestarsi bruscamente quando non vengono più modificati. Microsoft fornisce l'API di inerzia per eseguire i calcoli per questa semplice fisica, in modo che l'applicazione possa comportarsi in modo analogo ad altre applicazioni. Questo consente anche di risparmiare il lavoro richiesto per creare funzionalità di fisica affidabili. Nella figura seguente viene illustrato come è possibile utilizzare l'inerzia.

![illustrazione che mostra i messaggi di Windows Touch passati all'interfaccia IInertiaProcessor di un oggetto, che genera eventi con \- interfaccia IManipulationEvents](images/inertia-arch.png)

Si notino le analogie tra inerzia e manipolazione. L'unica differenza tra i due è che, nel caso di inerzia, i messaggi interpretati vengono consegnati a un processore di inerzia invece che a un processore di manipolazione e il processore di inerzia genera gli eventi. Nella parte superiore sinistra dell'illustrazione, nel messaggio [**WM \_ touch**](wm-touchdown.md) con il flag **TOUCHEVENTF \_ up** , i messaggi di tocco vengono usati per identificare un oggetto con lo stato attivo che contiene un processore di inerzia e un processore di manipolazione. I successivi messaggi **WM \_ touch** vengono inviati al processore di manipolazione e il processore di manipolazione esegue gli aggiornamenti all'interfaccia utente dell'applicazione. Al termine della manipolazione, i valori di velocità della manipolazione vengono usati per configurare un processore di inerzia. Come illustrato nella colonna centrale, il metodo [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) o [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) viene chiamato sull'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) usando un timer o un altro ciclo in un thread separato fino a quando le chiamate indicano che l'elaborazione del processore non è terminata. Durante queste chiamate vengono generati gli eventi di manipolazione, che vengono gestiti da un sink di evento di manipolazione basato sull'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) . Nella parte inferiore destra dell'illustrazione, questo sink di evento esegue quindi gli aggiornamenti all'interfaccia utente dell'applicazione in base agli eventi di manipolazione quando si verificano tramite gestori eventi nel sink di evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 