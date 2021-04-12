---
title: Esecuzione del rilevamento della prossimità
description: Esecuzione del rilevamento della prossimità
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK, esecuzione del rilevamento della prossimità
- Windows Media Format SDK, rilevamento della prossimità
- Advanced Systems Format (ASF), esecuzione del rilevamento della prossimità
- ASF (Advanced Systems Format), esecuzione del rilevamento della prossimità
- Advanced Systems Format (ASF), rilevamento prossimità
- ASF (formato avanzato dei sistemi), rilevamento della prossimità
- Digital Rights Management (DRM), esecuzione del rilevamento della prossimità
- DRM (Digital Rights Management), esecuzione del rilevamento della prossimità
- Digital Rights Management (DRM), rilevamento prossimità
- DRM (Digital Rights Management), rilevamento della prossimità
- rilevamento della prossimità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398534"
---
# <a name="performing-proximity-detection"></a>Esecuzione del rilevamento della prossimità

Prima di poter trasmettere i dati crittografati a un dispositivo registrato nel protocollo Windows Media DRM 10 per i dispositivi di rete, è necessario eseguire un processo denominato rilevamento della prossimità (chiamato anche convalida). Questo processo comporta l'invio di messaggi al dispositivo e la ricezione delle risposte. Il tempo necessario per ricevere una risposta viene usato per determinare se il dispositivo è sufficientemente vicino al computer della rete per ricevere dati protetti. Verificare che il dispositivo sia fisicamente vicino al computer client nella rete consente di impedire lo spoofing e altri accessi non autorizzati.

Quando il rilevamento della prossimità viene completato correttamente, il dispositivo viene definito valido. È possibile verificare se un dispositivo è valido chiamando il metodo [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) . I dispositivi devono essere convalidati ogni 48 ore. Un dispositivo che è stato convalidato più di 48 ore prima dell'esecuzione del programma deve essere riconvalidato eseguendo di nuovo il processo di rilevamento della prossimità.

Per eseguire il rilevamento della prossimità, è necessario stabilire le comunicazioni con il dispositivo e quindi chiamare il metodo [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) . Il processo di rilevamento viene completato in modo asincrono dai componenti DRM interni di Windows Media Format SDK. L'applicazione deve includere un'implementazione dell'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) per elaborare i messaggi di rilevamento prossimità.

Il processo di rilevamento della prossimità invia due messaggi: un messaggio di risultato e un messaggio di completamento.

Al \_ \_ termine del processo di rilevamento, viene inviato il messaggio di risultato WMT di prossimità. Il parametro *HR* del metodo di callback [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se il dispositivo è stato trovato abbastanza vicino al computer client. Se il parametro *HR* del messaggio di risultato indica esito positivo, il parametro *PValue* contiene un **valore DWORD** che specifica la latenza misurata al dispositivo in millisecondi.

Il messaggio di completamento, \_ prossimità WMT \_ completata, viene inviato quando il rilevamento viene finalizzato. È consigliabile rilasciare l'interfaccia [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) solo dopo la ricezione di questo messaggio.

Quando il rilevamento della prossimità per un dispositivo ha esito positivo, il database di registrazione del dispositivo viene aggiornato automaticamente. Le chiamate successive a [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) restituiscono **true** fino a quando non sono trascorse 48 ore e il dispositivo deve essere riconvalidato.

**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del protocollo Windows Media DRM 10 per i dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




