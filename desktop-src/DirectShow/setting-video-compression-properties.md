---
description: Impostazione delle proprietà di compressione video
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Impostazione delle proprietà di compressione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401235"
---
# <a name="setting-video-compression-properties"></a>Impostazione delle proprietà di compressione video

I filtri di compressione video possono supportare l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) nei pin di output. Usare questa interfaccia per impostare le proprietà di compressione, ad esempio la frequenza dei fotogrammi chiave, il numero di frame stimati (P) per fotogramma chiave e la qualità di compressione relativa.

Chiamare innanzitutto il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare il pin di output del filtro ed eseguire una query sul pin per l'interfaccia. Alcuni filtri potrebbero non supportare l'interfaccia. Altri possono esporre l'interfaccia ma non supportare ogni proprietà di compressione. Per determinare quali proprietà sono supportate, chiamare [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Questo metodo restituisce diverse informazioni:

-   Un set di flag di funzionalità
-   Stringa descrittiva e stringa di numero di versione
-   Valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità (se supportata)

Il metodo presenta la sintassi seguente:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



I parametri *pszVersion* e *pszDesc* sono buffer a caratteri wide che ricevono la stringa di versione e la stringa di descrizione. I parametri *cbVersion* e *cbDesc* ricevono le dimensioni del buffer richieste in byte (non caratteri). I parametri *lKeyFrame*, *lPFrame* e *dblQuality* ricevono i valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità. La qualità è espressa come numero a virgola mobile compreso tra 0,0 e 1,0. Il parametro *lCap* riceve **un operatore OR** bit per bit dei flag capabilities, definiti dal tipo enumerato [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .

Uno di questi parametri può essere **null**, nel qual caso il metodo ignora il parametro. Per allocare i buffer per le stringhe di versione e descrizione, ad esempio, chiamare prima il metodo con **null** nel primo e nel terzo parametro. Usare i valori restituiti per *cbVersion* e *cbDesc* per allocare i buffer e quindi chiamare di nuovo il metodo:


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



Il valore di *lCap* indica gli altri metodi **IAMVideoCompression** supportati dal filtro. Se, ad esempio, *lCap* contiene il \_ flag CompressionCaps CanKeyFrame, è possibile chiamare [**IAMVideoCompression:: Get \_ framerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) per ottenere la frequenza dei fotogrammi chiave e [**IAMVideoCompression::p la frequenza dei \_ fotogrammi**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) chiave per impostare la frequenza del fotogramma chiave. Un valore negativo indica che il filtro utilizzerà il valore predefinito, come ottenuto da [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Ad esempio:


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



L'esempio di codice seguente tenta di trovare l'interfaccia **IAMVideoCompression** sul pin di output. Se ha esito positivo, recupera i valori predefiniti e effettivi per le proprietà di compressione:


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Se si usa l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) per compilare il grafo, è possibile ottenere l'interfaccia **IAMVideoCompression** chiamando [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), invece di usare **IBaseFilter:: EnumPins**. Il metodo **FindInterface** è un metodo helper che cerca filtri e pin nel grafico per un'interfaccia specificata.

 

 

 



