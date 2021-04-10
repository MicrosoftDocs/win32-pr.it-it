---
description: Sessioni audio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sessioni audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ae67a3eafe7a76add2fad192823868304e860d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127674"
---
# <a name="audio-sessions"></a>Sessioni audio

Una *sessione audio* è un gruppo di flussi audio correlati che un client WASAPI può gestire collettivamente. I client possono controllare il livello di volume e lo stato di muting di ogni singola sessione. Il sistema applica in modo uniforme le impostazioni relative al volume e al silenziamento specificate dal client a tutti i flussi della sessione.

Quando un client Inizializza un flusso audio, assegna il flusso audio a una sessione audio. Per altre informazioni, vedere [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Una sessione audio contiene flussi di rendering o flussi di acquisizione, ma non entrambi. Per impostazione predefinita, le impostazioni volume e mute per una sessione di rendering sono persistenti tra i riavvii del sistema. Le impostazioni volume e mute per una sessione di acquisizione non sono permanenti. Una sessione che contiene flussi che operano in modalità loopback viene gestita come una sessione di acquisizione. Ovvero le impostazioni della sessione non sono permanenti. Per ulteriori informazioni sulla modalità loopback, vedere la pagina relativa alla [registrazione di loopback](loopback-recording.md).

Ogni flusso audio appartiene esattamente a una sessione. Un client assegna un flusso audio a una determinata sessione al momento dell'inizializzazione dell'oggetto flusso. Il flusso mantiene l'appartenenza della sessione per la durata del flusso. Dopo la creazione di un oggetto flusso, l'oggetto esiste fino a quando un client non rilascia l'ultimo riferimento conteggiato all'oggetto, quindi l'oggetto viene eliminato.

Anche se un client non è in grado di modificare la sessione a cui è assegnato un flusso esistente, può ottenere un effetto simile eliminando il flusso (rilasciando tutti i riferimenti a esso), creando un nuovo flusso per sostituire il flusso eliminato e assegnando il nuovo flusso a un'altra sessione.

Ogni sessione di rendering rappresenta un subset dei flussi che formano la combinazione globale che riproduce un particolare [dispositivo di endpoint audio](audio-endpoint-devices.md). La combinazione globale combina tutte le sessioni di tutte le applicazioni che condividono il dispositivo.

Spesso un'applicazione con più flussi assegna tutti i relativi flussi alla stessa sessione. Tuttavia, l'applicazione può scegliere di assegnare flussi diversi a sessioni diverse. Qualsiasi flusso che l'applicazione non assegna in modo esplicito a una sessione appartiene alla sessione predefinita.

Le applicazioni audio tipiche devono evitare di modificare le impostazioni di volume e di silenziamento per le sessioni. Al contrario, gli utenti controllano queste impostazioni tramite le interfacce utente dei programmi di controllo. Ad esempio, in Windows Vista, il programma fornito dal sistema, Sndvol.exe, Visualizza un controllo del volume e il controllo di silenziamento per ogni sessione di rendering attiva o di recente attiva nel sistema. Tramite questi controlli, gli utenti possono modificare le impostazioni del volume e del silenziamento per tutte le sessioni nel sistema.

Attualmente il programma sndvol Visualizza i controlli volume solo per i dispositivi endpoint di rendering audio. Non vengono visualizzati i controlli volume per i dispositivi di acquisizione audio.

Una sessione è attiva se contiene uno o più flussi attivi. Un flusso attivo è nello *stato in esecuzione*. Un flusso inattivo è nello *stato interrotto*. Una sessione diventa attiva quando il primo flusso diventa attivo. Una sessione diventa inattiva quando l'ultimo flusso attivo diventa inattivo. Dopo che una sessione è rimasta inattiva per un determinato periodo di tempo, il sistema modifica lo stato della sessione da inattivo a scaduto.

Sndvol Visualizza i controlli volume e mute per tutte le sessioni di rendering attive e inattive. Sndvol rimuove i controlli volume e mute per una sessione quando lo stato della sessione passa da inattivo a scaduto o quando la sessione viene terminata. Una sessione termina quando viene eliminato l'ultimo flusso, ovvero quando un client rilascia il conteggio dei riferimenti finali nell'ultimo oggetto flusso rimanente della sessione. L'unica eccezione a questa regola è rappresentata dai suoni delle notifiche di sistema. Sndvol Visualizza sempre i controlli volume e mute per i suoni di notifica del sistema indipendentemente dallo stato della sessione per questi suoni.

In genere, un flusso appartiene a una sessione che si estende solo al processo che contiene l'applicazione che ha creato il flusso. Tuttavia, le applicazioni hanno la possibilità di definire sessioni tra processi che combinano flussi da due o più processi.

WASAPI supporta le sessioni tra processi principalmente, in modo che:

-   Il programma sndvol può presentare all'utente un controllo volume singolo per gestire i suoni delle notifiche di sistema in tutte le applicazioni.
-   Un lettore multimediale che viene eseguito in un processo può trasmettere contenuti protetti a un programma di decrittografia eseguito in un altro processo.

Analogamente alle impostazioni di controllo per le sessioni di rendering specifiche del processo, le impostazioni di controllo per le sessioni di rendering tra processi sono, per impostazione predefinita, permanenti tra i riavvii del sistema. WASAPI fornisce questo comportamento principalmente per i vantaggi dei suoni di notifica del sistema, che devono mantenere le impostazioni di volume e di silenziamento dell'utente in quanto la combinazione di applicazioni varia nel tempo.

Il programma sndvol etichetta il controllo volume per ogni sessione con un nome visualizzato e un'icona. Un client ha la possibilità di assegnare in modo esplicito un nome visualizzato e un'icona a una sessione. Se il client non fornisce questi elementi, sndvol visualizzerà invece un nome predefinito e un'icona predefinita. Il nome predefinito incorpora informazioni come il titolo della finestra dell'applicazione. L'icona predefinita è l'icona della finestra dell'applicazione. Solo nel caso di sessioni specifiche del processo, queste impostazioni predefinite forniscono agli utenti informazioni significative. Si noti che una sessione tra processi può essere associata a più di un'applicazione. In questo caso, solo un nome visualizzato e un'icona specificati dal client sono significativi.

Sebbene le impostazioni volume e mute per una sessione di rendering siano, per impostazione predefinita, permanenti tra i riavvii del sistema, il nome visualizzato e l'icona specificati dal client non lo sono. Per assicurarsi che sndvol visualizzi il nome e l'icona forniti dal client, il client deve assegnare in modo esplicito il nome e l'icona alla sessione nel momento in cui il client assegna il primo flusso alla sessione. Il sistema mantiene il nome visualizzato e l'icona di una sessione solo fino al termine della sessione.

Ogni sessione è identificata da un GUID della sessione. Quando un client apre un flusso, il client assegna tale flusso a una determinata sessione. Il client fornisce le seguenti due informazioni per identificare la sessione:

-   GUID della sessione.
-   Se la sessione è una sessione specifica tra processi o processi, una sessione specifica del processo contiene solo i flussi del processo del client.

Queste informazioni sono sufficienti per distinguere una determinata sessione da tutte le altre sessioni nello stesso computer. Il GUID della sessione per una sessione specifica del processo identifica in modo univoco la sessione solo nell'ambito del processo a cui appartiene la sessione. Al contrario, il GUID della sessione per una sessione tra processi è univoco nell'ambito di tutti i processi in esecuzione nel computer.

Nel caso di una sessione specifica del processo, il sistema utilizza una combinazione di GUID di sessione e ID processo per identificare in modo univoco la sessione nell'ambito del computer. Pertanto, se i client in due processi diversi assegnano i rispettivi flussi a due sessioni specifiche del processo con GUID di sessione identici, il sistema considera le sessioni come separate perché gli ID del processo sono diversi. Inoltre, se una sessione tra processi usa lo stesso GUID della sessione di una o più sessioni specifiche del processo, il sistema considera la sessione tra processi come diversa dalle sessioni specifiche del processo, anche se condividono lo stesso GUID della sessione.

Ad esempio, in Windows Vista, le API di livello superiore, come le funzioni **waveOutXxx** multimediali di Windows e DirectSound, in genere assegnano i flussi audio creati alle sessioni predefinite, specifiche del processo, identificate dal GUID del valore GUID della sessione \_ null. Per i client di queste API, la sessione predefinita per ogni processo client è separata dalle sessioni predefinite per gli altri processi client, anche se le sessioni hanno GUID di sessione identici. Inoltre, se una o più applicazioni assegnano flussi alla sessione tra processi identificata dal GUID del valore GUID della sessione \_ null, il sistema considera questa sessione tra processi come separata dalle sessioni predefinite specifiche del processo che condividono lo stesso GUID della sessione. Di conseguenza, il programma sndvol Visualizza un controllo del volume separato per ogni sessione del client predefinita, specifica del processo, e visualizza un ulteriore controllo del volume per la sessione tra processi identificato dal GUID del valore GUID della sessione \_ null, se tale sessione esiste.

Ogni sessione è associata a un solo dispositivo endpoint audio. Se due sessioni hanno GUID di sessione e ID processo identici ma sono associati a dispositivi diversi, il sistema considera le due sessioni come separate. Una sessione non può mai contenere entrambi i flussi di acquisizione e rendering perché un flusso di acquisizione può essere associato solo a un dispositivo di acquisizione e un flusso di rendering può essere associato solo a un dispositivo di rendering.

Come indicato in precedenza, le impostazioni volume e mute per una sessione sono persistenti tra i riavvii del sistema. Due o più istanze di un'applicazione possono creare sessioni specifiche del processo con GUID di sessione identici. Tramite il programma sndvol, l'utente può selezionare impostazioni diverse per volume e mute per ognuna di queste sessioni. Al termine di queste sessioni, il sistema mantiene le impostazioni di controllo di una sola di queste sessioni, ovvero l'ultima sessione da terminare. In seguito, se una nuova istanza dell'applicazione crea una sessione specifica del processo con lo stesso GUID della sessione precedente, la sessione eredita le impostazioni del volume e del silenziamento precedentemente salvate.

Un'applicazione non deve tentare di aggiungere un flusso o controllare il livello del volume di una sessione di proprietà di un'altra applicazione non correlata. Inoltre, un'applicazione non deve tentare di controllare il livello di volume della sessione gestita dal sistema per i suoni di notifica. Tuttavia, un'applicazione può riprodurre un suono attraverso la sessione di sistema per i suoni di notifica chiamando la funzione **PlaySound** . Per ulteriori informazioni, vedere [la pagina relativa ai suoni di notifica per le applicazioni audio legacy](notification-sounds-for-legacy-audio-applications.md).

Un'applicazione può registrarsi per ricevere notifiche quando cambia lo stato di una sessione. Per ulteriori informazioni, vedere [eventi di sessione audio](audio-session-events.md).

In rari casi, un'applicazione che crea una sessione specifica del processo potrebbe dover consolidare il controllo delle sessioni specifiche del processo per due o più istanze dell'applicazione in un unico controllo volume in sndvol. Per ulteriori informazioni, vedere [parametri di raggruppamento](grouping-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



