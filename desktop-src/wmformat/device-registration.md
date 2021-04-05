---
title: Registrazione del dispositivo
description: Registrazione del dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, registrazione del dispositivo
- Windows Media Format SDK, registrazione dei dispositivi
- ASF (Advanced Systems Format), registrazione del dispositivo
- ASF (formato avanzato dei sistemi), registrazione del dispositivo
- ASF (Advanced Systems Format), registrazione dei dispositivi
- ASF (Advanced Systems Format), registrazione dei dispositivi
- Digital Rights Management (DRM), registrazione del dispositivo
- DRM (Digital Rights Management), registrazione del dispositivo
- Digital Rights Management (DRM), registrazione dei dispositivi
- DRM (Digital Rights Management), registrazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046306"
---
# <a name="device-registration"></a>Registrazione del dispositivo

Windows Media Format SDK consente di accedere al database di registrazione del dispositivo. Questo database è protetto nel computer client e viene usato per registrare i dispositivi che supportano Windows Media DRM 10 per i dispositivi di rete.

Quando un dispositivo viene aggiunto a una rete a cui è connesso il computer client, il dispositivo tenta di contattare un'applicazione di trasmissione di Windows Media DRM 10 per dispositivi di rete. Dopo aver stabilito le comunicazioni, il dispositivo invia un messaggio di richiesta di registrazione.

Quando riceve un messaggio di richiesta di registrazione, l'applicazione deve eseguire i passaggi seguenti:

1.  Analizzare il messaggio chiamando il metodo [**IWMDRMMessageParser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) . Questo metodo recupera il certificato del dispositivo e il numero di serie del dispositivo, entrambi necessari per identificare il dispositivo.
2.  Chiamare il metodo [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando il numero di serie del certificato e del dispositivo recuperato nel passaggio 1. Se il dispositivo viene trovato, è già registrato ed è possibile ignorare il passaggio successivo.
3.  Chiamare il metodo [**IWMDeviceRegistration:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) per aggiungere il dispositivo al database di registrazione del dispositivo.

Per accedere alle informazioni relative a qualsiasi dispositivo nel database di registrazione, è possibile recuperare l'oggetto dispositivo registrato associato. Esistono due modi per ottenere un oggetto dispositivo registrato. Se il certificato e il numero di serie del dispositivo sono disponibili, è possibile chiamare il metodo [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) . Se il certificato e il numero di serie del dispositivo non sono disponibili, è possibile enumerare tutti i dispositivi nel database chiamando [**IWMDeviceRegistration:: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguito da chiamate ripetute a [**IWMDeviceRegistration:: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) fino a quando una chiamata non restituisce \_ false.

Prima che l'applicazione possa inviare dati a un dispositivo, è necessario assicurarsi che il dispositivo sia approvato, convalidato e aperto.

L'approvazione del dispositivo deve coinvolgere l'interazione con l'utente. Quando un dispositivo invia un messaggio di registrazione, l'applicazione può chiedere all'utente di decidere se il dispositivo è quello che dovrebbe ricevere i dati dell'utente. Aggiornare quindi il database di registrazione del dispositivo chiamando il metodo [**IWMRegisteredDevice:: approv**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , passando **true** o **false** nel modo appropriato.

La convalida è detta anche rilevamento della prossimità. Si tratta di un processo mediante il quale gli oggetti DRM interni di Windows Media Format SDK determinano se il dispositivo è sufficientemente "vicino" al computer che esegue l'applicazione per la trasmissione sicura dei supporti. La prossimità è determinata dal tempo necessario per ottenere una risposta a un messaggio. Questa funzionalità è destinata a impedire a utenti non autorizzati di accedere alla rete e di ottenere il supporto protetto. Per ulteriori informazioni, vedere [esecuzione del rilevamento della prossimità](performing-proximity-detection.md).

Per aprire un dispositivo, chiamare [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Uso del protocollo Windows Media DRM 10 per i dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




