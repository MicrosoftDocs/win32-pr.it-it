---
description: Impostazione di una gestione credenziali
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Impostazione di una gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309000"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="e74ae-103">Impostazione di una gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="e74ae-103">Setting a Credential Manager</span></span>

<span data-ttu-id="e74ae-104">Un'applicazione che fornisce le credenziali per l'origine di rete deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e74ae-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="e74ae-105">Implementare un oggetto di gestione delle credenziali che espone l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="e74ae-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="e74ae-106">Prima di creare l'origine di rete, creare un nuovo archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e74ae-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="e74ae-107">Impostare la proprietà [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) nell'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e74ae-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="e74ae-108">Il valore della proprietà è un puntatore all'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="e74ae-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="e74ae-109">Passare un puntatore all'archivio delle proprietà al resolver di origine, come descritto in [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e74ae-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e74ae-110">Le origini di rete usano Gestione credenziali per ottenere le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="e74ae-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="e74ae-111">Se l'origine di rete richiede credenziali per accedere a una risorsa di rete, viene chiamato il metodo [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e74ae-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="e74ae-112">Questa chiamata avvia una richiesta asincrona per ottenere le credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e74ae-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="e74ae-113">Il metodo **BeginGetCredentials** può ottenere le credenziali dalla cache delle credenziali o dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e74ae-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="e74ae-114">Le credenziali vengono archiviate in un *oggetto credenziale*.</span><span class="sxs-lookup"><span data-stu-id="e74ae-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="e74ae-115">Al termine dell'operazione, l'applicazione richiama l'interfaccia di callback per notificare all'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="e74ae-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="e74ae-116">L'origine di rete chiama [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) per completare l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="e74ae-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="e74ae-117">Poiché si tratta di un'operazione asincrona, l'applicazione deve inviare il callback alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e74ae-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="e74ae-118">Per istruzioni dettagliate sulla scrittura di un metodo asincrono, vedere [scrittura di un metodo asincrono](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="e74ae-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="e74ae-119">Nell'esempio seguente viene illustrato come impostare la proprietà [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) nell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="e74ae-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e74ae-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e74ae-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74ae-121">Autenticazione origine rete</span><span class="sxs-lookup"><span data-stu-id="e74ae-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



