---
title: Oggetto registrazione dispositivo
description: Oggetto registrazione dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK, oggetti registrazione dispositivo
- ASF (Advanced Systems Format), oggetti di registrazione del dispositivo
- ASF (Advanced Systems Format), oggetti di registrazione del dispositivo
- oggetti, oggetti di registrazione del dispositivo
- oggetti di registrazione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299409"
---
# <a name="device-registration-object"></a>Oggetto registrazione dispositivo

L'oggetto registrazione dispositivo gestisce il database di registrazione del dispositivo. In questo database vengono archiviate le informazioni sui dispositivi di rete, ad esempio i lettori video di set-top, che sono connessi al computer client. Lo scopo principale del database di registrazione del dispositivo è quello di gestire i dispositivi che usano il protocollo Windows Media DRM 10 per i dispositivi di rete per la ricezione di flussi di dati protetti.

Se l'applicazione supporta Windows Media DRM 10 per i dispositivi di rete, è necessario utilizzare le interfacce di questo oggetto per registrare i dispositivi di rete e per convalidare tali dispositivi. È anche possibile usare il database di registrazione del dispositivo per archiviare le informazioni sui dispositivi di rete che non usano Windows Media DRM 10 per i dispositivi di rete, anche se non tutte le informazioni presenti nel database verranno applicate a tali dispositivi.

L'oggetto registrazione del dispositivo viene creato dalla funzione [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , che imposta un puntatore a un'interfaccia **IWMDeviceRegistration** . Gli altri metodi dell'oggetto registrazione del dispositivo possono essere ottenuti chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto registrazione del dispositivo.



| Interfaccia                                              | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Gestisce il database di registrazione del dispositivo. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analizza i messaggi inviati dai dispositivi.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Gestisce la convalida del dispositivo.                |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per usare i metodi dell'interfaccia **IWMProximityDetection** .



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve i messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 




