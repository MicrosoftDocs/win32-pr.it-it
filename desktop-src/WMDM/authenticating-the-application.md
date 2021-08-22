---
title: Autenticazione dell'applicazione
description: Autenticazione dell'applicazione
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Gestione dispositivi multimediali, autenticazione
- Gestione dispositivi, autenticazione
- guida per programmatori,autenticazione
- applicazioni desktop, autenticazione
- creazione Windows applicazioni di Gestione dispositivi multimediali, autenticazione
- autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b67ad7c603bbfd3a56667bfcfe8742775c8ae5683888d72661e0a0974aa5358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586736"
---
# <a name="authenticating-the-application"></a>Autenticazione dell'applicazione

Il primo passaggio che l'applicazione deve eseguire è l'autenticazione. L'autenticazione verifica l'identità dell'applicazione Windows Gestione dispositivi multimediali. Dopo aver autenticato l'applicazione, è possibile chiamare **QueryInterface** per ottenere l'interfaccia [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) radice, su cui è possibile eseguire query per altre interfacce necessarie, su cui è possibile eseguire una query per tutte le altre interfacce. L'autenticazione deve avere luogo una sola volta all'avvio.

Per autenticare l'applicazione, seguire questa procedura:

1.  Creare **l'oggetto MediaDevMgr** (ID classe MediaDevMgr) e richiedere [**un'interfaccia IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
2.  Creare un [oggetto CSecureChannelClient](csecurechannelclient-class.md) per gestire l'autenticazione.
3.  Passare la chiave dell'applicazione e trasferire il certificato all'oggetto canale sicuro. È possibile usare la chiave/certificato fittizio illustrata nel codice di esempio seguente per ottenere funzionalità di base dalle funzioni dell'SDK. Tuttavia, per ottenere la funzionalità completa (importante per il passaggio di file da e verso il dispositivo), è necessario richiedere una chiave e un certificato a Microsoft come descritto in [Strumenti per lo sviluppo](tools-for-development.md).
4.  Passare **l'interfaccia IComponentAuthenticate** creata nel passaggio 1 all'oggetto canale sicuro.
5.  Chiamare [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) per autenticare l'applicazione.
6.  Eseguire una **query su IComponentAuthenticate** per **l'interfaccia IWMDeviceManager.**

Questi passaggi sono illustrati nel codice C++ seguente.


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

[**Creazione di un'Windows di Gestione dispositivi multimediali**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 