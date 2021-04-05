---
title: Conversione di un file di DRM-Protected in un flusso Windows Media DRM 10 per dispositivi di rete
description: Conversione di un file di DRM-Protected in un flusso Windows Media DRM 10 per dispositivi di rete
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK, conversione di file protetti da DRM
- Windows Media Format SDK, file protetti da DRM
- ASF (Advanced Systems Format), conversione di file protetti da DRM
- ASF (Advanced Systems Format), conversione di file protetti da DRM
- ASF (Advanced Systems Format), file protetti da DRM
- ASF (Advanced Systems Format), file protetti da DRM
- Digital Rights Management (DRM), conversione di file protetti da DRM
- DRM (Digital Rights Management), conversione di file protetti da DRM
- Digital Rights Management (DRM), file protetti da DRM
- DRM (Digital Rights Management), file protetti da DRM
- Windows Media Format SDK, Windows Media DRM 10 per i dispositivi di rete
- Windows Media Format SDK, DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), Windows Media DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), Windows Media DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), DRM 10 per i dispositivi di rete
- Windows Media DRM 10 per i dispositivi di rete, conversione di file protetti da DRM
- DRM 10 per i dispositivi di rete, conversione di file protetti da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723599"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Conversione di un file di DRM-Protected in un flusso Windows Media DRM 10 per dispositivi di rete

Dopo la registrazione e la convalida di un dispositivo, è possibile iniziare l'elaborazione dei messaggi di richiesta di licenza. I messaggi di richiesta di licenza vengono inviati dai dispositivi quando è necessaria un'azione da parte dell'applicazione. L'unica azione attualmente supportata è "Play", che è una richiesta di dati protetti per la riproduzione.

Quando si riceve un messaggio di richiesta di licenza, attenersi alla procedura seguente:

1.  Analizzare il messaggio di richiesta di licenza chiamando il metodo [**IWMDRMMessageParser::P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) .
2.  Ottenere l'interfaccia [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) per il dispositivo chiamando il metodo [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando il certificato e il numero di serie ottenuti nel passaggio 1.
3.  Verificare che il dispositivo sia pronto per ricevere dati protetti:
    -   Chiamare [**IWMRegisteredDevice:: unapproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) per verificare che il dispositivo sia stato approvato. L'approvazione deve essere sempre basata sulla preferenza dell'utente.
    -   Chiamare [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) per verificare che il dispositivo sia stato convalidato entro le ultime 48 ore. Se il dispositivo non è valido, è necessario eseguire il rilevamento della prossimità. Per ulteriori informazioni, vedere [esecuzione del rilevamento della prossimità](performing-proximity-detection.md).
    -   Chiamare [**IWMRegisteredDevice:: di apertura**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) per verificare che il dispositivo sia stato aperto. Se il dispositivo non è aperto, è possibile aprirlo chiamando [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Nel computer è possibile aprire solo 10 dispositivi alla volta. È possibile che sia necessario chiudere un altro dispositivo prima di poter aprire quello per cui si sta elaborando la richiesta. Per chiudere un dispositivo, chiamare il metodo [**IWMRegisteredDevice:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) .
4.  Creare un'istanza dell'oggetto transcryptor DRM chiamando la funzione [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) .
5.  Chiamare il metodo [**IWMDRMTranscryptor:: Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) per inizializzare il transcryptor. Questo metodo accetta un puntatore all'implementazione dell'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) , che usa per recapitare i messaggi di stato. Questo metodo restituisce anche un messaggio di richiesta di licenza che deve essere inviato al dispositivo prima di continuare.
6.  Quando il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione riceve il \_ messaggio di stato init di WMT Transcriptor \_ , chiamare il metodo [**IWMDRMTranscryptor:: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) per cercare la posizione iniziale appropriata nel file. Per iniziare all'inizio del file, è necessario chiamare **Seek** con Time 0.
7.  Il Transcriptor Invia un \_ \_ messaggio ricercato di transcryptor WMT quando è pronto per il recapito dei dati dal file alla nuova ora di presentazione. Eseguire chiamate ripetute al metodo [**IWMDRMTranscryptor:: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) per ottenere blocchi convertiti di dati multimediali. Ogni chiamata è asincrona e non è completa fino a quando non \_ viene ricevuto un messaggio di lettura WMT TRANScryptor \_ . Quando si riceve il messaggio, è possibile inviare i dati al dispositivo di destinazione.
8.  Quando si riceve un messaggio di lettura di WMT \_ TRANScryptor \_ con il parametro *HR* impostato su NS \_ S \_ Transcriptor \_ EOF, viene letto l'intero file. A questo punto, chiamare il metodo [**IWMDRMTranscryptor:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) per chiudere il file e liberare risorse.
9.  Quando \_ viene ricevuto il messaggio WMT TRANScriptor \_ Closed, è possibile rilasciare l'interfaccia [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del protocollo Windows Media DRM 10 per i dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




