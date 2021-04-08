---
description: Informazioni sull'API MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informazioni sull'API MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748778"
---
# <a name="about-mmdevice-api"></a>Informazioni sull'API MMDevice

L'API Windows Multimedia Device (MMDevice) consente ai client audio di individuare i [dispositivi dell'endpoint audio](audio-endpoint-devices.md), determinarne le funzionalità e creare istanze di driver per tali dispositivi.

Il file di intestazione mmdeviceapi. h definisce le interfacce nell'API MMDevice.

L'API MMDevice è costituita da diverse interfacce. Il primo è l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Per accedere alle interfacce nell'API MMDevice, un client ottiene un riferimento all'interfaccia **IMMDeviceEnumerator** di un oggetto enumeratore del dispositivo chiamando la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , come illustrato nel frammento di codice seguente:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



Nel frammento di codice precedente, CLSID \_ MMDeviceEnumerator ed IID \_ IMMDeviceEnumerator sono i valori GUID collegati come attributi all'oggetto della classe **MMDeviceEnumerator** e all'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . La chiamata [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passa questi valori per riferimento. `hr`La variabile è di tipo **HRESULT** e la variabile `pEnumerator` è un puntatore all'interfaccia **IMMDeviceEnumerator** di un oggetto enumeratore del dispositivo. **IMMDeviceEnumerator** fornisce metodi per l'enumerazione di dispositivi endpoint audio. Per informazioni sull'operatore **\_ \_ uuidof** , sulla funzione **CoCreateInstance** e sulle costanti CLSCTX \_ *xxx* , vedere la documentazione Windows SDK.

Tramite l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , il client può ottenere riferimenti ad altre interfacce nell'API MMDevice. L'API MMDevice implementa le interfacce seguenti.



| Interfaccia                                          | Descrizione                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Rappresenta un dispositivo audio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Rappresenta una raccolta di dispositivi audio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Fornisce metodi per l'enumerazione dei dispositivi audio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Rappresenta un dispositivo endpoint audio.            |



 

Inoltre, i client dell'API MMDevice che richiedono la notifica delle modifiche di stato nei dispositivi dell'endpoint audio devono implementare la seguente interfaccia.



| Interfaccia                                              | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornisce notifiche quando viene aggiunto o rimosso un dispositivo endpoint audio, quando lo stato o le proprietà di un dispositivo cambiano oppure quando viene apportata una modifica al ruolo predefinito assegnato a un dispositivo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
