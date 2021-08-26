---
description: Windows Vista include un set di otto movimenti di sfarfallio di base. I gesti rapidi sono movimenti rapidi e lineari della penna associati ad azioni e comandi di scorrimento.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gesti sfarfallio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e7d53c42eb178900ce22b7890febcfd1c6aca95f2257b0c5ed06eb20173b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936516"
---
# <a name="flicks-gestures"></a>Gesti sfarfallio

Windows Vista include un set di otto movimenti di *sfarfallio di base.* I gesti rapidi sono movimenti rapidi e lineari della penna associati ad azioni e comandi di scorrimento.

## <a name="flick-details"></a>Dettagli di Un gesto rapido

La funzionalità dei gesti rapidi offre all'utente un nuovo modo di interagire con il Tablet PC consentendo l'esecuzione di azioni comuni tramite movimenti rapidi con la penna. I gesti rapidi coesistono e non interrompono le normali azioni dell'utente, ad esempio i tocchi sinistro e destro, lo scorrimento e l'input penna.

Un *gesto rapido* è un movimento di penna unidirezionale che richiede all'utente di contattare il digitalizzatore con un rapido movimento di sfarfallio. Un gesto rapido è caratterizzato da velocità elevata e un elevato grado di rettezza. Un gesto rapido è identificato dalla direzione. È possibile eseguire i gesti rapidi in otto direzioni corrispondenti alle direzioni della bussola cardinale e secondaria.

*Un'azione* o *un'azione di sfarfallio* è l'azione o il tasto di scelta rapida eseguito in risposta a un gesto rapido. I gesti rapidi vengono mappati alle azioni. La figura seguente mostra un diagramma di otto gesti rapidi con penna che corrispondono alle azioni di sfarfallio.

![illustrazione che mostra la mappa dei movimenti](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Quando l'utente sposta la penna sul digitalizzatore di un Tablet PC, l'hardware genera pacchetti di penna che vengono indirizzati al sottosistema di input penna della piattaforma Tablet PC. In genere, se la penna viene usata in sostituzione del mouse, il sottosistema di input della penna accetta questi pacchetti di penna e li invia, possibilmente con modifiche, a User32, il componente Windows responsabile dell'elaborazione dell'input del mouse. Se la penna viene usata su una superficie di input penna, viene eseguito il rendering dell'input penna anziché dei pacchetti del mouse generati.

La routine di rilevamento dei gesti rapidi viene implementata nel sottosistema di input penna. Il rilevamento dei gesti rapidi inizia dalla pressione della penna verso il basso e continua fino a quando:

1) la sequenza di pacchetti ricevuti viene determinata come non un gesto rapido o

2) Si verifica un pen-up.

Durante il rilevamento dei gesti rapidi, i pacchetti penna vengono mantenuti e non inviati al sistema. Questa operazione deve essere eseguita perché l'invio di pacchetti può interferire con l'azione di sfarfallio eseguita. Ad esempio, l'invio di pacchetti durante un gesto rapido che esegue il mapping a un'azione di copia ignora ciò che è stato selezionato, vale a dire che non ci sarebbe nulla da copiare al momento dell'invio dell'azione.

Man mano che i pacchetti scorrono nel sottosistema di input penna, la routine di rilevamento dei sfarfallii calcola le metriche relative a lunghezza, velocità, tempo e curvatura del movimento in esecuzione. Con ogni pacchetto che arriva, la routine di rilevamento aggiorna ognuna di queste metriche. Non appena una delle metriche non rientra in ciò che costituisce un gesto rapido, il rilevamento dei gesti rapidi termina e i pacchetti vengono inviati.

## <a name="where-flicks-are-detected"></a>Dove vengono rilevati i gesti rapidi

I movimenti di sfarfallio sono resi possibili dal fatto che i trascinamenti vengono in genere eseguiti piuttosto lentamente. L'utente deve prima impostare come destinazione il punto iniziale del trascinamento, eseguire il trascinamento e quindi puntare al punto finale. In genere questa operazione potrebbe richiedere troppo tempo per essere qualificata come un gesto rapido. Tuttavia, nelle superfici di input penna i tratti rapidi che si qualificano come gesti rapidi si verificano di frequente; L'attraversamento di una 't' è un esempio comune. Di conseguenza, per impostazione predefinita, il rilevamento dei gesti rapidi viene disattivato sulle superfici di input penna e attivato a livello di sistema.

## <a name="focus-issues"></a>Problemi di messa a fuoco

Dopo che è stato rilevato un gesto rapido, inizia una sequenza di eventi che alla fine porta il sistema a eseguire una determinata azione in risposta al gesto rapido che si è verificato. In primo luogo, la routine di rilevamento all'interno del sottosistema di input penna determina a quale finestra deve essere inviato il gesto rapido. Questa è in genere la finestra con lo stato attivo, ma esistono eccezioni. Per i gesti rapidi di scorrimento, il gesto rapido viene inviato alla finestra su cui si è verificato il gesto. Si noti che questa non è necessariamente la finestra con lo stato attivo. Quando viene inviato un gesto rapido a una finestra che non ha lo stato attivo, lo stato attivo non cambia in tale finestra.

## <a name="flick-actions"></a>Azioni di sfarfallio

Una volta determinata la finestra di destinazione, tale finestra può gestire il gesto rapido a seconda del comportamento predefinito o programmato dell'evento. Le applicazioni possono rispondere all'azione più appropriata in base all'applicazione e alla direzione e alla posizione del gesto rapido. In un'applicazione di mapping, ad esempio, i gesti rapidi verso l'alto e verso il basso potrebbero fare zoom avanti o indietro anziché scorrere verticalmente, come previsto dal comportamento predefinito.

Per avvisare un'applicazione che si è verificato un gesto rapido, viene inviato un messaggio di finestra. Questo messaggio della finestra contiene sia il punto iniziale del gesto rapido che la direzione del gesto. Se l'applicazione gestisce questo messaggio della finestra, il sottosistema di input penna non intraprese altre azioni.

Dopo aver rilevato un gesto rapido, sullo schermo viene visualizzato un feedback visivo che rappresenta l'azione di sfarfallio. Questo feedback ha due scopi. In primo luogo, conferma all'utente che il gesto rapido ha avuto esito positivo. In secondo momento, ricorda all'utente quale azione è stata eseguita, consentendo all'utente di connettere la direzione del gesto rapido all'azione associata.

Il feedback sui gesti rapidi è costituito da due parti: un'icona che rappresenta l'azione e un'etichetta contenente il nome dell'azione. L'etichetta viene visualizzata sotto l'icona. Il feedback viene visualizzato immediatamente dopo che è stato rilevato il gesto rapido. Anche se le applicazioni possono personalizzare il comportamento in risposta ai gesti rapidi gestendo il messaggio della finestra di gestibilità, l'applicazione non può disabilitare o modificare il feedback dei gesti rapidi.

È previsto che la maggior parte delle applicazioni non sia in grado di riconoscere lo sfarfallio e quindi non gestirà il messaggio della finestra descritto in precedenza. Se il messaggio non viene gestito, il sottosistema di input penna deve eseguire altre azioni. In primo luogo, cerca l'azione associata alla direzione del gesto rapido rilevato. Successivamente, eseguirà i passaggi descritti nella tabella seguente per fare in modo che la finestra di destinazione esecriva questa azione. Per molte delle azioni di scorrimento rapido ciò comporta l'invio di un comando dell'applicazione, ma alcune azioni implementate non lo fanno.

## <a name="processing-application-commands"></a>Elaborazione dei comandi dell'applicazione

L'applicazione deve rispondere a uno qualsiasi dei comandi dell'applicazione che potrebbero essere potenzialmente assegnati a un movimento di sfarfallio. Se un'applicazione non risponde al messaggio [**WM \_ TABLET \_ FLICK,**](wm-tablet-flick-message.md)Windows Vista segue inviando la notifica [**\_ APPCOMMAND WM**](/windows/desktop/inputdev/wm-appcommand) applicabile, seguita da una notifica WM [**\_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)

Di seguito è riportato un elenco di comandi dell'applicazione che possono essere assegnati ai gesti rapidi, con il messaggio di sequenza di tasti di backup che potrebbe essere inviato.



| Comando                                  | Sequenza di tasti di backup  |
|------------------------------------------|-------------------|
| APPCOMMAND \_ BROWSER \_ BACKWARD<br/> | Nessuno<br/>   |
| APPCOMMAND \_ BROWSER \_ FORWARD<br/>  | Nessuno<br/>   |
| COPIA \_ DI APPCOMMAND<br/>              | CTRL+C<br/> |
| INCOLLA \_ DI APPCOMMAND<br/>             | CTRL+V<br/> |
| APPCOMMAND \_ UNDO<br/>              | CTRL+Z<br/> |
| APPCOMMAND \_ DELETE<br/>            | CANC<br/>    |
| APPCOMMAND \_ CUT<br/>               | CTRL+X<br/> |
| APPCOMMAND \_ OPEN<br/>              | CTRL+O<br/> |
| APPCOMMAND \_ PRINT<br/>             | Ctrl+P<br/> |
| APPCOMMAND \_ SAVE<br/>              | CTRL+S<br/> |
| APPCOMMAND \_ REDO<br/>              | CTRL+Y<br/> |
| CHIUSURA \_ DI APPCOMMAND<br/>             |                   |



 

I comandi di modifica, ad esempio Copia, Incolla, Taglia e Elimina, possono essere indirizzati a una selezione o all'oggetto posizionato alla base del movimento di tocco. Se non è presente alcuna selezione, è possibile usare i dati nella struttura [**FLICK \_ POINT**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) per determinare quale, se presente, oggetto potrebbe essere stato la destinazione del comando di modifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API di gesti rapidi](flicks-api-reference.md)
</dt> <dt>

[Risposta ai movimenti di sfarfallio](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

