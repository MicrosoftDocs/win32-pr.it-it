---
description: A Windows Vista, viene fatto un uso maggiore delle immagini di anteprima specifiche del file rispetto alle versioni precedenti di Windows.
title: Creazione di gestori di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4923c01b0387069a8d50ae4d293c40db496f126fdb40ca37d1309dc0201cd51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050858"
---
# <a name="building-thumbnail-handlers"></a>Creazione di gestori di anteprime

A Windows Vista, viene fatto un uso maggiore delle immagini di anteprima specifiche del file rispetto alle versioni precedenti di Windows. Vengono usati in tutte le visualizzazioni, nei dialoghe e per qualsiasi tipo di file che le fornisce. È stata modificata anche la visualizzazione dell'anteprima. È disponibile una gamma continua di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio icone e anteprime.

[**L'interfaccia IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) rende più semplice fornire un'anteprima rispetto a [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) o [**IExtractImage2 meno recente.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2) Si noti, tuttavia, che il codice esistente che usa **IExtractImage** o **IExtractImage2** è ancora valido e supportato.

## <a name="the-recipethumbnailprovider-sample"></a>Esempio recipeThumbnailProvider

[L'esempio RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustrato in questa sezione è incluso in Windows Software Development Kit (SDK). Il percorso di installazione predefinito è C: \\ Programmi Microsoft SDK Windows \\ \\ \\ v6.0 \\ Samples \\ WinUI Shell \\ \\ AppShellIntegration \\ RecipeThumbnailProvider. Tuttavia, anche la maggior parte del codice è inclusa qui.

[L'esempio RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustra l'implementazione di un gestore di anteprime per un nuovo tipo di file registrato con estensione recipe. L'esempio illustra l'uso delle diverse API del gestore di anteprime per registrare i server COM (Thumbnail Extraction Component Object Model) per tipi di file personalizzati. Questo argomento illustra il codice di esempio, evidenziando le scelte e le linee guida per la scrittura del codice.

Un gestore di anteprime deve implementare [**sempre IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) insieme a una di queste interfacce:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

In alcuni casi l'inizializzazione con i flussi non è possibile. Negli scenari in cui il gestore di anteprime non implementa [**IInitializeWithStream,**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)deve rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo inserisce per impostazione predefinita quando viene apportata una modifica al flusso. Per rifiutare esplicitamente la funzionalità di isolamento del processo, impostare il valore del Registro di sistema seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Se si implementa [**IInitializeWithStream e si**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) esegue un'inizializzazione basata su flusso, il gestore è più sicuro e affidabile. In genere, la disabilitazione dell'isolamento dei processi è destinata solo ai gestori legacy. evitare di disabilitare questa funzionalità per qualsiasi nuovo codice. **IInitializeWithStream deve essere la** prima scelta dell'interfaccia di inizializzazione quando possibile.

Poiché il file di immagine nell'esempio non è incorporato nel file con estensione recipe e non fa parte del flusso di file, nell'esempio viene usato [**IInitializeWithItem.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) L'implementazione [**del metodo IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) passa semplicemente i parametri alle variabili di classe private.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) ha un solo metodo,[**GetThumbnail,**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)che viene chiamato con le dimensioni desiderate più grandi dell'immagine, in pixel. Anche se il parametro è *denominato cx*, il relativo valore viene usato come dimensione massima delle dimensioni x e y dell'immagine. Se l'anteprima recuperata non è quadrata, l'asse più lungo è limitato da *cx* e le proporzioni dell'immagine originale vengono mantenute.

Quando viene restituito, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornisce un handle per l'immagine recuperata. Fornisce anche un valore che indica il formato del colore dell'immagine e se contiene informazioni alfa valide.

L'implementazione di GetThumbnail nell'esempio inizia con una chiamata al metodo **\_ GetBase64EncodedImageString** privato.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



Il tipo di file con estensione recipe è semplicemente un file XML registrato come estensione di file univoca. Include un elemento denominato **Picture** che fornisce il percorso relativo e il nome file dell'immagine da usare come anteprima per questo particolare file con estensione recipe. **L'elemento Picture** è costituito **dall'attributo Source** che specifica un'immagine codificata in base 64 e da un attributo **Size** facoltativo.

**Size** ha due valori, Small e Large. In questo modo è possibile fornire più **nodi Immagine** con immagini separate. L'immagine recuperata dipende quindi dal valore delle dimensioni massime (*cx*) fornito nella chiamata a [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Poiché Windows dimensioni dell'immagine non superano mai le dimensioni massime, è possibile specificare immagini diverse per risoluzioni diverse. Tuttavia, per semplicità, l'esempio omette **l'attributo Size** e fornisce una sola immagine per tutte le situazioni.

Il **\_ metodo GetBase64EncodedImageString,** la cui implementazione è illustrata qui, usa LE API DOM (XML Document Object Model) per recuperare il **nodo** Picture. Da tale nodo estrae l'immagine dai dati **dell'attributo** Source.


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



[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) passa quindi la stringa recuperata a **\_ GetStreamFromString**.


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



Il **\_ metodo GetStreamFromString,** la cui implementazione è illustrata qui, che converte l'immagine codificata in un flusso.


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



**GetThumbnail** usa quindi le API WIC (Windows Imaging Component) per estrarre una bitmap dal flusso e ottenere un handle per tale bitmap. Le informazioni alfa vengono impostate, wic viene chiuso correttamente e il metodo termina correttamente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprime](thumbnail-providers.md)
</dt> <dt>

[Linee guida per il gestore di anteprime](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV \_ ARGS**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
