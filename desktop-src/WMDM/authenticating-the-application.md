---
title: Autenticazione dell'applicazione
description: Autenticazione dell'applicazione
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media Gestione dispositivi, autenticazione
- Gestione dispositivi, autenticazione
- Guida per programmatori, autenticazione
- applicazioni desktop, autenticazione
- creazione di applicazioni Windows Media Gestione dispositivi, autenticazione
- autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299891"
---
# <a name="authenticating-the-application"></a>Autenticazione dell'applicazione

Il primo passaggio che l'applicazione deve eseguire è l'autenticazione. L'autenticazione verifica l'identità dell'applicazione in Windows Media Gestione dispositivi. Una volta autenticata l'applicazione, è possibile chiamare **QueryInterface** per ottenere l'interfaccia [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) radice, che può essere sottoposta a query per altre interfacce obbligatorie, che possono essere sottoposte a query per tutte le altre interfacce. L'autenticazione deve essere eseguita solo una volta all'avvio.

Per autenticare l'applicazione, eseguire questi passaggi:

1.  Cocreare l'oggetto **MediaDevMgr** (ID classe MediaDevMgr) e richiedere un'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .
2.  Creare un oggetto [CSecureChannelClient](csecurechannelclient-class.md) per gestire l'autenticazione.
3.  Passare la chiave dell'applicazione e trasferire il certificato all'oggetto canale sicuro. È possibile usare la chiave o il certificato fittizio illustrato nel codice di esempio seguente per ottenere le funzionalità di base dalle funzioni SDK. Tuttavia, per ottenere la funzionalità completa (importante per il passaggio di file da e verso il dispositivo), è necessario richiedere una chiave e un certificato di Microsoft, come descritto in [strumenti per lo sviluppo](tools-for-development.md).
4.  Passare l'interfaccia **IComponentAuthenticate** creata nel passaggio 1 all'oggetto canale sicuro.
5.  Chiamare [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) per autenticare l'applicazione.
6.  Eseguire una query su **IComponentAuthenticate** per l'interfaccia **IWMDeviceManager** .

Questi passaggi sono illustrati nel codice C++ riportato di seguito.


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 