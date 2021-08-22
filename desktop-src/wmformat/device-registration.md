---
title: Registrazione del dispositivo
description: Registrazione del dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, registrazione del dispositivo
- Windows Media Format SDK, registrazione dei dispositivi
- Advanced Systems Format (ASF), registrazione del dispositivo
- ASF (Advanced Systems Format),registrazione del dispositivo
- Advanced Systems Format (ASF), registrazione dei dispositivi
- ASF (Advanced Systems Format), registrazione dei dispositivi
- digital rights management (DRM), registrazione del dispositivo
- DRM (digital rights management),registrazione del dispositivo
- digital rights management (DRM), registrazione dei dispositivi
- DRM (digital rights management), registrazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2efbfefaaabf3af0a33f304ad2cc32f7fe3b84691da8242203eddbb18fdb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027929"
---
# <a name="device-registration"></a>Registrazione del dispositivo

L Windows Media Format SDK fornisce l'accesso al database di registrazione del dispositivo. Questo database è protetto nel computer client e viene usato per registrare i dispositivi che supportano Windows Media DRM 10 per i dispositivi di rete.

Quando un dispositivo viene aggiunto a una rete a cui è connesso il computer client, il dispositivo tenta di contattare un'applicazione trasmettitore Windows Media DRM 10 per dispositivi di rete. Dopo aver stabilito le comunicazioni, il dispositivo invia un messaggio di richiesta di registrazione.

L'applicazione deve eseguire la procedura seguente quando riceve un messaggio di richiesta di registrazione:

1.  Analizzare il messaggio chiamando il [**metodo IWMDRMMessageParser::P arseRegistrationReqMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) Questo metodo recupera il certificato del dispositivo e il numero di serie del dispositivo, entrambi necessari per identificare il dispositivo.
2.  Chiamare il [**metodo IWMDeviceRegistration::GetRegisteredDeviceByID,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) passando il certificato e il numero di serie del dispositivo recuperati nel passaggio 1. Se il dispositivo viene trovato, è già registrato ed è possibile ignorare il passaggio successivo.
3.  Chiamare il [**metodo IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) per aggiungere il dispositivo al database di registrazione del dispositivo.

È possibile accedere alle informazioni su qualsiasi dispositivo nel database di registrazione recuperando l'oggetto dispositivo registrato associato. Esistono due modi per ottenere un oggetto dispositivo registrato. Se si dispone del certificato e del numero di serie del dispositivo, è possibile chiamare il metodo [**IWMDeviceRegistration::GetRegisteredDeviceByID.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) Se non si dispone del certificato e del numero di serie del dispositivo, è possibile enumerare tutti i dispositivi nel database chiamando [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguito da chiamate ripetute a [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) finché una chiamata non restituisce S \_ FALSE.

Prima che l'applicazione possa inviare dati a un dispositivo, è necessario assicurarsi che il dispositivo sia approvato, convalidato e aperto.

L'approvazione del dispositivo deve comportare l'interazione con l'utente. Quando un dispositivo invia un messaggio di registrazione, l'applicazione può chiedere all'utente di decidere se il dispositivo deve ricevere i dati dell'utente. Aggiornare quindi il database di registrazione del dispositivo chiamando il [**metodo IWMRegisteredDevice::Approve,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) passando **TRUE** o **FALSE** in base alle esigenze.

La convalida è detta anche rilevamento di prossimità. Si tratta di un processo tramite il quale gli oggetti DRM interni di Windows Media Format SDK determinano se il dispositivo è sufficientemente "vicino" al computer che esegue l'applicazione per trasmettere in modo sicuro i supporti. La prossimità è determinata dal tempo necessario per ottenere una risposta a un messaggio. Questa funzionalità ha lo scopo di impedire a utenti non autorizzati di accedere alla rete e ottenere i supporti protetti. Per altre informazioni, vedere [Esecuzione del rilevamento di prossimità](performing-proximity-detection.md).

Per aprire un dispositivo, chiamare [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Uso del Windows DRM 10 per dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




