---
description: Componenti audio User-Mode
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: Componenti audio User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877937"
---
# <a name="user-mode-audio-components"></a>Componenti audio User-Mode

In Windows Vista, le API di base audio vengono utilizzate come base del sottosistema audio in modalità utente. Le API audio principali vengono implementate come un thin layer di componenti di sistema in modalità utente che separano i client in modalità utente dai driver audio in modalità kernel e dall'hardware audio. Le API audio di livello superiore, ad esempio DirectSound e le funzioni multimediali di Windows, accedono ai dispositivi audio tramite le API audio di base. Inoltre, alcune applicazioni audio comunicano direttamente con le API di base dell'audio.

Le API audio principali supportano la nozione intuitiva di un dispositivo endpoint audio. Un dispositivo endpoint audio è un'astrazione del software che rappresenta un dispositivo fisico che l'utente modifica direttamente. Esempi di dispositivi di endpoint audio sono altoparlanti, cuffie e microfoni. Per altre informazioni, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).

Nel diagramma seguente vengono illustrate le principali API audio e le relative relazioni con gli altri componenti audio in modalità utente di Windows Vista.

![diagramma dei componenti per il rendering audio in modalità utente](images/fig1.jpg)

Per semplicità, il diagramma precedente Mostra solo un percorso dati di rendering audio al dispositivo endpoint: il diagramma non mostra un percorso dati di acquisizione audio. Le API audio principali includono l' [API di MMDevice](mmdevice-api.md), [WASAPI](wasapi.md), l' [API DeviceTopology](devicetopology-api.md)e l' [API EndpointVolume](endpointvolume-api.md), che vengono implementate nel Audioses.dll e Mmdevapi.dll moduli di sistema in modalità utente.

Come illustrato nel diagramma precedente, le API audio principali forniscono una base per le API di livello superiore seguenti:

-   Media Foundation
-   Funzioni **waveXxx** e **mixerXxx** multimediali di Windows
-   DirectSound
-   DirectMusic

DirectSound, le funzioni audio multimediali di Windows e Media Foundation (tramite il renderer di streaming audio, o SAR, Component) comunicano direttamente con le API di base audio. DirectMusic comunica indirettamente con le API audio principali tramite DirectSound.

Un client di WASAPI passa i dati a un dispositivo endpoint tramite un *buffer dell'endpoint*. I componenti hardware e software di sistema gestiscono lo spostamento dei dati dal buffer dell'endpoint al dispositivo endpoint in modo che sia ampiamente trasparente per il client. Inoltre, per un dispositivo endpoint che si connette a una scheda audio con rilevamento della presenza Jack, il client può creare un buffer dell'endpoint solo per un dispositivo endpoint fisicamente presente. Per altre informazioni sul rilevamento della presenza di Jack, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).

Il diagramma precedente mostra due tipi di buffer dell'endpoint. Se un client di WASAPI apre un flusso in *modalità condivisa*, il client scrive i dati audio nel buffer dell'endpoint e il motore audio di Windows legge i dati dal buffer. In questa modalità il client condivide l'hardware audio con altre applicazioni in esecuzione in altri processi. Il motore audio combina i flussi di queste applicazioni e riproduce la combinazione risultante attraverso l'hardware. Il motore audio è un componente di sistema in modalità utente (Audiodg.dll) che esegue tutte le operazioni di elaborazione del flusso nel software. Al contrario, se un client apre un flusso in *modalità esclusiva*, il client dispone di accesso esclusivo all'hardware audio. In genere, solo un numero ridotto di applicazioni di tipo "Audio Pro" o RTC richiede la modalità esclusiva. Sebbene nel diagramma siano visualizzati sia i flussi in modalità condivisa che in modalità esclusiva, solo uno di questi due flussi (e il buffer dell'endpoint corrispondente) esiste, a seconda che il client Apra il flusso in modalità condivisa o in modalità esclusiva.

In modalità esclusiva il client può scegliere di aprire il flusso in qualsiasi formato audio supportato dal dispositivo endpoint. In modalità condivisa il client deve aprire il flusso nel formato di combinazione attualmente utilizzato dal motore audio (o un formato simile al formato di combinazione). I flussi di input del motore audio e la combinazione di output del motore sono tutti in questo formato.

In Windows 7 è stata aggiunta una nuova funzionalità denominata *modalità latence bassa* per i flussi in modalità di condivisione. In questa modalità, il motore audio viene eseguito in modalità pull, in cui si verifica una riduzione significativa della latenza. Questa operazione è molto utile per le applicazioni di comunicazione che richiedono una latenza di flusso audio bassa per un flusso più veloce.

Le applicazioni che gestiscono flussi audio a bassa latenza possono utilizzare il servizio Utilità di pianificazione classi multimediali (MMCSS) in Windows Vista per aumentare la priorità dei thread dell'applicazione che accedono ai buffer dell'endpoint. MMCSS consente di eseguire le applicazioni audio con priorità alta senza negare risorse della CPU alle applicazioni con priorità più bassa. MMCSS assegna una priorità a un thread in base al nome dell'attività. Windows Vista, ad esempio, supporta i nomi di attività "audio" e "Audio Pro" per i thread che gestiscono flussi audio. Per impostazione predefinita, la priorità di un thread "Audio Pro" è superiore a quella di un thread "audio". Per ulteriori informazioni su MMCSS, vedere la documentazione Windows SDK.

Le API audio principali supportano sia il formato PCM che quello non PCM. Tuttavia, il motore audio può combinare solo flussi PCM. In questo modo, solo i flussi in modalità esclusiva possono avere formati non PCM. Per altre informazioni, vedere [formati di dispositivo](device-formats.md).

Il motore audio viene eseguito nel proprio processo protetto, che è separato dal processo in cui viene eseguita l'applicazione. Per supportare un flusso in modalità condivisa, il servizio audio Windows (la casella con etichetta "servizio audio" nel diagramma precedente) alloca un buffer dell'endpoint tra processi accessibile sia all'applicazione che al motore audio. Per la modalità esclusiva, il buffer dell'endpoint risiede nella memoria accessibile sia all'applicazione che all'hardware audio.

Il servizio audio Windows è il modulo che implementa i criteri audio di Windows. I criteri audio sono un set di regole interne che il sistema applica alle interazioni tra flussi audio da più applicazioni che condividono e competono per l'uso dello stesso hardware audio. Il servizio audio Windows implementa i criteri audio impostando i parametri di controllo per il motore audio. I compiti del servizio audio includono:

-   Tenere traccia dei dispositivi audio aggiunti o rimossi dall'utente dal sistema.
-   Monitoraggio dei ruoli assegnati ai dispositivi audio nel sistema.
-   Gestione dei flussi audio da gruppi di attività che producono classi simili di contenuto audio (console, Multimedia e comunicazioni).
-   Controllo del livello del volume del flusso di output combinato ("submix") per ognuno dei vari tipi di contenuto audio.
-   Informare il motore audio sugli elementi di elaborazione nei percorsi dati per i flussi audio.

In alcune versioni di Windows, il servizio audio Windows è disabilitato per impostazione predefinita e deve essere attivato in modo esplicito prima che il sistema possa riprodurre l'audio.

Nell'esempio illustrato nel diagramma precedente, il dispositivo endpoint è un set di altoparlanti collegati alla scheda audio. L'applicazione client scrive i dati audio nel buffer dell'endpoint e il motore audio gestisce i dettagli del trasferimento dei dati dal buffer al dispositivo dell'endpoint.

La casella denominata "driver audio" nel diagramma precedente potrebbe essere una combinazione di componenti driver forniti dal sistema e del fornitore. Nel caso di una scheda audio in un bus PCI o PCI Express, il sistema fornisce al driver di sistema della classe porta (Portcls.sys), che implementa un set di driver di porta per le varie funzioni audio nella scheda e il fornitore dell'hardware fornisce un driver di adattatore che implementa un set di driver miniport per gestire le operazioni specifiche del dispositivo per i driver della porta. Nel caso di un controller e un codec audio a definizione elevata su un bus PCI o PCI Express, il sistema fornisce il driver dell'adattatore (Hdaudio.sys) e non è necessario alcun driver fornito dal fornitore. Nel caso di una scheda audio su un bus USB, il sistema fornisce il driver di sistema della classe AVStream (Ks.sys) oltre al driver audio USB (Usbaudio.sys); anche in questo caso non è necessario alcun driver fornito dal fornitore.

Per semplicità, il diagramma precedente Mostra solo i flussi di rendering. Tuttavia, le API di base audio supportano anche i flussi di acquisizione. In modalità condivisa, diversi client possono condividere il flusso acquisito da un dispositivo hardware audio. In modalità esclusiva, un client dispone di accesso esclusivo al flusso acquisito dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



