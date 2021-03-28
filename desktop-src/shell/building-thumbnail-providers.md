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
# <a name="building-thumbnail-handlers"></a>Compilazione di gestori di anteprime

A partire da Windows Vista, un uso più ampio è costituito da immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows. Vengono usati in tutte le visualizzazioni, nelle finestre di dialogo e per qualsiasi tipo di file che li fornisce. È stata modificata anche la visualizzazione delle anteprime. È disponibile una gamma continua di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio icone e anteprime.

L'interfaccia [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) rende più semplice la creazione di un'anteprima rispetto alla precedente [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2). Si noti, tuttavia, che il codice esistente che usa **IExtractImage** o **IExtractImage2** è ancora valido e supportato.

## <a name="the-recipethumbnailprovider-sample"></a>Esempio RecipeThumbnailProvider

Il campione [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sezionato in questa sezione è incluso in Windows Software Development Kit (SDK). Il percorso di installazione predefinito è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider. Tuttavia, la maggior parte del codice è inclusa anche qui.

L'esempio [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustra l'implementazione di un gestore di anteprime per un nuovo tipo di file registrato con l'estensione recipe. Nell'esempio viene illustrato l'utilizzo delle diverse API del gestore di anteprime per registrare i server COM (thumbnail Extraction Component Object Model) per i tipi di file personalizzati. In questo argomento viene illustrato il codice di esempio, in cui sono evidenziate le opzioni e le linee guida di codifica.

Un gestore di anteprime deve sempre implementare [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concerto con una di queste interfacce:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

In alcuni casi non è possibile inizializzare con i flussi. Negli scenari in cui il gestore di anteprime non implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), è necessario rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo inserisce per impostazione predefinita quando viene apportata una modifica al flusso. Per rifiutare esplicitamente la funzionalità di isolamento dei processi, impostare il valore del registro di sistema seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Se si implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) e si esegue un'inizializzazione basata sul flusso, il gestore è più sicuro e affidabile. In genere, la disabilitazione dell'isolamento dei processi è destinata solo ai gestori legacy; evitare di disabilitare questa funzionalità per qualsiasi nuovo codice. Quando possibile, **IInitializeWithStream** deve essere la prima scelta dell'interfaccia di inizializzazione.

Poiché il file di immagine nell'esempio non è incorporato nel file con estensione Recipe e non fa parte del relativo flusso di file, nell'esempio viene utilizzato [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) . L'implementazione del metodo [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) passa semplicemente i parametri alle variabili della classe privata.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) dispone di un solo metodo, ovvero [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), che viene chiamato con le dimensioni massime desiderate dell'immagine, in pixel. Anche se il parametro è denominato *CX*, il relativo valore viene usato come dimensione massima delle dimensioni x e y dell'immagine. Se l'anteprima recuperata non è quadrata, l'asse più lungo è limitato da *CX* e le proporzioni dell'immagine originale vengono mantenute.

Quando restituisce, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornisce un handle per l'immagine recuperata. Fornisce inoltre un valore che indica il formato di colore dell'immagine e se dispone di informazioni Alpha valide.

L'implementazione di GetThumbnail nell'esempio inizia con una chiamata al metodo **\_ GetBase64EncodedImageString** privato.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



Il tipo di file Recipe è semplicemente un file XML registrato come estensione del nome file univoco. Include un elemento denominato **Picture** che fornisce il percorso relativo e il nome file dell'immagine da usare come anteprima per il file. Recipe specifico. L'elemento **Picture** è costituito dall'attributo **source** che specifica un'immagine con codifica base 64 e da un attributo di **dimensione** facoltativo.

**Size** ha due valori, Small e large. In questo modo è possibile fornire più nodi **immagine** con immagini separate. L'immagine recuperata dipende quindi dal valore di dimensione massima (*CX*) fornito nella chiamata a [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Poiché Windows non ridimensiona mai l'immagine con dimensioni maggiori di quelle massime, è possibile fornire diverse immagini per risoluzioni diverse. Per semplicità, tuttavia, l'esempio omette l'attributo **size** e fornisce solo un'immagine per tutte le situazioni.

Il metodo **\_ GetBase64EncodedImageString** , la cui implementazione è illustrata di seguito, USA le API XML Document Object Model (Dom) per recuperare il nodo **immagine** . Da tale nodo estrae l'immagine dai dati dell'attributo di **origine** .


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



Il metodo **\_ GetStreamFromString** , la cui implementazione è illustrata di seguito, che converte l'immagine codificata in un flusso.


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



**GetThumbnail** usa quindi le API di Windows Imaging Component (WIC) per estrarre una bitmap dal flusso e ottenere un handle per tale bitmap. Le informazioni alfa sono impostate, l'oggetto WIC è stato chiuso correttamente e il metodo termina correttamente.


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

[Linee guida per gestore anteprime](thumbnail-provider-guidelines.md)
</dt> <dt>

[**argomenti di IID \_ PPV \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
