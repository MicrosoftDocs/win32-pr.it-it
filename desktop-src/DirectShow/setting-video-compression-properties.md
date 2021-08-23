---
description: Impostazione delle proprietà di compressione video
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Impostazione delle proprietà di compressione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583281"
---
# <a name="setting-video-compression-properties"></a>Impostazione delle proprietà di compressione video

I filtri di compressione video possono supportare [**l'interfaccia IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) sui pin di output. Usare questa interfaccia per impostare le proprietà di compressione, ad esempio la frequenza dei fotogrammi chiave, il numero di fotogrammi stimati (P) per ogni fotogramma chiave e la qualità di compressione relativa.

Chiamare prima di tutto [**il metodo IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare il pin di output del filtro ed eseguire una query sul pin per l'interfaccia. Alcuni filtri potrebbero non supportare affatto l'interfaccia . Altri possono esporre l'interfaccia ma non supportano tutte le proprietà di compressione. Per determinare le proprietà supportate, chiamare [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Questo metodo restituisce diverse informazioni:

-   Un set di flag di funzionalità
-   Stringa descrittiva e stringa del numero di versione
-   Valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità (se supportati)

Il metodo ha la sintassi seguente:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



I *parametri pszVersion* e *pszDesc* sono buffer di caratteri wide che ricevono la stringa di versione e la stringa di descrizione. I *parametri cbVersion* *e cbDesc* ricevono le dimensioni del buffer richieste in byte (non i caratteri). I *parametri lKeyFrame*, *lPFrame* e *dblQuality* ricevono i valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità. La qualità è espressa come numero a virgola mobile da 0,0 a 1,0. Il *parametro lCap* riceve un **OR** bit per bit dei flag di funzionalità, definiti dal tipo enumerato [**CompressionCaps.**](/windows/desktop/api/strmif/ne-strmif-compressioncaps)

Uno di questi parametri può essere **NULL,** nel qual caso il metodo ignora tale parametro. Ad esempio, per allocare buffer per le stringhe di versione e descrizione, chiamare prima il metodo con **NULL** nel primo e nel terzo parametro. Usare i valori restituiti *per cbVersion* *e cbDesc* per allocare i buffer e quindi chiamare nuovamente il metodo :


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



Il valore *di lCap* indica quale degli altri metodi **IAMVideoCompression** supportati dal filtro. Ad esempio, se *lCap* contiene il flag CompressionCaps CanKeyFrame, è possibile chiamare \_ [**IAMVideoCompression::get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) per ottenere la frequenza dei fotogrammi chiave e [**IAMVideoCompression::p ut \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) per impostare la frequenza dei fotogrammi chiave. Un valore negativo indica che il filtro userà il valore predefinito, ottenuto da [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Esempio:


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



L'esempio di codice seguente tenta di trovare **l'interfaccia IAMVideoCompression** sul pin di output. Se ha esito positivo, recupera i valori predefiniti ed effettivi per le proprietà di compressione:


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
> Se si usa [**l'interfaccia ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) per compilare il grafico, è possibile ottenere l'interfaccia **IAMVideoCompression** chiamando [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)invece di usare **IBaseFilter::EnumPins**. Il **metodo FindInterface** è un metodo helper che cerca filtri e segnaposto nel grafico per un'interfaccia specificata.

 

 

 



