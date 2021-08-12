---
title: Autenticazione del provider di servizi
description: Autenticazione del provider di servizi
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Gestione dispositivi multimediali, autenticazione
- Gestione dispositivi, autenticazione
- guida per programmatori,autenticazione
- provider di servizi, autenticazione
- creazione di provider di servizi, autenticazione
- autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d6931acb4644d4222659d428be10877deb164a184c95609663a915c12b95d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586487"
---
# <a name="authenticating-the-service-provider"></a>Autenticazione del provider di servizi

Per essere accessibile da Windows Gestione dispositivi multimediali, un provider di servizi deve ereditare e implementare [**l'interfaccia IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)

Per autenticarsi, un provider di servizi esegue la procedura seguente:

1.  Durante la creazione di un'istanza, crea un nuovo oggetto [CSecureChannelServer globale](csecurechannelserver-class.md) e imposta i valori del certificato e della chiave dal relativo file di chiave.
2.  Implementa i metodi [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) e [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) passando semplicemente i parametri al relativo membro CSecureChannelServer globale.
3.  Prima di gestire i metodi di Windows Gestione dispositivi multimediali implementati, il provider di servizi deve verificare l'autenticazione del chiamante chiamando CSecureChannelServer::fIsAuthenticated e ha esito negativo se il chiamante non è autenticato.

Questi passaggi sono illustrati negli esempi C++ seguenti.

**Creazione dell'oggetto CSecureChannelServer**


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



**Implementazione dei metodi IComponentAuthenticate**


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



**Verifica dell'autenticazione del chiamante**

Nell'esempio di codice seguente viene illustrato un provider di servizi che controlla l'autenticazione del chiamante come parte dell'implementazione **dell'interfaccia IMDServiceProvider.**


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




