---
title: Autenticazione del provider di servizi
description: Autenticazione del provider di servizi
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media Gestione dispositivi, autenticazione
- Gestione dispositivi, autenticazione
- Guida per programmatori, autenticazione
- provider di servizi, autenticazione
- creazione di provider di servizi, autenticazione
- autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298617"
---
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="4bf6d-109">Autenticazione del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="4bf6d-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="4bf6d-110">Per essere accessibile da Windows Media Gestione dispositivi, un provider di servizi deve ereditare e implementare l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="4bf6d-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="4bf6d-111">Per autenticarsi, un provider di servizi esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4bf6d-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="4bf6d-112">Quando si crea un'istanza, viene creato un nuovo oggetto [CSecureChannelServer](csecurechannelserver-class.md) globale e vengono impostati i valori del certificato e della chiave dal relativo file di chiave.</span><span class="sxs-lookup"><span data-stu-id="4bf6d-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="4bf6d-113">Implementa i metodi [**IComponentAuthenticate:: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) e [**IComponentAuthenticate:: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) passando semplicemente i parametri al relativo membro CSecureChannelServer globale.</span><span class="sxs-lookup"><span data-stu-id="4bf6d-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="4bf6d-114">Prima di gestire qualsiasi metodo di Windows Media Gestione dispositivi implementato, il provider di servizi deve verificare l'autenticazione del chiamante chiamando CSecureChannelServer:: fIsAuthenticated e non riesce se il chiamante non è autenticato.</span><span class="sxs-lookup"><span data-stu-id="4bf6d-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="4bf6d-115">Questi passaggi sono illustrati negli esempi seguenti di C++.</span><span class="sxs-lookup"><span data-stu-id="4bf6d-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="4bf6d-116">**Creazione dell'oggetto CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="4bf6d-116">**Creating the CSecureChannelServer object**</span></span>


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



<span data-ttu-id="4bf6d-117">**Implementazione dei metodi IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="4bf6d-117">**Implementing the IComponentAuthenticate methods**</span></span>


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



<span data-ttu-id="4bf6d-118">**Verifica dell'autenticazione del chiamante**</span><span class="sxs-lookup"><span data-stu-id="4bf6d-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="4bf6d-119">Nell'esempio di codice seguente viene illustrato un provider di servizi che controlla l'autenticazione del chiamante come parte dell'implementazione dell'interfaccia **IMDServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="4bf6d-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4bf6d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bf6d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf6d-121">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="4bf6d-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




