---
description: A partire da Windows Vista, un uso più ampio è costituito da immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows.
title: Compilazione di gestori di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977391"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="dc85f-103">Compilazione di gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="dc85f-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="dc85f-104">A partire da Windows Vista, un uso più ampio è costituito da immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc85f-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="dc85f-105">Vengono usati in tutte le visualizzazioni, nelle finestre di dialogo e per qualsiasi tipo di file che li fornisce.</span><span class="sxs-lookup"><span data-stu-id="dc85f-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="dc85f-106">È stata modificata anche la visualizzazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="dc85f-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="dc85f-107">È disponibile una gamma continua di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio icone e anteprime.</span><span class="sxs-lookup"><span data-stu-id="dc85f-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="dc85f-108">L'interfaccia [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) rende più semplice la creazione di un'anteprima rispetto alla precedente [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span><span class="sxs-lookup"><span data-stu-id="dc85f-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="dc85f-109">Si noti, tuttavia, che il codice esistente che usa **IExtractImage** o **IExtractImage2** è ancora valido e supportato.</span><span class="sxs-lookup"><span data-stu-id="dc85f-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="dc85f-110">Esempio RecipeThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="dc85f-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="dc85f-111">Il campione [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sezionato in questa sezione è incluso in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="dc85f-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dc85f-112">Il percorso di installazione predefinito è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider.</span><span class="sxs-lookup"><span data-stu-id="dc85f-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="dc85f-113">Tuttavia, la maggior parte del codice è inclusa anche qui.</span><span class="sxs-lookup"><span data-stu-id="dc85f-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="dc85f-114">L'esempio [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustra l'implementazione di un gestore di anteprime per un nuovo tipo di file registrato con l'estensione recipe.</span><span class="sxs-lookup"><span data-stu-id="dc85f-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="dc85f-115">Nell'esempio viene illustrato l'utilizzo delle diverse API del gestore di anteprime per registrare i server COM (thumbnail Extraction Component Object Model) per i tipi di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="dc85f-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="dc85f-116">In questo argomento viene illustrato il codice di esempio, in cui sono evidenziate le opzioni e le linee guida di codifica.</span><span class="sxs-lookup"><span data-stu-id="dc85f-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="dc85f-117">Un gestore di anteprime deve sempre implementare [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concerto con una di queste interfacce:</span><span class="sxs-lookup"><span data-stu-id="dc85f-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="dc85f-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="dc85f-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="dc85f-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="dc85f-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="dc85f-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="dc85f-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="dc85f-121">In alcuni casi non è possibile inizializzare con i flussi.</span><span class="sxs-lookup"><span data-stu-id="dc85f-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="dc85f-122">Negli scenari in cui il gestore di anteprime non implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), è necessario rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo inserisce per impostazione predefinita quando viene apportata una modifica al flusso.</span><span class="sxs-lookup"><span data-stu-id="dc85f-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="dc85f-123">Per rifiutare esplicitamente la funzionalità di isolamento dei processi, impostare il valore del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="dc85f-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="dc85f-124">Se si implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) e si esegue un'inizializzazione basata sul flusso, il gestore è più sicuro e affidabile.</span><span class="sxs-lookup"><span data-stu-id="dc85f-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="dc85f-125">In genere, la disabilitazione dell'isolamento dei processi è destinata solo ai gestori legacy; evitare di disabilitare questa funzionalità per qualsiasi nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="dc85f-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="dc85f-126">Quando possibile, **IInitializeWithStream** deve essere la prima scelta dell'interfaccia di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="dc85f-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="dc85f-127">Poiché il file di immagine nell'esempio non è incorporato nel file con estensione Recipe e non fa parte del relativo flusso di file, nell'esempio viene utilizzato [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) .</span><span class="sxs-lookup"><span data-stu-id="dc85f-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="dc85f-128">L'implementazione del metodo [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) passa semplicemente i parametri alle variabili della classe privata.</span><span class="sxs-lookup"><span data-stu-id="dc85f-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="dc85f-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) dispone di un solo metodo, ovvero [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), che viene chiamato con le dimensioni massime desiderate dell'immagine, in pixel.</span><span class="sxs-lookup"><span data-stu-id="dc85f-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="dc85f-130">Anche se il parametro è denominato *CX*, il relativo valore viene usato come dimensione massima delle dimensioni x e y dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dc85f-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="dc85f-131">Se l'anteprima recuperata non è quadrata, l'asse più lungo è limitato da *CX* e le proporzioni dell'immagine originale vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="dc85f-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="dc85f-132">Quando restituisce, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornisce un handle per l'immagine recuperata.</span><span class="sxs-lookup"><span data-stu-id="dc85f-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="dc85f-133">Fornisce inoltre un valore che indica il formato di colore dell'immagine e se dispone di informazioni Alpha valide.</span><span class="sxs-lookup"><span data-stu-id="dc85f-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="dc85f-134">L'implementazione di GetThumbnail nell'esempio inizia con una chiamata al metodo **\_ GetBase64EncodedImageString** privato.</span><span class="sxs-lookup"><span data-stu-id="dc85f-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="dc85f-135">Il tipo di file Recipe è semplicemente un file XML registrato come estensione del nome file univoco.</span><span class="sxs-lookup"><span data-stu-id="dc85f-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="dc85f-136">Include un elemento denominato **Picture** che fornisce il percorso relativo e il nome file dell'immagine da usare come anteprima per il file. Recipe specifico.</span><span class="sxs-lookup"><span data-stu-id="dc85f-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="dc85f-137">L'elemento **Picture** è costituito dall'attributo **source** che specifica un'immagine con codifica base 64 e da un attributo di **dimensione** facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dc85f-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="dc85f-138">**Size** ha due valori, Small e large.</span><span class="sxs-lookup"><span data-stu-id="dc85f-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="dc85f-139">In questo modo è possibile fornire più nodi **immagine** con immagini separate.</span><span class="sxs-lookup"><span data-stu-id="dc85f-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="dc85f-140">L'immagine recuperata dipende quindi dal valore di dimensione massima (*CX*) fornito nella chiamata a [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span><span class="sxs-lookup"><span data-stu-id="dc85f-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="dc85f-141">Poiché Windows non ridimensiona mai l'immagine con dimensioni maggiori di quelle massime, è possibile fornire diverse immagini per risoluzioni diverse.</span><span class="sxs-lookup"><span data-stu-id="dc85f-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="dc85f-142">Per semplicità, tuttavia, l'esempio omette l'attributo **size** e fornisce solo un'immagine per tutte le situazioni.</span><span class="sxs-lookup"><span data-stu-id="dc85f-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="dc85f-143">Il metodo **\_ GetBase64EncodedImageString** , la cui implementazione è illustrata di seguito, USA le API XML Document Object Model (Dom) per recuperare il nodo **immagine** .</span><span class="sxs-lookup"><span data-stu-id="dc85f-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="dc85f-144">Da tale nodo estrae l'immagine dai dati dell'attributo di **origine** .</span><span class="sxs-lookup"><span data-stu-id="dc85f-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="dc85f-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) passa quindi la stringa recuperata a **\_ GetStreamFromString**.</span><span class="sxs-lookup"><span data-stu-id="dc85f-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="dc85f-146">Il metodo **\_ GetStreamFromString** , la cui implementazione è illustrata di seguito, che converte l'immagine codificata in un flusso.</span><span class="sxs-lookup"><span data-stu-id="dc85f-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="dc85f-147">**GetThumbnail** usa quindi le API di Windows Imaging Component (WIC) per estrarre una bitmap dal flusso e ottenere un handle per tale bitmap.</span><span class="sxs-lookup"><span data-stu-id="dc85f-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="dc85f-148">Le informazioni alfa sono impostate, l'oggetto WIC è stato chiuso correttamente e il metodo termina correttamente.</span><span class="sxs-lookup"><span data-stu-id="dc85f-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dc85f-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc85f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc85f-150">Gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="dc85f-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="dc85f-151">Linee guida per gestore anteprime</span><span class="sxs-lookup"><span data-stu-id="dc85f-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="dc85f-152">**argomenti di IID \_ PPV \_**</span><span class="sxs-lookup"><span data-stu-id="dc85f-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
