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
# <a name="authenticating-the-application"></a><span data-ttu-id="9eda6-109">Autenticazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9eda6-109">Authenticating the Application</span></span>

<span data-ttu-id="9eda6-110">Il primo passaggio che l'applicazione deve eseguire è l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9eda6-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="9eda6-111">L'autenticazione verifica l'identità dell'applicazione in Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9eda6-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="9eda6-112">Una volta autenticata l'applicazione, è possibile chiamare **QueryInterface** per ottenere l'interfaccia [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) radice, che può essere sottoposta a query per altre interfacce obbligatorie, che possono essere sottoposte a query per tutte le altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="9eda6-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="9eda6-113">L'autenticazione deve essere eseguita solo una volta all'avvio.</span><span class="sxs-lookup"><span data-stu-id="9eda6-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="9eda6-114">Per autenticare l'applicazione, eseguire questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="9eda6-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="9eda6-115">Cocreare l'oggetto **MediaDevMgr** (ID classe MediaDevMgr) e richiedere un'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="9eda6-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="9eda6-116">Creare un oggetto [CSecureChannelClient](csecurechannelclient-class.md) per gestire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9eda6-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="9eda6-117">Passare la chiave dell'applicazione e trasferire il certificato all'oggetto canale sicuro.</span><span class="sxs-lookup"><span data-stu-id="9eda6-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="9eda6-118">È possibile usare la chiave o il certificato fittizio illustrato nel codice di esempio seguente per ottenere le funzionalità di base dalle funzioni SDK.</span><span class="sxs-lookup"><span data-stu-id="9eda6-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="9eda6-119">Tuttavia, per ottenere la funzionalità completa (importante per il passaggio di file da e verso il dispositivo), è necessario richiedere una chiave e un certificato di Microsoft, come descritto in [strumenti per lo sviluppo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="9eda6-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="9eda6-120">Passare l'interfaccia **IComponentAuthenticate** creata nel passaggio 1 all'oggetto canale sicuro.</span><span class="sxs-lookup"><span data-stu-id="9eda6-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="9eda6-121">Chiamare [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) per autenticare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9eda6-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="9eda6-122">Eseguire una query su **IComponentAuthenticate** per l'interfaccia **IWMDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="9eda6-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="9eda6-123">Questi passaggi sono illustrati nel codice C++ riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="9eda6-123">These steps are shown in the following C++ code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9eda6-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eda6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eda6-125">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="9eda6-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 