---
title: Conversione di un DRM-Protected file in un flusso Windows Media DRM 10 per dispositivi di rete
description: Conversione di un DRM-Protected file in un flusso Windows Media DRM 10 per dispositivi di rete
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK, conversione di file protetti da DRM
- Windows Media Format SDK, file protetti da DRM
- Advanced Systems Format (ASF), conversione di file protetti da DRM
- ASF (Advanced Systems Format), conversione di file protetti da DRM
- Advanced Systems Format (ASF), file protetti da DRM
- ASF (Advanced Systems Format), file protetti da DRM
- digital rights management (DRM), conversione di file protetti da DRM
- DRM (digital rights management), conversione di file protetti da DRM
- digital rights management (DRM), file protetti da DRM
- DRM (digital rights management),file protetti da DRM
- Windows Media Format SDK,Windows Media DRM 10 per dispositivi di rete
- Windows Media Format SDK,DRM 10 per dispositivi di rete
- Advanced Systems Format (ASF), Windows Media DRM 10 per dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per dispositivi di rete
- Advanced Systems Format (ASF), DRM 10 per dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per dispositivi di rete
- DRM (Digital Rights Management), Windows Media DRM 10 per dispositivi di rete
- DRM (digital rights management), Windows Media DRM 10 per dispositivi di rete
- digital rights management (DRM), DRM 10 per dispositivi di rete
- DRM (digital rights management),DRM 10 per dispositivi di rete
- Windows Media DRM 10 per dispositivi di rete, conversione di file protetti da DRM
- DRM 10 per dispositivi di rete, conversione di file protetti da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe5aa16b13f41c0376da84237a846612b7ae6e730e630be6ec4a45ce48ff4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848912"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Conversione di un DRM-Protected file in un flusso Windows Media DRM 10 per dispositivi di rete

Dopo che un dispositivo è stato registrato e convalidato, è possibile iniziare a elaborare i messaggi di richiesta di licenza da esso. I messaggi di richiesta di licenza vengono inviati dai dispositivi quando è necessaria un'azione dall'applicazione. L'unica azione attualmente supportata è "Play", ovvero una richiesta di dati sicuri per la riproduzione.

Quando si riceve un messaggio di richiesta di licenza, è necessario seguire questa procedura:

1.  Analizzare il messaggio di richiesta di licenza chiamando il [**metodo IWMDRMMessageParser::P arseLicenseRequestMsg.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg)
2.  Ottenere [**l'interfaccia IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) per il dispositivo chiamando il metodo [**IWMDeviceRegistration::GetRegisteredDeviceByID,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) passando il certificato e il numero di serie ottenuti nel passaggio 1.
3.  Verificare che il dispositivo sia pronto per ricevere dati sicuri:
    -   Chiamare [**IWMRegisteredDevice::IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) per verificare che il dispositivo sia stato approvato. L'approvazione deve essere sempre basata sulle preferenze dell'utente.
    -   Chiamare [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) per verificare che il dispositivo sia stato convalidato nelle ultime 48 ore. Se il dispositivo non è valido, è necessario eseguire il rilevamento della prossimità. Per altre informazioni, vedere [Esecuzione del rilevamento di prossimità](performing-proximity-detection.md).
    -   Chiamare [**IWMRegisteredDevice::IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) per verificare che il dispositivo sia stato aperto. Se il dispositivo non è aperto, è possibile aprirlo chiamando [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Nel computer possono essere aperti solo 10 dispositivi alla volta. Potrebbe essere necessario chiudere un altro dispositivo prima di aprire quello per cui si sta elaborando la richiesta. Per chiudere un dispositivo, chiamare il [**metodo IWMRegisteredDevice::Close.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close)
4.  Creare un'istanza dell'oggetto transcryptor DRM chiamando la [**funzione WMCreateDRMTranscryptor.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)
5.  Chiamare il [**metodo IWMDRMTranscryptor::Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) per inizializzare il transcryptor. Questo metodo accetta un puntatore all'implementazione [**dell'interfaccia IWMStatusCallback,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) che usa per recapitare i messaggi di stato. Questo metodo restituisce anche un messaggio di richiesta di licenza che deve essere inviato al dispositivo prima di continuare.
6.  Quando il metodo [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione riceve il messaggio di stato INIT WMT TRANSCRYPTOR, chiamare il metodo \_ \_ [**IWMDRMTranscryptor::Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) per cercare la posizione iniziale appropriata nel file. Per iniziare all'inizio del file, è necessario chiamare **Seek** con l'ora 0.
7.  Il transcryptor invia un messaggio WMT TRANSCRYPTOR SEEKED quando è pronto per recapitare i dati dal \_ file al nuovo momento della \_ presentazione. Effettuare chiamate ripetute al [**metodo IWMDRMTranscryptor::Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) per ottenere blocchi convertiti di dati multimediali. Ogni chiamata è asincrona e non viene completata fino a quando non viene ricevuto un messaggio WMT \_ TRANSCRYPTOR \_ READ. Quando si riceve il messaggio, è possibile inviare i dati al dispositivo ricevente.
8.  Quando si riceve un messaggio WMT TRANSCRYPTOR READ con il parametro hr impostato su \_ \_ NS S  \_ \_ TRANSCRYPTOR EOF, \_ l'intero file è stato letto. A questo punto, chiamare il [**metodo IWMDRMTranscryptor::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) per chiudere il file e liberare risorse.
9.  Quando viene ricevuto il messaggio WMT \_ TRANSCRYPTOR \_ CLOSED, è possibile rilasciare [**l'interfaccia IWMDRMTranscryptor.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor)

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del Windows DRM 10 per dispositivi di rete**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




