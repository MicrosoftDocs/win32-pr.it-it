---
description: Sessioni audio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sessioni audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d5b8cee0a3a53709d2c450bef36ae00e3a6f4d9323c75ff80e96b19550eb39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929411"
---
# <a name="audio-sessions"></a>Sessioni audio

Una *sessione audio* è un gruppo di flussi audio correlati che un client WASAPI può gestire collettivamente. I client possono controllare il livello del volume e lo stato di disattivazione di ogni singola sessione. Il sistema applica le impostazioni del volume e dell'audio specificate dal client in modo uniforme a tutti i flussi nella sessione.

Quando un client inizializza un flusso audio, lo assegna a una sessione audio. Per altre informazioni, vedere [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Una sessione audio contiene flussi di rendering o di acquisizione, ma non entrambi. Per impostazione predefinita, le impostazioni del volume e dell'audio per una sessione di rendering sono persistenti tra i riavvii del sistema. Le impostazioni del volume e dell'audio per una sessione di acquisizione non sono persistenti. Una sessione che contiene flussi che operano in modalità loopback viene considerata come una sessione di acquisizione. In altri modo, le impostazioni della sessione non sono persistenti. Per altre informazioni sulla modalità loopback, vedere [Registrazione loopback.](loopback-recording.md)

Ogni flusso audio appartiene esattamente a una sessione. Un client assegna un flusso audio a una sessione specifica nel momento in cui inizializza l'oggetto flusso. Il flusso mantiene l'appartenenza alla sessione per la durata del flusso. Dopo la creazione di un oggetto flusso, l'oggetto esiste fino a quando un client non rilascia l'ultimo riferimento conteggiato all'oggetto e quindi l'oggetto viene eliminato.

Anche se un client non può modificare la sessione a cui è assegnato un flusso esistente, può ottenere un effetto simile eliminando il flusso (rilasciando tutti i riferimenti ad esso), creando un nuovo flusso per sostituire il flusso eliminato e assegnando il nuovo flusso a un'altra sessione.

Ogni sessione di rendering rappresenta un subset dei flussi che formano la combinazione globale riprodotta tramite un dispositivo [endpoint audio specifico.](audio-endpoint-devices.md) La combinazione globale combina tutte le sessioni di tutte le applicazioni che condividono il dispositivo.

Spesso, un'applicazione con più flussi assegna tutti i relativi flussi alla stessa sessione. Tuttavia, l'applicazione può, come opzione, assegnare flussi diversi a sessioni diverse. Qualsiasi flusso che l'applicazione non assegna in modo esplicito a una sessione appartiene alla sessione predefinita.

Le applicazioni audio tipiche devono evitare di modificare le impostazioni del volume e dell'audio per le sessioni. Al contrario, gli utenti controllano queste impostazioni tramite le interfacce utente dei programmi di controllo. Ad esempio, in Windows Vista, il programma fornito dal sistema, Sndvol.exe, visualizza un controllo del volume e disattiva il controllo per ogni sessione di rendering attiva o attiva di recente nel sistema. Tramite questi controlli, gli utenti possono modificare le impostazioni del volume e dell'audio per tutte le sessioni del sistema.

Il programma Sndvol attualmente visualizza i controlli del volume solo per i dispositivi endpoint di rendering audio. Non visualizza i controlli del volume per i dispositivi di acquisizione audio.

Una sessione è attiva se contiene uno o più flussi attivi. Un flusso attivo è nello *stato di esecuzione*. Un flusso inattivo è nello *stato arrestato.* Una sessione diventa attiva quando il primo flusso diventa attivo. Una sessione diventa inattiva quando l'ultimo flusso attivo diventa inattivo. Dopo che una sessione è stata inattiva per un periodo di tempo, il sistema modifica lo stato della sessione da inattivo a scaduto.

Sndvol visualizza i controlli di volume e disattivazione dell'audio per tutte le sessioni di rendering attive e inattive. Sndvol rimuove il volume e i controlli di disattivazione dell'audio per una sessione quando lo stato della sessione cambia da inattivo a scaduto o quando la sessione termina. Una sessione termina quando viene eliminato l'ultimo dei relativi flussi, ovvero quando un client rilascia il conteggio dei riferimenti finale sull'ultimo oggetto flusso rimanente nella sessione. L'unica eccezione a questa regola è per i suoni di notifica di sistema. Sndvol visualizza sempre i controlli del volume e dell'audio per i suoni di notifica di sistema indipendentemente dallo stato della sessione per questi suoni.

In genere, un flusso appartiene a una sessione che si estende solo sul processo che contiene l'applicazione che ha creato il flusso. Tuttavia, le applicazioni hanno la possibilità di definire sessioni tra processi che combinano flussi di due o più processi.

WASAPI supporta principalmente le sessioni tra processi in modo che:

-   Il programma Sndvol può presentare all'utente un singolo controllo del volume per gestire i suoni delle notifiche di sistema in tutte le applicazioni.
-   Un lettore multimediale eseguito in un processo può trasmettere contenuto protetto a un programma di decrittografia eseguito in un altro processo.

Analogamente alle impostazioni di controllo per le sessioni di rendering specifiche del processo, le impostazioni di controllo per le sessioni di rendering tra processi sono, per impostazione predefinita, persistenti tra i riavvii del sistema. WASAPI offre questo comportamento principalmente a vantaggio dei suoni di notifica di sistema, che devono mantenere le impostazioni di volume e di disattivazione dell'audio dell'utente quando la combinazione di applicazioni varia nel tempo.

Il programma Sndvol etichetta il controllo del volume per ogni sessione con un nome visualizzato e un'icona. Un client può assegnare in modo esplicito un nome visualizzato e un'icona a una sessione. Se il client non fornisce questi elementi, Sndvol visualizza invece un nome predefinito e un'icona predefinita. Il nome predefinito incorpora informazioni quali il titolo della finestra dell'applicazione. L'icona predefinita è l'icona per la finestra dell'applicazione. Solo nel caso di sessioni specifiche del processo, queste impostazioni predefinite forniscono informazioni significative agli utenti. Si noti che una sessione tra processi può essere associata a più applicazioni. In questo caso, solo un nome visualizzato e un'icona forniti dal client sono significativi.

Anche se le impostazioni del volume e dell'audio per una sessione di rendering sono persistenti per impostazione predefinita nei riavvii del sistema, il nome visualizzato e l'icona forniti dal client non lo sono. Per assicurarsi che Sndvol visualizzi il nome e l'icona forniti dal client, il client deve assegnare in modo esplicito il nome e l'icona alla sessione nel momento in cui il client assegna il primo flusso alla sessione. Il sistema mantiene il nome visualizzato e l'icona per una sessione solo fino al termine della sessione.

Ogni sessione è identificata da un GUID di sessione. Nel momento in cui un client apre un flusso, il client assegna tale flusso a una sessione specifica. Il client fornisce le due informazioni seguenti per identificare la sessione:

-   GUID di sessione.
-   Se la sessione è una sessione multi-processo o specifica del processo, una sessione specifica del processo contiene solo flussi dal processo del client.

Queste informazioni sono sufficienti per distinguere una sessione specifica da tutte le altre sessioni nello stesso computer. Il GUID della sessione per una sessione specifica del processo identifica in modo univoco la sessione solo nell'ambito del processo proprietario della sessione. Al contrario, il GUID di sessione per una sessione cross-process è univoco nell'ambito di tutti i processi in esecuzione nel computer.

Nel caso di una sessione specifica del processo, il sistema usa una combinazione di GUID di sessione e ID processo per identificare in modo univoco la sessione nell'ambito del computer. Pertanto, se i client in due processi diversi assegnano i rispettivi flussi a due sessioni specifiche del processo con GUID di sessione identici, il sistema considera le sessioni separate perché i relativi ID di processo sono diversi. Inoltre, se una sessione tra processi usa lo stesso GUID di sessione di una o più sessioni specifiche del processo, il sistema considera la sessione tra processi come distinta dalle sessioni specifiche del processo, anche se condividono lo stesso GUID di sessione.

Ad esempio, in Windows Vista le API di livello superiore, ad esempio le funzioni **waveOutXxx** multimediali di Windows e DirectSound, assegnano in genere i flussi audio creati alle sessioni predefinite specifiche del processo identificate dal valore GUID DELLA sessione GUID \_ NULL. Per i client di queste API, la sessione predefinita per ogni processo client è separata dalle sessioni predefinite per altri processi client, anche se le sessioni hanno GUID di sessione identici. Inoltre, se una o più applicazioni assegnano flussi alla sessione tra processi identificata dal valore GUID della sessione GUID NULL, il sistema considera questa sessione cross-process come separata dalle sessioni predefinite specifiche del processo che condividono lo stesso GUID di \_ sessione. Di conseguenza, il programma Sndvol visualizza un controllo del volume separato per la sessione predefinita, specifica del processo di ogni client, e visualizza un controllo del volume aggiuntivo per la sessione tra processi identificato dal valore GUID della sessione GUID NULL, se tale sessione \_ esiste.

Ogni sessione è associata a un solo dispositivo endpoint audio. Se due sessioni hanno GUID di sessione identici e ID processo, ma sono associati a dispositivi diversi, il sistema considera le due sessioni separate. Una sessione non può mai contenere flussi di acquisizione e rendering perché un flusso di acquisizione può essere associato solo a un dispositivo di acquisizione e un flusso di rendering può essere associato solo a un dispositivo di rendering.

Come accennato in precedenza, le impostazioni del volume e dell'audio per una sessione sono persistenti tra i riavvii del sistema. Due o più istanze di un'applicazione possono creare sessioni specifiche del processo con GUID di sessione identici. Tramite il programma Sndvol, l'utente può selezionare impostazioni di volume e disattivazione dell'audio diverse per ognuna di queste sessioni. Al termine di queste sessioni, il sistema mantiene le impostazioni di controllo di una sola di queste sessioni, ovvero l'ultima sessione da terminare. In seguito, se una nuova istanza dell'applicazione crea una sessione specifica del processo con lo stesso GUID di sessione precedente, tale sessione eredita il volume salvato in precedenza e le impostazioni di disattivazione dell'audio.

Un'applicazione non deve tentare di aggiungere un flusso a o controllare il livello di volume di una sessione di proprietà di un'altra applicazione non correlata. Inoltre, un'applicazione non deve tentare di controllare il livello di volume della sessione gestita dal sistema per i suoni di notifica. Tuttavia, un'applicazione può riprodurre un suono tramite la sessione di sistema per i suoni di notifica chiamando la **funzione PlaySound.** Per altre informazioni, vedere [Suoni di notifica per applicazioni audio legacy.](notification-sounds-for-legacy-audio-applications.md)

Un'applicazione può registrarsi per ricevere notifiche quando lo stato di una sessione cambia. Per altre informazioni, vedere [Eventi sessione audio](audio-session-events.md).

In rari casi, un'applicazione che crea una sessione specifica del processo potrebbe dover consolidare il controllo delle sessioni specifiche del processo per due o più istanze dell'applicazione in un singolo controllo del volume in Sndvol. Per altre informazioni, vedere [Parametri di raggruppamento](grouping-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



