---
description: In Windows 7 il pannello Windows di controllo multimediale, Mmsys.cpl, fornisce una nuova scheda Comunicazioni.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Uso di un dispositivo di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dccba320e7b7adbe7804b1cd98bea72e0f1f0de5904ee6b41df08934940ff3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834077"
---
# <a name="using-a-communication-device"></a>Uso di un dispositivo di comunicazione

In Windows 7 il pannello Windows di controllo multimediale, Mmsys.cpl, fornisce una nuova **scheda** Comunicazioni. Questa scheda contiene opzioni che consentono a un utente di impostare opzioni che definiscono la modalità di gestione di un dispositivo di comunicazione da parte *del sistema.* Un dispositivo di comunicazione viene usato principalmente per effettuare o ricevere chiamate telefoniche nel computer. Per un computer con un solo dispositivo di rendering (altoparlante) e un dispositivo di acquisizione (microfono), questi dispositivi audio fungono anche da dispositivi di comunicazione predefiniti. Quando un utente connette un nuovo dispositivo, ad esempio un visore VR USB, il sistema esegue il rilevamento automatico del ruolo del dispositivo cercando le impostazioni di configurazione popolate dall'OEM. Se il sistema determina che un dispositivo è più adatto per la comunicazione, assegna il ruolo **eCommunications** al dispositivo. Per questi dispositivi, il Windows 7 Mmsys.cpl offre  l'opzione Dispositivo di comunicazione predefinito che consente a un utente di selezionare un dispositivo di comunicazione per il rendering audio **(scheda** Riproduzione) e l'acquisizione audio **(scheda** Registrazione). Il sistema esegue il rilevamento automatico dei ruoli, ma non imposta un particolare dispositivo da usare per le comunicazioni. Questa operazione deve essere eseguita dall'utente. Il nuovo **ruolo eCommunications** consente a un'applicazione di distinguere tra un dispositivo scelto dall'utente per la gestione delle chiamate telefoniche e un dispositivo da usare come dispositivo multimediale (riproduzione di musica). Ad esempio, se l'utente ha un visore VR e un altoparlante connesso al computer, il sistema assegna il ruolo **eConsole** all'altoparlante e il ruolo **eCommunications** al visore VR. Dopo che l'utente ha selezionato il visore VR da usare come dispositivo di comunicazione, per sviluppare un'applicazione di comunicazione, è possibile impostare come destinazione il visore VR in modo specifico per il rendering di un flusso audio. Un'applicazione che l'utente non può modificare il ruolo del dispositivo assegnato dal sistema. Per altre informazioni sui ruoli dei dispositivi, vedere [Ruoli del dispositivo.](device-roles.md)

Le applicazioni di comunicazione, ad esempio le applicazioni VoIP e Unified Communication, eseranno e riceveranno chiamate telefoniche tramite un computer. Ad esempio, un'applicazione VoIP potrebbe assegnare un flusso che contiene la notifica dell'anello all'endpoint di un set di dispositivi di comunicazione per il rendering dei flussi audio. Inoltre, l'applicazione potrebbe aprire i flussi di input e output vocali nei dispositivi endpoint di acquisizione e rendering impostati come dispositivi di comunicazione.

Per integrare le funzionalità di comunicazione nelle applicazioni, è possibile usare:

-   [API MMDevice:](mmdevice-api.md)per ottenere un riferimento all'endpoint del dispositivo di comunicazione.
-   [WASAPI:](wasapi.md)per eseguire il rendering e l'acquisizione di flussi audio tramite il dispositivo di comunicazione. Il sistema operativo considera il flusso aperto in un dispositivo di comunicazione come un *flusso di comunicazione*.

L'applicazione di comunicazione enumera i dispositivi e fornisce la gestione dei flussi per un flusso di comunicazione (rendering o acquisizione) nello stesso modo in cui gestirebbe un flusso non di comunicazione usando le API core audio.

Una delle funzionalità che è possibile integrare nell'applicazione di comunicazione è *l'attenuazione del* *flusso.* Questo comportamento definisce cosa deve accadere ad altri suoni all'apertura di un flusso di comunicazione, ad esempio quando viene ricevuta una telefonata sul dispositivo di comunicazione. Il sistema potrebbe disattivare o ridurre il volume audio del flusso non di comunicazione a seconda della scelta dell'utente. Il sistema audio genera eventi di intercettazione quando un flusso di comunicazione viene aperto o chiuso per il rendering o l'acquisizione di flussi. Per impostazione predefinita, il sistema operativo offre un'esperienza di controllo predefinita. Un'applicazione multimediale può sostituire il comportamento predefinito e gestire questi eventi per offrire un'esperienza di controllo personalizzata.

Le sezioni seguenti descrivono come usare le API Core Audio per offrire un'esperienza di descrizione personalizzata.

-   [Esperienza di analisi predefinita](stream-attenuation.md)
-   [Disabilitazione dell'esperienza di analisi predefinita](disabling-the-ducking-experience.md)
-   [Fornire un comportamento personalizzato per l'accodamento](providing-a-custom-ducking-experience.md)
-   [Considerazioni sull'implementazione per l'accodamento delle notifiche](handling-audio-ducking-events-from-communication-devices.md)
-   [Recupero di eventi di antartide](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Recupero di un riferimento all'endpoint del dispositivo di comunicazione

Per usare il dispositivo di comunicazione, un client WASAPI diretto deve enumerare i dispositivi usando l'enumeratore dispositivo. Ottenere un riferimento all'endpoint del dispositivo di comunicazione predefinito chiamando [**IMMDeviceEnumerator::GetDefaultAudioEndpoint.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) In questa chiamata, l'applicazione deve **specificare eCommunications nel** parametro *Role* per limitare l'enumerazione dei dispositivi ai dispositivi di comunicazione. Dopo aver creato un riferimento all'endpoint del dispositivo per il dispositivo, è possibile attivare i servizi con ambito per l'endpoint chiamando [**IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Ad esempio, è possibile passare l'identificatore di servizio **\_ IID IAudioClient** per attivare un oggetto client audio e usarlo per la gestione dei flussi, l'identificatore **\_ IAudioEndpointVolume per** ottenere l'accesso ai controlli del volume dell'endpoint del dispositivo di comunicazione o l'identificatore **\_ IId IAudioSessionManager** per attivare la gestione sessione che consente di interagire con il motore dei criteri dell'endpoint. Per informazioni sulle operazioni di flusso, vedere [Gestione dei flussi.](stream-management.md)

Usando il riferimento [**IMMDevice,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) è anche possibile accedere all'archivio delle proprietà per l'endpoint del dispositivo. Questi valori di proprietà, ad esempio il nome descrittivo del dispositivo e il nome del produttore, vengono popolati dall'OEM e consentono a un'applicazione di determinare le caratteristiche di un dispositivo di comunicazione. Per altre informazioni, vedere [Proprietà del dispositivo.](device-properties.md)

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

 

 



