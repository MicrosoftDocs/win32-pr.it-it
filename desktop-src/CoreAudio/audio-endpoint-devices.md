---
description: Dispositivi endpoint audio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivi endpoint audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14d21aa174e34f8cb4ddab520819446a0e0ec89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966340"
---
# <a name="audio-endpoint-devices"></a>Dispositivi endpoint audio

Il termine *dispositivo endpoint* fa riferimento a un dispositivo hardware che si trova a un'estremità di un percorso dati che ha origine o termina in un programma dell'applicazione. Esempi di dispositivi di endpoint audio sono altoparlanti, cuffie, microfoni e lettori CD. I dati audio che si spostano lungo il percorso dati potrebbero attraversare un certo numero di componenti software e hardware durante il suo viaggio tra l'applicazione e il dispositivo endpoint. Sebbene questi componenti siano essenziali per il funzionamento del dispositivo endpoint, tendono a essere invisibili agli utenti. È più probabile che gli utenti pensino in termini di dispositivi endpoint che modificano direttamente invece che in termini di dispositivi sulle schede audio a cui i dispositivi endpoint si collegano o in termini di componenti software che elaborano i flussi audio che passano da e verso questi adapter.

Per evitare confusione con i dispositivi endpoint, questa documentazione si riferisce a un dispositivo in una scheda audio come un *dispositivo adattatore*.

Il diagramma seguente illustra il modo in cui i dispositivi dell'endpoint audio differiscono da quelli di adapter.

![esempi di dispositivi dell'endpoint audio e dispositivi adapter](images/devices.jpg)

Nel diagramma precedente, di seguito sono riportati alcuni esempi di dispositivi endpoint:

-   Altoparlanti
-   Microfono
-   Dispositivo di input ausiliario

Di seguito sono riportati alcuni esempi di dispositivi Adapter:

-   Dispositivo di output wave (che contiene il convertitore da digitale a analogico)
-   Dispositivo dei controlli di output (contiene i controlli volume e mute)
-   Dispositivo di input wave (contiene il convertitore da analogico a digitale)
-   Dispositivo dei controlli di input (contiene il controllo del volume e il multiplexer)

In genere, le interfacce utente delle applicazioni audio fanno riferimento a dispositivi endpoint audio, non a dispositivi adapter. Windows Vista semplifica la progettazione di applicazioni semplici da parte dell'utente, supportando direttamente l'astrazione del dispositivo dell'endpoint.

Alcuni dispositivi endpoint potrebbero connettersi in modo permanente a un dispositivo adapter. Ad esempio, un computer potrebbe contenere dispositivi interni, ad esempio un lettore di CD, un microfono o altoparlanti integrati nello chassis del sistema. In genere, l'utente non rimuove fisicamente questi dispositivi endpoint.

Altri dispositivi endpoint potrebbero connettersi a una scheda audio tramite jack audio. L'utente inserisce e scollega questi dispositivi esterni. Ad esempio, un dispositivo endpoint audio come un microfono esterno o cuffie si trova a un'estremità di un cavo la cui altra estremità si connette a un jack su un dispositivo di adapter.

L'adapter comunica con il processore di sistema tramite un bus di sistema (in genere, PCI o PCI Express) o il bus esterno (USB o IEEE 1394) che supporta Plug and Play (PnP). Durante l'enumerazione dei dispositivi, il gestore Plug and Play identifica i dispositivi nella scheda audio e li registra per renderli disponibili per l'uso da parte del sistema operativo e dalle applicazioni.

Diversamente dalla connessione tra un adapter e un bus esterno, ad esempio USB o il bus IEEE 1394, la connessione tra un dispositivo endpoint e un dispositivo adapter non supporta il rilevamento di dispositivi PnP. Tuttavia, alcune schede audio supportano il *rilevamento della presenza di Jack*: quando un plug viene inserito o rimosso da un Jack, l'hardware genera un interrupt per notificare al driver della scheda la modifica apportata alla configurazione hardware. Gestione endpoint in Windows Vista è in grado di sfruttare questa funzionalità hardware per notificare alle applicazioni i dispositivi endpoint presenti in qualsiasi momento. In questo modo, l'operazione di Gestione endpoint è analoga a quella di gestione Plug and Play, che tiene traccia dei dispositivi Adapter presenti nel sistema.

In Windows Vista, il sistema audio tiene traccia sia di dispositivi endpoint che di dispositivi adapter. Gestione endpoint registra i dispositivi endpoint e il gestore Plug and Play registra i dispositivi dell'adapter. La registrazione dei dispositivi endpoint rende più semplice per le applicazioni intuitive consentire agli utenti di fare riferimento ai dispositivi endpoint gestiti direttamente dagli utenti anziché fare riferimento a dispositivi adapter che potrebbero essere nascosti all'interno dello chassis del computer. I dispositivi endpoint segnalati dal sistema operativo registrano fedelmente le modifiche dinamiche nella configurazione dell'hardware audio con rilevamento presenze Jack. Mentre un dispositivo endpoint rimane collegato, il sistema enumera il dispositivo. Quando l'utente scollega un dispositivo endpoint, il sistema smette di enumerarlo.

Nelle versioni precedenti di Windows, tra cui Windows 98, Windows me, Windows 2000 e Windows XP, il sistema Visualizza in modo esplicito solo i dispositivi PnP per le applicazioni. Pertanto, le applicazioni devono dedurre l'esistenza di dispositivi endpoint. Un sistema operativo che non dispone del supporto esplicito per i dispositivi endpoint impone alle applicazioni client di eseguire un maggior numero di operazioni. Ad esempio, un'applicazione di acquisizione audio deve eseguire i passaggi seguenti per abilitare l'acquisizione da un microfono esterno:

1.  Enumerare tutti i dispositivi di acquisizione audio (ovvero dispositivi Adapter) precedentemente registrati da gestione PnP.
2.  Dopo aver selezionato un dispositivo di acquisizione, aprire un flusso di acquisizione sul dispositivo chiamando la funzione **waveInOpen** o l'API **DirectSoundCapture** o DirectShow.
3.  Chiamare la funzione mixerOpen e usare le altre funzioni **mixerXxx** per cercare una riga del \_ \_ microfono src MIXERLINE COMPONENTTYPE \_ che corrisponda al dispositivo di acquisizione aperto nel passaggio 2. Si tratta di una supposizione plausibile.
4.  Sbloccare il percorso dati dal microfono. Se il percorso dati include un nodo di silenziamento, il client deve disabilitare il muting del segnale dal microfono. Se il dispositivo di acquisizione contiene un multiplexer per la selezione tra diversi input, il client deve selezionare l'input del microfono.

Questo processo è soggetto a errori perché il software che esegue queste operazioni potrebbe avere esito negativo se viene rilevata una configurazione hardware non prevista per le finestre di progettazione o per la quale non è stata testata.

In Windows Vista, che supporta i dispositivi endpoint, il processo di connessione allo stesso dispositivo endpoint è molto più semplice:

1.  Selezionare un microfono da una raccolta di dispositivi endpoint.
2.  Attivare un'interfaccia di acquisizione audio sul microfono.

Il sistema operativo esegue tutte le operazioni necessarie per identificare e abilitare il dispositivo endpoint. Ad esempio, se il percorso dati del microfono include un multiplexer, il sistema seleziona automaticamente l'input del microfono per il multiplexer.

Il comportamento del sottosistema audio è più affidabile e deterministico se le applicazioni, invece di implementare i propri algoritmi di identificazione degli endpoint, possono relegare l'attività di identificazione dei dispositivi endpoint al sistema operativo. I fornitori di software non devono più verificare che gli algoritmi di identificazione degli endpoint funzionino correttamente con tutti i dispositivi e le configurazioni hardware disponibili. possono semplicemente basarsi sul sistema operativo per l'identificazione degli endpoint. Analogamente, i fornitori di hardware non devono più verificare che tutte le applicazioni client pertinenti possano identificare facilmente qualsiasi dispositivo endpoint connesso alla scheda audio. devono solo verificare che il sistema operativo sia in grado di identificare un dispositivo endpoint connesso alla scheda audio.

Negli argomenti seguenti vengono fornite informazioni aggiuntive sui dispositivi dell'endpoint audio:

-   [Informazioni sull'API MMDevice](mmdevice-api.md)
-   [Enumerazione dei dispositivi audio](enumerating-audio-devices.md)
-   [Stringhe ID endpoint](endpoint-id-strings.md)
-   [Proprietà dispositivo](device-properties.md)
-   [Eventi dispositivo](device-events.md)
-   [Ruoli del dispositivo](device-roles.md)
-   [Formati di dispositivo](device-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



