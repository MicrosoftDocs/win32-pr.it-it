---
description: Passaggio 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Passaggio 3B. Implementare il metodo GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386c16e3166f910e8221d139af519363d1b49279a412603e0cfddfa41773ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583111"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Passaggio 3B. Implementare il metodo GetMediaType

Questo è il passaggio 3B dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter.**

 

Il [**metodo CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) restituisce uno dei tipi di output preferiti del filtro, a cui fa riferimento il numero di indice. Questo metodo non viene mai chiamato a meno che il pin di input del filtro non sia già connesso. Pertanto, è possibile usare il tipo di supporto della connessione upstream per determinare i tipi di output preferiti.

Un codificatore offre in genere un singolo tipo preferito, che rappresenta il formato di destinazione. I decodificatori supportano in genere una gamma di formati di output e li offrono in ordine decrescente di qualità o efficienza. Ad esempio, l'elenco potrebbe essere UYVY, Y211, RGB-24, RGB-565, RGB-555 e RGB-8, in questo ordine. I filtri degli effetti possono richiedere una corrispondenza esatta tra il formato di output e il formato di input.

L'esempio seguente restituisce un singolo tipo di output, costruito modificando il tipo di input per specificare la compressione RLE8:


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



In questo esempio il metodo chiama [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) per ottenere il tipo di input dal pin di input. Modifica quindi alcuni campi per indicare il formato di compressione, come indicato di seguito:

-   Assegna un nuovo GUID del sottotipo, costruito dal codice FOURCC 'MRLE', usando la [**classe FOURCCMap.**](fourccmap.md)
-   Chiama il metodo [**CMediaType::SetVariableSize,**](cmediatype-setvariablesize.md) che imposta il flag **bFixedSizeSamples** su **FALSE** e il membro **lSampleSize** su zero, indicando esempi di dimensioni variabili.
-   Chiama il [**metodo CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) con il valore **FALSE,** a indicare che ogni fotogramma è un fotogramma chiave. Questo campo è solo informativo, quindi è possibile ignorarlo.
-   Imposta il **campo biCompression** su BI \_ RLE8.
-   Imposta il campo **biSizeImage** sulla dimensione dell'immagine.

Passaggio [3C. Implementare il metodo CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



