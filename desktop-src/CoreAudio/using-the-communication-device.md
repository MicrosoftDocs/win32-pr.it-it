---
description: In Windows 7, il pannello di controllo multimediale di Windows, Mmsys.cpl, fornisce una nuova scheda comunicazioni.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Uso di un dispositivo di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877934"
---
# <a name="using-a-communication-device"></a>Uso di un dispositivo di comunicazione

In Windows 7, il pannello di controllo multimediale di Windows, Mmsys.cpl, fornisce una nuova scheda **comunicazioni** . Questa scheda contiene opzioni che consentono a un utente di impostare opzioni che definiscono la modalità di gestione di un *dispositivo di comunicazione* da parte del sistema. Un dispositivo di comunicazione viene utilizzato principalmente per l'inserimento o la ricezione di chiamate telefoniche sul computer. Per un computer che dispone di un solo dispositivo di rendering (altoparlante) e un dispositivo di acquisizione (microfono), questi dispositivi audio fungono anche da dispositivi di comunicazione predefiniti. Quando un utente connette un nuovo dispositivo, ad esempio una cuffia USB, il sistema esegue il rilevamento automatico del ruolo del dispositivo cercando le impostazioni di configurazione popolate dall'OEM. Se il sistema determina che un dispositivo è più adatto a scopi di comunicazione, il sistema assegna il ruolo **comunicazioni elettroniche** al dispositivo. Per questi dispositivi, il Mmsys.cpl di Windows 7 fornisce l'opzione **dispositivo di comunicazione predefinito** che consente a un utente di selezionare un dispositivo di comunicazione ciascuno per il rendering audio (scheda **riproduzione** ) e l'acquisizione audio (scheda **registrazione** ). Il sistema esegue il rilevamento automatico dei ruoli, ma non imposta un dispositivo specifico da usare per le comunicazioni. Questa operazione deve essere eseguita dall'utente. Il nuovo ruolo **comunicazioni elettroniche** consente a un'applicazione di distinguere tra un dispositivo scelto dall'utente per la gestione delle chiamate telefoniche e di un dispositivo da usare come dispositivo multimediale (riproduzione musicale). Ad esempio, se l'utente dispone di una cuffia e di un altoparlante connesso al computer, il sistema assegna il ruolo **eConsole** al relatore e il ruolo **comunicazioni elettroniche** all'auricolare. Dopo che l'utente ha selezionato la cuffia da usare come dispositivo di comunicazione, per sviluppare un'applicazione di comunicazione, è possibile indirizzare l'auricolare in modo specifico per il rendering di un flusso audio. Un'applicazione l'utente non può modificare il ruolo del dispositivo assegnato dal sistema. Per ulteriori informazioni sui ruoli del dispositivo, vedere [ruoli del dispositivo](device-roles.md).

Le applicazioni di comunicazione, ad esempio le applicazioni VoIP e Unified Communication, inseriscono e ricevono telefonate tramite un computer. Ad esempio, un'applicazione VoIP potrebbe assegnare un flusso che contiene la notifica dell'anello all'endpoint di un set di dispositivi di comunicazione per il rendering dei flussi audio. Inoltre, l'applicazione potrebbe aprire i flussi di input e output vocali nei dispositivi dell'endpoint di acquisizione e rendering impostati come dispositivi di comunicazione.

Per integrare le funzionalità di comunicazione nelle applicazioni, è possibile usare:

-   [API MMDevice](mmdevice-api.md): per ottenere un riferimento all'endpoint del dispositivo di comunicazione.
-   [WASAPI](wasapi.md): per eseguire il rendering e acquisire i flussi audio tramite il dispositivo di comunicazione. Il sistema operativo considera il flusso aperto in un dispositivo di comunicazione come *flusso di comunicazione*.

L'applicazione di comunicazione enumera i dispositivi e fornisce la gestione del flusso per un flusso di comunicazione (rendering o acquisizione) nello stesso modo in cui gestirebbe un flusso non di comunicazione usando le API di base di audio.

Una delle funzionalità che è possibile integrare nell'applicazione di comunicazione è il *ducking* o l' *attenuazione del flusso*. Questo comportamento definisce cosa deve accadere ad altri suoni quando viene aperto un flusso di comunicazione, ad esempio quando viene ricevuta una telefonata sul dispositivo di comunicazione. Il sistema potrebbe disattivare o abbassare il volume audio del flusso non di comunicazione a seconda della scelta dell'utente. Il sistema audio genera eventi ducking quando viene aperto o chiuso un flusso di comunicazione per il rendering o l'acquisizione di flussi. Per impostazione predefinita, il sistema operativo fornisce un'esperienza di ducking predefinita. Un'applicazione multimediale può sostituire il comportamento predefinito e gestire questi eventi per offrire un'esperienza di ducking personalizzata.

Le sezioni seguenti descrivono come usare le API audio di base per offrire un'esperienza di ducking personalizzata.

-   [Esperienza di ducking predefinita](stream-attenuation.md)
-   [Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
-   [Fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md)
-   [Considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md)
-   [Recupero di eventi ducking](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Ottenere un riferimento all'endpoint del dispositivo di comunicazione

Per usare il dispositivo di comunicazione, un client WASAPI diretto deve enumerare i dispositivi usando l'enumeratore del dispositivo. Ottenere un riferimento all'endpoint del dispositivo di comunicazione predefinito chiamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In questa chiamata, l'applicazione deve specificare **comunicazioni elettroniche** nel parametro *Role* per limitare l'enumerazione del dispositivo ai dispositivi di comunicazione. Dopo aver ottenuto un riferimento all'endpoint del dispositivo per il dispositivo, è possibile attivare i servizi che hanno come ambito l'endpoint chiamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Ad esempio, è possibile passare l'identificatore del servizio **IID \_ IAudioClient** per attivare un oggetto client audio e usarlo per la gestione del flusso, l'identificatore di **\_ IAudioEndpointVolume IID** per ottenere l'accesso ai controlli volume dell'endpoint del dispositivo di comunicazione o l'identificatore **IID \_ IAudioSessionManager** per attivare il gestore sessioni che consente di interagire con il motore dei criteri dell'endpoint. Per informazioni sulle operazioni di flusso, vedere [gestione dei flussi](stream-management.md).

Usando il riferimento [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , è anche possibile accedere all'archivio delle proprietà per l'endpoint del dispositivo. Questi valori di proprietà, come il nome descrittivo del dispositivo e il nome del produttore, vengono popolati dall'OEM e consentono a un'applicazione di determinare le caratteristiche di un dispositivo di comunicazione. Per altre informazioni, vedere [proprietà del dispositivo](device-properties.md).

Il codice di esempio seguente ottiene un riferimento all'endpoint del dispositivo di comunicazione predefinito per il rendering di un flusso audio.


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



