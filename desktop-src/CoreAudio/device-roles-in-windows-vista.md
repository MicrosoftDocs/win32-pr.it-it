---
description: Uso dei ruoli del dispositivo
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Uso dei ruoli del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7e3d0d2612415ddc3f72571774f11a2d62c911290b156be7efb543c48546e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406894"
---
# <a name="working-with-device-roles"></a>Uso dei ruoli del dispositivo

[L'API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo. [**L'enumerazione ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) definisce i ruoli del dispositivo supportati dall'API MMDevice.

> [!Note]  
> Anche se [l'API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità.

 

Un'applicazione può usare l'API MMDevice per supportare i ruoli [del](device-roles.md) dispositivo tramite i metodi [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) e [**IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) Tuttavia, l'interfaccia utente in Windows Vista non supporta l'assegnazione di singoli ruoli a dispositivi diversi. In Windows Vista, l'interfaccia utente consente all'utente di selezionare un dispositivo audio predefinito per il rendering e un dispositivo audio predefinito per l'acquisizione. Quando l'utente seleziona un dispositivo di rendering o acquisizione predefinito, il sistema assegna tutti e tre i ruoli del dispositivo (eConsole, eMultimedia ed eCommunications) a tale dispositivo. Le applicazioni non possono modificare i ruoli assegnati ai dispositivi endpoint audio. Il sistema operativo consente solo all'utente di assegnare i ruoli del dispositivo.

Un client può registrarsi per ricevere una notifica dall'API MMDevice ogni volta che si verifica una modifica nell'assegnazione dei ruoli ai dispositivi endpoint audio. Quando un ruolo passa da un dispositivo a un altro, il client può scegliere se continuare a riprodurre (o registrare) i flussi attraverso lo stesso dispositivo o passare i flussi a un altro dispositivo. Per impostazione predefinita, i flussi continuano a essere riprodotti (o registrati) tramite il dispositivo originale. In Windows Vista, per passare i flussi a un altro dispositivo, il client deve eliminare i flussi nel dispositivo originale e creare flussi sostitutivi nel nuovo dispositivo. In Windows 7, il client può restare in ascolto di nuove notifiche per implementare un commutatore facile senza interrompere la riproduzione o la sessione di acquisizione. Per altre informazioni, vedere [Routing di flusso](stream-routing.md).

Se si prevede di usare Windows Vista per testare l'applicazione, è possibile configurare un ambiente di test per verificare che l'applicazione si comporti come previsto quando l'utente può assegnare singoli ruoli del dispositivo a dispositivi diversi. Per altre informazioni, inviare un messaggio di posta elettronica all'indirizzo uaa@microsoft.com.

## <a name="communication-devices"></a>Dispositivi di comunicazione

L Windows'interfaccia utente di Windows 7 è in grado di aggiungere dispositivi *di comunicazione.* Il **pannello di** controllo Audio consente all'utente di selezionare un dispositivo di comunicazione predefinito per il rendering e l'acquisizione del flusso audio. Per impostazione predefinita, quando un nuovo dispositivo è connesso al computer, il sistema operativo esegue il rilevamento automatico del ruolo e determina se il dispositivo è adatto per il ruolo eCommunication. La destinazione dei dispositivi di comunicazione consente di sviluppare applicazioni che usano le API Audio core per implementare soluzioni di comunicazione PC-phone. Ad esempio, un'applicazione VoIP potrebbe assegnare i flussi di input e output vocali ai dispositivi endpoint di acquisizione e rendering predefiniti con il ruolo eCommunications. Come qualsiasi altro flusso, un'applicazione di comunicazione deve ottenere un riferimento all'endpoint del dispositivo di comunicazione chiamando [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In questa chiamata, l'applicazione deve **specificare eCommunications** nel *parametro Role.* Le operazioni di flusso WASAPI su un flusso, aperte in un dispositivo di comunicazione, sono simili a qualsiasi altro flusso audio. L'applicazione di comunicazione può migliorare l'esperienza utente implementando comportamenti come l'abbassamento delle prestazioni gestendo le notifiche dall'endpoint del dispositivo. Per altre informazioni, vedere [Uso di un dispositivo di comunicazione](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Rilevamento automatico del ruolo del dispositivo

Si consideri uno scenario in cui un computer ha un dispositivo di rendering predefinito, gli altoparlanti e un dispositivo di acquisizione predefinito, un microfono. L'utente connette un visore USB al computer. Dopo aver installato i driver appropriati, il sistema operativo tenta di rilevare un ruolo da assegnare per il nuovo dispositivo audio.

In Windows 7, la funzionalità di rilevamento del ruolo del dispositivo è stata migliorata in modo significativo per determinare i ruoli appropriati adatti per i dispositivi audio. Tutti i dispositivi audio contengono un set di impostazioni di configurazione popolate dall'OEM del dispositivo, che consentono al sistema di decidere come usare il dispositivo. Queste impostazioni includono informazioni quali la posizione fisica del jack audio del tipo di dispositivo, il sottotipo jack e le funzionalità di rilevamento in modo che il sistema possa determinare se il dispositivo è collegato. Recuperando questi valori dal dispositivo, il sistema operativo determina il ruolo da assegnare al dispositivo. In questo scenario, il sistema ha eseguito query sul dispositivo visore USB, ha eseguito il rilevamento automatico dei ruoli e ha deciso che il dispositivo è più adatto per essere un dispositivo di comunicazione.

Un'applicazione può anche ottenere informazioni sul jack usando le API Core Audio. Per altre informazioni, vedere [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) e [**IKsJackDescription2.**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ruoli del dispositivo](device-roles.md)
</dt> </dl>

 

 



