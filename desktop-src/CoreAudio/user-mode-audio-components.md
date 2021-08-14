---
description: User-Mode componenti audio
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode componenti audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8768cb6ece5825ae48803f30d8c1631a2e593f40815565b5dc879d23afd961aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166032"
---
# <a name="user-mode-audio-components"></a>User-Mode componenti audio

In Windows Vista le API audio principali fungono da base per il sottosistema audio in modalità utente. Le API audio di base vengono implementate come un thin livello di componenti di sistema in modalità utente che separano i client in modalità utente dai driver audio in modalità kernel e dall'hardware audio. Le API audio di livello superiore, ad esempio DirectSound e le Windows multimediali, accedono ai dispositivi audio tramite le API audio di base. Inoltre, alcune applicazioni audio comunicano direttamente con le API audio di base.

Le API audio di base supportano la nozione semplice di dispositivo endpoint audio. Un dispositivo endpoint audio è un'astrazione software che rappresenta un dispositivo fisico che l'utente modifica direttamente. Esempi di dispositivi endpoint audio sono altoparlanti, cuffia e microfoni. Per altre informazioni, vedere [Dispositivi endpoint audio.](audio-endpoint-devices.md)

Il diagramma seguente illustra le API audio principali e la relativa relazione con gli altri componenti audio in modalità utente in Windows Vista.

![Diagramma dei componenti di rendering audio in modalità utente](images/fig1.jpg)

Per semplicità, il diagramma precedente mostra solo un percorso dati di rendering audio per il dispositivo endpoint. Il diagramma non mostra un percorso dati di acquisizione audio. Le API audio principali includono [l'API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md), [l'API DeviceTopology](devicetopology-api.md)e l'API [EndpointVolume](endpointvolume-api.md), implementate nei moduli di sistema Audioses.dll e Mmdevapi.dll in modalità utente.

Come illustrato nel diagramma precedente, le API audio di base forniscono una base per le API di livello superiore seguenti:

-   Media Foundation
-   Windows funzioni **waveXxx e** **mixerXxx multimediali**
-   Directsound
-   Directmusic

DirectSound, il Windows funzioni audio multimediali e Media Foundation (tramite il renderer audio di streaming, o SAR, componente) comunicano direttamente con le API audio di base. DirectMusic comunica indirettamente con le API audio principali tramite DirectSound.

Un client di WASAPI passa i dati a un dispositivo endpoint tramite un *buffer dell'endpoint*. I componenti hardware e software di sistema gestiscono lo spostamento dei dati dal buffer dell'endpoint al dispositivo endpoint in modo in gran parte trasparente per il client. Inoltre, per un dispositivo endpoint che si collega a un adattatore audio con rilevamento della presenza di jack, il client può creare un buffer endpoint solo per un dispositivo endpoint fisicamente presente. Per altre informazioni sul rilevamento della presenza di jack, vedere [Dispositivi endpoint audio.](audio-endpoint-devices.md)

Il diagramma precedente mostra due tipi di buffer dell'endpoint. Se un client di WASAPI apre un flusso *in* modalità condivisa, il client scrive i dati audio nel buffer dell'endpoint e il motore audio Windows legge i dati dal buffer. In questa modalità, il client condivide l'hardware audio con altre applicazioni in esecuzione in altri processi. Il motore audio combina i flussi di queste applicazioni e riproduce la combinazione risultante tramite l'hardware. Il motore audio è un componente di sistema in modalità utente (Audiodg.dll) che esegue tutte le operazioni di elaborazione dei flussi nel software. Al contrario, se un client apre un flusso in *modalità esclusiva,* il client ha accesso esclusivo all'hardware audio. In genere, solo un numero ridotto di applicazioni "pro audio" o RTC richiede la modalità esclusiva. Anche se il diagramma mostra sia i flussi in modalità condivisa che i flussi in modalità esclusiva, esiste solo uno di questi due flussi (e il buffer dell'endpoint corrispondente), a seconda che il client apra il flusso in modalità condivisa o in modalità esclusiva.

In modalità esclusiva, il client può scegliere di aprire il flusso in qualsiasi formato audio supportato dal dispositivo endpoint. In modalità condivisa, il client deve aprire il flusso nel formato di combinazione attualmente in uso dal motore audio (o in un formato simile al formato di combinazione). I flussi di input del motore audio e la combinazione di output del motore sono tutti in questo formato.

Nella Windows 7 è stata aggiunta una nuova funzionalità denominata modalità a *bassa latenza* per i flussi in modalità di condivisione. In questa modalità, il motore audio viene eseguito in modalità pull, in cui è presente una riduzione significativa della latenza. Ciò è molto utile per le applicazioni di comunicazione che richiedono una bassa latenza del flusso audio per lo streaming più veloce.

Le applicazioni che gestiscono flussi audio a bassa latenza possono usare il servizio Utilità di pianificazione classi multimediali (MMCSS) in Windows Vista per aumentare la priorità dei thread dell'applicazione che accedono ai buffer degli endpoint. MMCSS consente l'esecuzione di applicazioni audio con priorità alta senza negare le risorse della CPU alle applicazioni con priorità più bassa. MMCSS assegna una priorità a un thread in base al nome dell'attività. Ad esempio, Windows Vista supporta i nomi di attività "Audio" e "Pro Audio" per i thread che gestiscono i flussi audio. Per impostazione predefinita, la priorità di un thread "audio Pro" è superiore a quella di un thread "Audio". Per altre informazioni su MMCSS, vedere la documentazione Windows SDK.

Le API audio di base supportano sia formati di flusso PCM che non PCM. Tuttavia, il motore audio può combinare solo flussi PCM. Di conseguenza, solo i flussi in modalità esclusiva possono avere formati non PCM. Per altre informazioni, vedere [Formati di dispositivo.](device-formats.md)

Il motore audio viene eseguito nel proprio processo protetto, separato dal processo in cui viene eseguita l'applicazione. Per supportare un flusso in modalità condivisa, il servizio audio Windows (la casella con etichetta "Servizio audio" nel diagramma precedente) alloca un buffer dell'endpoint tra processi accessibile sia all'applicazione che al motore audio. Per la modalità esclusiva, il buffer dell'endpoint risiede in memoria accessibile sia all'applicazione che all'hardware audio.

Il Windows audio è il modulo che implementa i Windows audio. I criteri audio sono un set di regole interne che il sistema applica alle interazioni tra flussi audio da più applicazioni che condividono e concorreranno per l'uso dello stesso hardware audio. Il Windows audio implementa i criteri audio impostando i parametri di controllo per il motore audio. I compiti del servizio audio includono:

-   Tenere traccia dei dispositivi audio che l'utente aggiunge o rimuove dal sistema.
-   Monitoraggio dei ruoli assegnati ai dispositivi audio nel sistema.
-   Gestione dei flussi audio da gruppi di attività che producono classi simili di contenuto audio (console, contenuti multimediali e comunicazioni).
-   Controllo del livello di volume del flusso di output combinato ("submix") per ognuno dei vari tipi di contenuto audio.
-   Informazioni sul motore audio sugli elementi di elaborazione nei percorsi dati per i flussi audio.

In alcune versioni di Windows, il servizio audio Windows è disabilitato per impostazione predefinita e deve essere attivato in modo esplicito prima che il sistema possa riprodurre l'audio.

Nell'esempio illustrato nel diagramma precedente, il dispositivo endpoint è un set di altoparlanti collegati alla scheda audio. L'applicazione client scrive i dati audio nel buffer dell'endpoint e il motore audio gestisce i dettagli del trasporto dei dati dal buffer al dispositivo endpoint.

La casella con etichetta "Driver audio" nel diagramma precedente potrebbe essere una combinazione di componenti driver forniti dal sistema e forniti dal fornitore. Nel caso di una scheda audio su un bus PCI o PCI Express, il sistema fornisce il driver di sistema della classe porta (Portcls.sys), che implementa un set di driver di porta per le varie funzioni audio nell'adattatore e il fornitore dell'hardware fornisce un driver di scheda che implementa un set di driver miniport per gestire operazioni specifiche del dispositivo per i driver di porta. Nel caso di un controller e codec High Definition Audio in un bus PCI o PCI Express, il sistema fornisce il driver dell'adattatore (Hdaudio.sys) e non è necessario alcun driver fornito dal fornitore. Nel caso di una scheda audio su un bus USB, il sistema fornisce il driver di sistema di classe AVStream (Ks.sys) più il driver audio USB (Usbaudio.sys); anche in questo caso, non è necessario alcun driver fornito dal fornitore.

Per semplicità, il diagramma precedente mostra solo i flussi di rendering. Tuttavia, anche le API audio di base supportano i flussi di acquisizione. In modalità condivisa, diversi client possono condividere il flusso acquisito da un dispositivo hardware audio. In modalità esclusiva, un client ha accesso esclusivo al flusso acquisito dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



