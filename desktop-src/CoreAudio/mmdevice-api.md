---
description: Informazioni sull'API MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informazioni sull'API MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e2f33c6969e00006c12b0bc6dc1ba37b70c5ff38ea2846633d5eb61da03b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077545"
---
# <a name="about-mmdevice-api"></a>Informazioni sull'API MMDevice

L Windows API MmDevice (Multimedia Device) consente ai client audio di individuare i dispositivi [endpoint audio,](audio-endpoint-devices.md)determinarne le funzionalità e creare istanze di driver per tali dispositivi.

Il file di intestazione Mmdeviceapi.h definisce le interfacce nell'API MMDevice.

L'API MMDevice è costituita da diverse interfacce. Il primo di questi è [**l'interfaccia IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Per accedere alle interfacce nell'API MMDevice, un client ottiene un riferimento **all'interfaccia IMMDeviceEnumerator** di un oggetto device-enumerator chiamando la funzione [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) come illustrato nel frammento di codice seguente:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



Nel frammento di codice precedente CLSID MMDeviceEnumerator e IID IMMDeviceEnumerator sono i valori GUID associati come attributi all'oggetto classe \_ \_ **MMDeviceEnumerator** e [**all'interfaccia IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) La [**chiamata CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passa questi valori per riferimento. La variabile è di tipo HRESULT e la variabile è un puntatore `hr`  `pEnumerator` all'interfaccia **IMMDeviceEnumerator** di un oggetto device-enumerator. **IMMDeviceEnumerator fornisce** metodi per l'enumerazione dei dispositivi endpoint audio. Per informazioni sull'operatore **\_ \_ uuidof,** sulla funzione **CoCreateInstance** e sulle costanti CLSCTX Xxx, vedere la documentazione \_  Windows SDK.

Tramite [**l'interfaccia IMMDeviceEnumerator,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) il client può ottenere riferimenti alle altre interfacce nell'API MMDevice. L'API MMDevice implementa le interfacce seguenti.



| Interfaccia                                          | Descrizione                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Rappresenta un dispositivo audio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Rappresenta una raccolta di dispositivi audio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Fornisce metodi per enumerare i dispositivi audio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Rappresenta un dispositivo endpoint audio.            |



 

Inoltre, i client dell'API MMDevice che richiedono la notifica delle modifiche dello stato nei dispositivi endpoint audio devono implementare l'interfaccia seguente.



| Interfaccia                                              | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornisce notifiche quando un dispositivo endpoint audio viene aggiunto o rimosso, quando lo stato o le proprietà di un dispositivo cambiano o quando viene apportata una modifica al ruolo predefinito assegnato a un dispositivo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
