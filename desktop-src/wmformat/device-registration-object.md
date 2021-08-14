---
title: Oggetto Registrazione dispositivo
description: Oggetto Registrazione dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows MEDIA Format SDK, oggetti registrazione dispositivo
- Advanced Systems Format (ASF), oggetti di registrazione del dispositivo
- ASF (Advanced Systems Format),device registration objects
- oggetti, oggetti di registrazione del dispositivo
- oggetti registrazione dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4594b17f6824e4e3a9e7690e5ea933e24670e9c8b5d95feb16e555f577f87f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433887"
---
# <a name="device-registration-object"></a>Oggetto Registrazione dispositivo

L'oggetto registrazione del dispositivo gestisce il database di registrazione del dispositivo. In questo database vengono archiviate informazioni sui dispositivi di rete, ad esempio i lettori video principali, connessi al computer client. Lo scopo principale del database di registrazione dei dispositivi è gestire i dispositivi che usano il protocollo Windows Media DRM 10 per dispositivi di rete per ricevere flussi di dati protetti.

Se l'applicazione supporta Windows Media DRM 10 per i dispositivi di rete, è necessario usare le interfacce di questo oggetto per registrare i dispositivi di rete e convalidare tali dispositivi. È anche possibile usare il database di registrazione dei dispositivi per archiviare le informazioni sui dispositivi di rete che non usano Windows Media DRM 10 per i dispositivi di rete, anche se non tutte le informazioni nel database verranno applicate a tali dispositivi.

L'oggetto registrazione dispositivo viene creato dalla [**funzione WMCreateDeviceRegistration,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) che imposta un puntatore a **un'interfaccia IWMDeviceRegistration.** Gli altri metodi dell'oggetto registrazione dispositivo possono essere ottenuti chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto di registrazione del dispositivo.



| Interfaccia                                              | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Gestisce il database di registrazione del dispositivo. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analizza i messaggi inviati dai dispositivi.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Gestisce la convalida dei dispositivi.                |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per usare i metodi **dell'interfaccia IWMProximityDetection.**



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve i messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 




