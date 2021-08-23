---
title: Esecuzione del rilevamento di prossimità
description: Esecuzione del rilevamento di prossimità
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK, esecuzione del rilevamento di prossimità
- Windows MEDIA Format SDK, rilevamento prossimità
- Advanced Systems Format (ASF), esecuzione del rilevamento di prossimità
- ASF (Advanced Systems Format), esecuzione del rilevamento di prossimità
- Advanced Systems Format (ASF), rilevamento prossimità
- ASF (Advanced Systems Format), rilevamento prossimità
- digital rights management (DRM), esecuzione del rilevamento di prossimità
- DRM (Digital Rights Management), esecuzione del rilevamento di prossimità
- digital rights management (DRM), rilevamento prossimità
- DRM (Digital Rights Management),rilevamento prossimità
- rilevamento di prossimità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b13d56e4c2b1fea0da1ff761f6d915680ff89c42747b9faf4260184ae4205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963980"
---
# <a name="performing-proximity-detection"></a>Esecuzione del rilevamento di prossimità

Prima di poter trasmettere i dati crittografati a un dispositivo registrato nel protocollo Windows Media DRM 10 per dispositivi di rete, è necessario eseguire un processo denominato rilevamento di prossimità (detto anche convalida). Questo processo comporta l'invio di messaggi al dispositivo e la ricezione di risposte. Il tempo necessario per ricevere una risposta viene usato per determinare se il dispositivo è "abbastanza vicino" al computer in rete per ricevere dati protetti. Verificare che il dispositivo sia fisicamente vicino al computer client in rete consente di impedire lo spoofing e altri accessi non autorizzati.

Quando il rilevamento di prossimità viene completato correttamente, il dispositivo viene detto valido. È possibile controllare se un dispositivo è valido chiamando il [**metodo IWMRegisteredDevice::IsValid.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) I dispositivi devono essere convalidati ogni 48 ore. Un dispositivo convalidato più di 48 ore prima dell'esecuzione del programma deve essere riconvalidato eseguendo di nuovo il processo di rilevamento della prossimità.

Per eseguire il rilevamento di prossimità, è necessario stabilire le comunicazioni con il dispositivo e quindi chiamare il [**metodo IWMProximityDetection::StartDetection.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) Il processo di rilevamento viene completato in modo asincrono dai componenti DRM interni di Windows Media Format SDK. L'applicazione deve includere un'implementazione [**dell'interfaccia IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) per elaborare i messaggi di rilevamento di prossimità.

Il processo di rilevamento di prossimità invii due messaggi: un messaggio di risultato e un messaggio di completamento.

Il messaggio di risultato, WMT \_ PROXIMITY RESULT, viene inviato al termine del processo di \_ rilevamento. Il *parametro hr* del metodo di callback [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se il dispositivo è stato trovato abbastanza vicino al computer client. Se il *parametro hr* del messaggio di risultato indica l'esito positivo, il *parametro pValue* contiene un **valore DWORD** che specifica la latenza misurata per il dispositivo in millisecondi.

Il messaggio di completamento, WMT \_ PROXIMITY \_ COMPLETED, viene inviato quando il rilevamento viene finalizzato. È consigliabile rilasciare [**l'interfaccia IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) solo dopo aver ricevuto questo messaggio.

Quando il rilevamento di prossimità per un dispositivo ha esito positivo, il database di registrazione del dispositivo viene aggiornato automaticamente. Le chiamate successive [**a IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) restituiranno **TRUE** fino a quando non sono trascorse 48 ore e il dispositivo deve essere riconvalidato.

**Nota** DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del protocollo Windows Media DRM 10 per dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




