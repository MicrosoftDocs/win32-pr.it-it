---
description: Dispositivi endpoint audio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivi endpoint audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11145227ff4f6cf4eb7dd11342e28b3a8260aac95c41b32faed6b2d6bd414dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407332"
---
# <a name="audio-endpoint-devices"></a>Dispositivi endpoint audio

Il termine *dispositivo endpoint* si riferisce a un dispositivo hardware che si trova a un'estremità di un percorso dati che ha origine o termina in un programma applicativo. Esempi di dispositivi endpoint audio sono altoparlanti, cuffia, microfoni e lettori CD. I dati audio che si spostano lungo il percorso dati potrebbero attraversare una serie di componenti software e hardware durante il percorso tra l'applicazione e il dispositivo endpoint. Anche se questi componenti sono essenziali per il funzionamento del dispositivo endpoint, tendono a essere invisibili agli utenti. È più probabile che gli utenti pensino in termini di dispositivi endpoint che manipolano direttamente anziché in termini di dispositivi su schede audio a cui i dispositivi endpoint si collegano o in termini di componenti software che elaborano i flussi audio che fluiranno da e verso tali schede.

Per evitare confusione con i dispositivi endpoint, questa documentazione fa riferimento a un dispositivo in una scheda audio come dispositivo *adapter.*

Il diagramma seguente illustra le differenze tra i dispositivi endpoint audio e i dispositivi adapter.

![esempi di dispositivi endpoint audio e dispositivi adapter](images/devices.jpg)

Nel diagramma precedente, di seguito sono riportati esempi di dispositivi endpoint:

-   Altoparlanti
-   Microfono
-   Dispositivo di input ausiliario

Di seguito sono riportati esempi di dispositivi adapter:

-   Dispositivo di output Wave (contiene convertitore da digitale ad analogico)
-   Dispositivo di controlli di output (contiene i controlli volume e disattivazione dell'audio)
-   Dispositivo di input wave (contiene convertitore da analogico a digitale)
-   Dispositivo di controlli di input (contiene il controllo del volume e il multiplexer)

In genere, le interfacce utente delle applicazioni audio fanno riferimento ai dispositivi endpoint audio, non ai dispositivi adapter. Windows Vista semplifica la progettazione di applicazioni di facile utilizzo supportando direttamente l'astrazione del dispositivo endpoint.

Alcuni dispositivi endpoint potrebbero connettersi in modo permanente a un dispositivo adapter. Ad esempio, un computer potrebbe contenere dispositivi interni, ad esempio un lettore CD, un microfono o altoparlanti integrati nello chassis del sistema. In genere, l'utente non rimuove fisicamente questi dispositivi endpoint.

Altri dispositivi endpoint potrebbero connettersi a un adattatore audio tramite jack audio. L'utente collega e scollega questi dispositivi esterni. Ad esempio, un dispositivo endpoint audio, ad esempio un microfono esterno o le cuffia, si trova su un'estremità di un cavo la cui altra estremità si collega a un jack in un dispositivo adattatore.

L'adattatore comunica con il processore di sistema tramite un bus di sistema (in genere PCI o PCI Express) o bus esterno (USB o IEEE 1394) che supporta Plug and Play (PnP). Durante l'enumerazione dei dispositivi, Plug and Play manager identifica i dispositivi nella scheda audio e li registra per renderli disponibili per l'uso da parte del sistema operativo e dalle applicazioni.

A differenza della connessione tra un adattatore e un bus esterno, ad esempio USB o il bus IEEE 1394, la connessione tra un dispositivo endpoint e un dispositivo adattatore non supporta il rilevamento del dispositivo PnP. Tuttavia, alcune schede audio supportano il rilevamento della presenza di jack: quando un *plug-in* viene inserito o rimosso da un jack, l'hardware genera un interrupt per notificare al driver della scheda la modifica nella configurazione hardware. Il gestore degli endpoint in Windows Vista può sfruttare questa funzionalità hardware per notificare alle applicazioni quali dispositivi endpoint sono presenti in qualsiasi momento. In questo modo, il funzionamento di Gestione endpoint è analogo a quello del gestore di Plug and Play, che tiene traccia dei dispositivi adapter presenti nel sistema.

In Windows Vista, il sistema audio tiene traccia sia dei dispositivi endpoint che dei dispositivi adapter. Il gestore degli endpoint registra i dispositivi endpoint e Plug and Play manager registra i dispositivi adapter. La registrazione dei dispositivi endpoint rende più semplice per le applicazioni di facile utilizzo consentire agli utenti di fare riferimento ai dispositivi endpoint che gli utenti modificano direttamente invece di fare riferimento ai dispositivi adapter che potrebbero essere nascosti all'interno dello chassis del computer. I dispositivi endpoint segnalati dal sistema operativo monitorano fedelmente le modifiche dinamiche nella configurazione dell'hardware audio con rilevamento della presenza di jack. Mentre un dispositivo endpoint rimane collegato, il sistema enumera tale dispositivo. Quando l'utente scollega un dispositivo endpoint, il sistema smette di enumerarlo.

Nelle versioni precedenti di Windows, tra cui Windows 98, Windows Me, Windows 2000 e Windows XP, il sistema presenta in modo esplicito solo i dispositivi PnP alle applicazioni. Di conseguenza, le applicazioni devono dedurre l'esistenza di dispositivi endpoint. Un sistema operativo privo di supporto esplicito per i dispositivi endpoint impone alle applicazioni client di eseguire più operazioni. Ad esempio, un'applicazione di acquisizione audio deve eseguire la procedura seguente per abilitare l'acquisizione da un microfono esterno:

1.  Enumerare tutti i dispositivi di acquisizione audio (si tratta di dispositivi adapter) registrati in precedenza dal gestore PnP.
2.  Dopo aver selezionato un dispositivo di acquisizione, aprire un flusso di acquisizione nel dispositivo chiamando la funzione **waveInOpen** o usando l'API **DirectSoundCapture** o DirectShow.
3.  Chiamare la funzione mixerOpen e usare le altre funzioni **mixerXxx** per cercare una linea MIXERLINE COMPONENTTYPE SRC MICROPHONE corrispondente al dispositivo di acquisizione aperto \_ nel passaggio \_ \_ 2. Si tratta di un'ipotesi educata.
4.  Sbloccare il percorso dei dati dal microfono. Se il percorso dei dati include un nodo mute, il client deve disabilitare la disattivazione del segnale dal microfono. Se il dispositivo di acquisizione contiene un multiplexer da selezionare tra diversi input, il client deve selezionare l'input del microfono.

Questo processo è a prova di errore perché il software che esegue queste operazioni potrebbe non riuscire se rileva una configurazione hardware non anticipata dai progettisti o per la quale non è stata testata.

In Windows Vista, che supporta i dispositivi endpoint, il processo di connessione allo stesso dispositivo endpoint è molto più semplice:

1.  Selezionare un microfono da una raccolta di dispositivi endpoint.
2.  Attivare un'interfaccia di acquisizione audio sul microfono.

Il sistema operativo esegue tutte le operazioni necessarie per identificare e abilitare il dispositivo endpoint. Ad esempio, se il percorso dati dal microfono include un multiplexer, il sistema seleziona automaticamente l'input del microfono per il multiplexer.

Il comportamento del sottosistema audio è più affidabile e deterministico se le applicazioni, invece di implementare i propri algoritmi di identificazione degli endpoint, possono relegare l'attività di identificazione dei dispositivi endpoint al sistema operativo. I fornitori di software non devono più verificare che gli algoritmi di identificazione degli endpoint funzionino correttamente con tutti i dispositivi e le configurazioni hardware audio disponibili. Possono semplicemente basarsi sul sistema operativo per l'identificazione degli endpoint. Analogamente, i fornitori di hardware non devono più verificare che ogni applicazione client pertinente possa identificare facilmente qualsiasi dispositivo endpoint connesso alla scheda audio, ma solo per verificare che il sistema operativo sia in grado di identificare un dispositivo endpoint connesso alla scheda audio.

Gli argomenti seguenti forniscono informazioni aggiuntive sui dispositivi endpoint audio:

-   [Informazioni sull'API MMDevice](mmdevice-api.md)
-   [Enumerazione di dispositivi audio](enumerating-audio-devices.md)
-   [Stringhe di ID endpoint](endpoint-id-strings.md)
-   [Proprietà dispositivo](device-properties.md)
-   [Eventi del dispositivo](device-events.md)
-   [Ruoli del dispositivo](device-roles.md)
-   [Formati dei dispositivi](device-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



