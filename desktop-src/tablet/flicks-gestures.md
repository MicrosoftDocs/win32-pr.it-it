---
description: Windows Vista include un set di otto movimenti di scorrimento di base. I gesti rapidi sono movimenti di penna veloci e lineari associati a comandi e azioni di scorrimento.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Movimenti rapidi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85d519f47b265779741b2f98fcb1b2f5d69df5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570155"
---
# <a name="flicks-gestures"></a>Movimenti rapidi

Windows Vista include un set di otto *movimenti di scorrimento* di base. I gesti rapidi sono movimenti di penna veloci e lineari associati a comandi e azioni di scorrimento.

## <a name="flick-details"></a>Dettagli tocco

La funzionalità gesti rapidi fornisce all'utente un nuovo modo per interagire con il Tablet PC consentendo l'esecuzione di azioni comuni mediante la creazione di movimenti rapidi con la penna. I gesti rapidi coesisteranno con e non interferiscono con le normali azioni dell'utente, ad esempio i rubinetti sinistro e destro, lo scorrimento e l'Inking.

Un *gesto rapido è un* gesto di penna unidirezionale che richiede all'utente di contattare il digitalizzatore in un rapido movimento di scorrimento. Un gesto rapido è caratterizzato da alta velocità e da un elevato grado di unidritità. Un gesto rapido viene identificato in base alla direzione. I gesti rapidi possono essere eseguiti in otto direzioni corrispondenti alle direzioni Cardinal e secondaria della bussola.

Un' *azione o un gesto* *rapido* è l'azione o il collegamento eseguito in risposta a un gesto rapido. Viene eseguito il mapping di gesti rapidi alle azioni. Nella figura seguente viene illustrato un diagramma di otto gesti rapidi penna che corrispondono alle azioni rapide.

![illustrazione che mostra la mappa movimenti](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Quando l'utente sposta la penna sul digitalizzatore di un Tablet PC, l'hardware genera pacchetti penna che vengono indirizzati al sottosistema di input penna della piattaforma Tablet PC. In genere, se la penna viene usata come sostituto del mouse, il sottosistema di input penna accetta questi pacchetti penna e li invia, possibilmente con modifiche, a User32, il componente di Windows responsabile dell'elaborazione dell'input del mouse. Se la penna viene utilizzata su una superficie di Inking, viene eseguito il rendering dell'input penna anziché i pacchetti del mouse generati.

La routine di rilevamento rapido è implementata nel sottosistema di input penna. Il rilevamento rapido inizia alla penna e continua fino a:

1) la sequenza di pacchetti ricevuti viene determinata in modo da non essere un gesto rapido o

2) si verifica la penna.

Mentre è in corso il rilevamento rapido, i pacchetti di penna vengono mantenuti e non inviati al sistema. Questa operazione deve essere eseguita perché l'invio di pacchetti può interferire con l'azione di scorrimento rapido eseguita. Se, ad esempio, si inviano pacchetti durante un gesto rapido che esegue il mapping a un'azione di copia, si ignora ciò che è stato selezionato, ovvero non ci sono elementi da copiare nel momento in cui l'azione è stata inviata.

Quando i pacchetti vengono propagati nel sottosistema di input penna, la routine di rilevamento rapido calcola le metriche relative alla lunghezza, alla velocità, al tempo e alla curvatura del movimento eseguito. Con ogni pacchetto che arriva, la routine di rilevamento aggiorna ogni metrica. Non appena una delle metriche si trova al di fuori di quello che costituirebbe un gesto rapido, il rilevamento del gesto rapido termina e i pacchetti vengono inviati tramite.

## <a name="where-flicks-are-detected"></a>Dove vengono rilevati i gesti rapidi

I movimenti rapidi sono resi possibili dal fatto che i trascinamenti vengono in genere eseguiti piuttosto lentamente. L'utente deve prima avere come destinazione il punto iniziale del trascinamento, eseguire il trascinamento e quindi definire come destinazione il punto finale. Normalmente questa operazione richiederà troppo tempo per essere qualificata come un gesto rapido. Tuttavia, in caso di Inking, i tratti rapidi che sarebbero idonei ai gesti rapidi si verificano di frequente; il passaggio a' t'è un esempio comune. Pertanto, per impostazione predefinita, il rilevamento rapido viene disattivato sulle superfici di Inking e attivato a livello di sistema.

## <a name="focus-issues"></a>Problemi di stato attivo

Una volta rilevato un gesto rapido, viene avviata una sequenza di eventi che in definitiva conduce al sistema che esegue una determinata azione in risposta al Flick che si è verificato. In primo luogo, la routine di rilevamento all'interno del sottosistema di input penna determina la finestra a cui deve essere inviato il gesto rapido. Si tratta in genere della finestra con lo stato attivo, ma vi sono eccezioni. Per scorrere i gesti rapidi, il flick viene inviato alla finestra su cui si è verificato il movimento. Si noti che questo non è necessariamente la finestra con lo stato attivo. Quando viene inviato un gesto rapido a una finestra che non ha lo stato attivo, lo stato attivo non cambia in tale finestra.

## <a name="flick-actions"></a>Azioni di gesto rapido

Una volta determinata la finestra di destinazione, la finestra potrebbe gestire il flick a seconda del comportamento predefinito o programmato dell'evento. Le applicazioni possono rispondere all'azione più appropriata in base all'applicazione e alla direzione e alla posizione del gesto rapido. Ad esempio, in un'applicazione di mapping, i gesti rapidi verso l'alto e verso il basso possono eseguire lo zoom avanti o indietro anziché scorrere verticalmente, come previsto dal comportamento predefinito.

Per avvertire un'applicazione che si è verificato un gesto rapido, viene inviato un messaggio di finestra. Questo messaggio di finestra contiene sia il punto iniziale del gesto rapido che la direzione del movimento rapido. Se l'applicazione gestisce questo messaggio della finestra, non viene eseguita alcuna azione ulteriore da parte del sottosistema di input penna.

Dopo aver rilevato un gesto rapido, viene visualizzato un feedback visivo che rappresenta l'azione di scorrimento rapido sullo schermo. Questo feedback ha due scopi. Prima di tutto, conferma che l'utente ha avuto esito positivo. In secondo luogo, ricorda all'utente quale azione è stata eseguita, consentendo all'utente di connettere la direzione di scorrimento con l'azione associata.

Il feedback rapido è costituito da due parti: icona che rappresenta l'azione e un'etichetta contenente il nome dell'azione. L'etichetta viene visualizzata sotto l'icona. Il feedback viene visualizzato immediatamente dopo che è stato rilevato il gesto rapido. Sebbene le applicazioni possano personalizzare il proprio comportamento in risposta ai gesti rapidi gestendo il messaggio della finestra di scorrimento rapido, l'applicazione non può disabilitare o modificare il feedback rapido.

Si prevede che la maggior parte delle applicazioni non sarà in grado di riconoscere il tocco e pertanto non gestirà il messaggio della finestra descritto in precedenza. Se il messaggio non viene gestito, il sottosistema di input penna eseguirà ulteriori azioni. Prima di tutto, Cerca l'azione associata alla direzione del movimento rapido rilevato. Successivamente, verrà eseguita la procedura descritta nella tabella seguente per fare in modo che la finestra di destinazione esegua l'azione. Per molte delle azioni rapide, questo comporta l'invio di un comando dell'applicazione, ma non alcune azioni implementate.

## <a name="processing-application-commands"></a>Elaborazione dei comandi dell'applicazione

L'applicazione deve rispondere a tutti i comandi dell'applicazione che potrebbero essere potenzialmente assegnati a un gesto rapido. Se un'applicazione non riesce a rispondere al [**\_ messaggio di \_ scorrimento rapido del Tablet WM**](wm-tablet-flick-message.md), Windows Vista viene seguito inviando la notifica [**\_ APPCOMMAND di WM**](/windows/desktop/inputdev/wm-appcommand) applicabile, seguito da una notifica di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) .

Di seguito è riportato un elenco di comandi dell'applicazione che possono essere assegnati ai gesti rapidi, con il messaggio di sequenza di tasti di backup che può essere inviato.



| Comando                                  | Sequenza di tasti di backup  |
|------------------------------------------|-------------------|
| \_browser APPCOMMAND \_ indietro<br/> | nessuno<br/>   |
| APPCOMMAND \_ browser \_ in futuro<br/>  | nessuno<br/>   |
| copia di APPCOMMAND \_<br/>              | CTRL+C<br/> |
| \_Incolla APPCOMMAND<br/>             | CTRL+V<br/> |
| \_Annulla APPCOMMAND<br/>              | CTRL+Z<br/> |
| eliminazione di APPCOMMAND \_<br/>            | CANC<br/>    |
| \_taglia APPCOMMAND<br/>               | CTRL+X<br/> |
| APPCOMMAND \_ aperto<br/>              | CTRL+O<br/> |
| \_stampa APPCOMMAND<br/>             | Ctrl+P<br/> |
| \_Salva APPCOMMAND<br/>              | CTRL+S<br/> |
| \_ripetizione APPCOMMAND<br/>              | CTRL+Y<br/> |
| chiusura di APPCOMMAND \_<br/>             |                   |



 

La modifica di comandi quali copy, paste, Cut ed delete può essere indirizzata a una selezione o all'oggetto posizionato alla base del movimento di scorrimento rapido. Se non è presente alcuna selezione, è possibile usare i dati nella [**\_ struttura del punto di scorrimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) per determinare l'eventuale oggetto che potrebbe essere stato la destinazione del comando di modifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API](flicks-api-reference.md)
</dt> <dt>

[Risposta a movimenti rapidi](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

