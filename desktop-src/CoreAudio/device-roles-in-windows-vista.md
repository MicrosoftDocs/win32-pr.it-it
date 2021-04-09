---
description: Utilizzo dei ruoli del dispositivo
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Utilizzo dei ruoli del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965895"
---
# <a name="working-with-device-roles"></a>Utilizzo dei ruoli del dispositivo

L' [API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo. L'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) definisce i ruoli del dispositivo supportati dall'API MMDevice.

> [!Note]  
> Sebbene l' [API MMDevice](mmdevice-api.md) supporti i ruoli del dispositivo, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità.

 

Un'applicazione può usare l'API MMDevice per supportare i [ruoli del dispositivo](device-roles.md) tramite i metodi [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) e [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) . Tuttavia, l'interfaccia utente di Windows Vista non supporta l'assegnazione di singoli ruoli a dispositivi diversi. In Windows Vista, l'interfaccia utente consente all'utente di selezionare un dispositivo audio predefinito per il rendering e un dispositivo audio predefinito per l'acquisizione. Quando l'utente seleziona un dispositivo di rendering o acquisizione predefinito, il sistema assegna tutti e tre i ruoli del dispositivo (eConsole, eMultimedia e comunicazioni elettroniche) a tale dispositivo. Le applicazioni non possono modificare i ruoli assegnati a dispositivi endpoint audio. Il sistema operativo consente solo all'utente di assegnare i ruoli del dispositivo.

Un client può registrarsi per ricevere una notifica dall'API MMDevice ogni volta che si verifica una modifica nell'assegnazione dei ruoli ai dispositivi dell'endpoint audio. Quando un ruolo passa da un dispositivo a un altro, il client può scegliere se continuare a riprodurre (o registrare) i flussi attraverso lo stesso dispositivo o per spostare i flussi in un altro dispositivo. Per impostazione predefinita, i flussi continuano a essere riprodotti o registrati tramite il dispositivo originale. In Windows Vista, per passare i flussi a un altro dispositivo, il client deve eliminare i flussi sul dispositivo originale e creare flussi sostitutivi nel nuovo dispositivo. In Windows 7 il client può rimanere in ascolto di nuove notifiche per implementare un commutire senza interruzioni della riproduzione o della sessione di acquisizione. Per altre informazioni, vedere [routing del flusso](stream-routing.md).

Se si prevede di utilizzare Windows Vista per testare l'applicazione, è possibile configurare un ambiente di test per verificare che il comportamento dell'applicazione sia quello previsto quando l'utente può assegnare singoli ruoli del dispositivo a dispositivi diversi. Per altre informazioni, inviare un messaggio di posta elettronica all'indirizzo uaa@microsoft.com.

## <a name="communication-devices"></a>Dispositivi di comunicazione

L'interfaccia utente di Windows 7 è in grado di aggiungere *dispositivi di comunicazione*. Il pannello di controllo **audio** consente all'utente di selezionare un dispositivo di comunicazione predefinito per il rendering e l'acquisizione del flusso audio. Per impostazione predefinita, quando un nuovo dispositivo è connesso al computer, il sistema operativo esegue il rilevamento automatico dei ruoli e determina se il dispositivo è adatto al ruolo eCommunication. Grazie alla destinazione dei dispositivi di comunicazione, è possibile sviluppare applicazioni che usano le API audio di base per implementare soluzioni di comunicazione per PC e telefono. Ad esempio, un'applicazione VoIP può assegnare i flussi di input e output vocali ai dispositivi dell'endpoint di acquisizione e rendering predefiniti con il ruolo comunicazioni elettroniche. Analogamente a qualsiasi altro flusso, un'applicazione di comunicazione deve ottenere un riferimento all'endpoint del dispositivo di comunicazione chiamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In questa chiamata, l'applicazione deve specificare **comunicazioni elettroniche** nel parametro *Role* . Le operazioni di flusso WASAPI su un flusso, aperto su un dispositivo di comunicazione, sono simili a qualsiasi altro flusso audio. L'applicazione di comunicazione può migliorare l'esperienza utente implementando comportamenti come ad esempio ducking gestendo le notifiche dall'endpoint del dispositivo. Per altre informazioni, vedere [uso di un dispositivo di comunicazione](using-the-communication-device.md).

## <a name="automatic-device-role-detection"></a>Rilevamento automatico dei ruoli del dispositivo

Si consideri uno scenario in cui un computer dispone di un dispositivo di rendering predefinito, dei relatori e di un dispositivo di acquisizione predefinito, un microfono. L'utente connette una cuffia USB al computer. Una volta installati i driver appropriati, il sistema operativo tenta di rilevare un ruolo da assegnare per il nuovo dispositivo audio.

In Windows 7 la funzionalità di rilevamento dei ruoli del dispositivo è stata migliorata in modo significativo per determinare i ruoli appropriati adatti ai dispositivi audio. Tutti i dispositivi audio contengono un set di impostazioni di configurazione popolate dal dispositivo OEM, che consentono al sistema di decidere come usare il dispositivo. Queste impostazioni includono informazioni quali la posizione fisica del Jack audio, il tipo di dispositivo, il sottotipo Jack e le funzionalità di rilevamento, in modo che il sistema possa determinare se il dispositivo è collegato. Recuperando questi valori dal dispositivo, il sistema operativo determina il ruolo da assegnare al dispositivo. In questo scenario, il sistema ha eseguito una query sul dispositivo headset USB, ha eseguito il rilevamento automatico del ruolo e ha deciso che il dispositivo è più adatto per essere un dispositivo di comunicazione.

Un'applicazione può anche ottenere informazioni su Jack usando le API di base di audio. Per ulteriori informazioni, vedere [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) e [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ruoli del dispositivo](device-roles.md)
</dt> </dl>

 

 



