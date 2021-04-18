---
description: Sblocco di Windows Media Format SDK
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Sblocco di Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320722"
---
# <a name="unlocking-the-windows-media-format-sdk"></a><span data-ttu-id="daeed-103">Sblocco di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="daeed-103">Unlocking the Windows Media Format SDK</span></span>

<span data-ttu-id="daeed-104">Per accedere alla versione 7 o 7,1 di Windows Media Format SDK, un'applicazione deve fornire un certificato software, detto anche chiave, in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="daeed-104">To access version 7 or 7.1 of the Windows Media Format SDK, an application must provide a software certificate, also called a key, at run time.</span></span> <span data-ttu-id="daeed-105">Questa chiave è contenuta in una libreria statica denominata wmstub. lib a cui si collega l'applicazione in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="daeed-105">This key is contained in a static library called wmstub.lib to which the application links at build time.</span></span> <span data-ttu-id="daeed-106">Una chiave individualizzata è necessaria solo per la creazione o la lettura di file protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="daeed-106">An individualized key is only required for creating or reading DRM-protected files.</span></span> <span data-ttu-id="daeed-107">È possibile creare file non DRM usando la libreria statica fornita con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="daeed-107">Non-DRM files can be created using the static library provided with the Windows Media Format SDK.</span></span> <span data-ttu-id="daeed-108">Per informazioni dettagliate su come ottenere la chiave DRM, vedere Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="daeed-108">For details on obtaining the DRM key, see the Windows Media Format SDK.</span></span> <span data-ttu-id="daeed-109">Un'applicazione DirectShow fornisce il certificato al writer ASF WM quando viene aggiunto al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="daeed-109">A DirectShow application provides its certificate to the WM ASF Writer when it is added to the filter graph.</span></span> <span data-ttu-id="daeed-110">L'applicazione deve essere registrata come provider chiave utilizzando le interfacce COM **IServiceProvider** e **IObjectWithSite** .</span><span class="sxs-lookup"><span data-stu-id="daeed-110">The application must register as a key provider using the COM **IServiceProvider** and **IObjectWithSite** interfaces.</span></span> <span data-ttu-id="daeed-111">Utilizzando questa tecnica, l'applicazione implementa una classe del provider di chiavi derivata da **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="daeed-111">Using this technique, the application implements a key provider class derived from **IServiceProvider**.</span></span> <span data-ttu-id="daeed-112">Questa classe implementa i tre metodi COM standard,**AddRef**, **QueryInterface** e **Release**, insieme a un altro metodo, **QueryService**, che viene chiamato da Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="daeed-112">This class implements the three standard COM methods—**AddRef**, **QueryInterface**, and **Release**—along with one additional method, **QueryService**, which is called by the filter graph manager.</span></span> <span data-ttu-id="daeed-113">**QueryService** chiama il metodo SDK di Windows Media Format [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) e torna al gestore del grafico del filtro un puntatore al certificato creato.</span><span class="sxs-lookup"><span data-stu-id="daeed-113">**QueryService** calls the Windows Media Format SDK method [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) and returns to the filter graph manager a pointer to the certificate that was created.</span></span> <span data-ttu-id="daeed-114">Se il certificato è valido, il gestore del grafico dei filtri consente di continuare il processo di compilazione del grafico.</span><span class="sxs-lookup"><span data-stu-id="daeed-114">If the certificate is valid, the filter graph manager allows the graph-building process to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="daeed-115">Per compilare un'applicazione, includere Wmsdkidl. h per il prototipo per [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))e collegarsi alla libreria Wmstub. lib.</span><span class="sxs-lookup"><span data-stu-id="daeed-115">To build an application, include Wmsdkidl.h for the prototype for [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)), and link to the Wmstub.lib library.</span></span>

 

<span data-ttu-id="daeed-116">Nell'esempio di codice riportato di seguito vengono illustrati i passaggi di base di questo processo:</span><span class="sxs-lookup"><span data-stu-id="daeed-116">The following code example illustrates the basic steps in this process:</span></span>


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a><span data-ttu-id="daeed-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daeed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daeed-118">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="daeed-118">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
