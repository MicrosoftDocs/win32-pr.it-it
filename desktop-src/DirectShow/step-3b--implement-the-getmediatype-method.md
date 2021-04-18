---
description: Passaggio 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Passaggio 3B. Implementare il metodo GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530499"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Passaggio 3B. Implementare il metodo GetMediaType

Questo è il passaggio 3B dell'esercitazione sulla [scrittura dei filtri di trasformazione](writing-transform-filters.md).

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.

 

Il metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) restituisce uno dei tipi di output preferiti del filtro, a cui fa riferimento il numero di indice. Questo metodo non viene mai chiamato a meno che il pin di input del filtro non sia già connesso. Pertanto, è possibile utilizzare il tipo di supporto della connessione upstream per determinare i tipi di output preferiti.

Un codificatore offre in genere un singolo tipo preferito, che rappresenta il formato di destinazione. I decodificatori in genere supportano una gamma di formati di output e li offrono in ordine di qualità o efficienza decrescente. Ad esempio, l'elenco potrebbe essere UYVY, Y211, RGB-24, RGB-565, RGB-555 e RGB-8, in questo ordine. I filtri effetti possono richiedere una corrispondenza esatta tra il formato di output e il formato di input.

Nell'esempio seguente viene restituito un singolo tipo di output, che viene costruito modificando il tipo di input per specificare la compressione RLE8:


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



In questo esempio, il metodo chiama [**Ipin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) per ottenere il tipo di input dal pin di input. Modifica quindi alcuni campi per indicare il formato di compressione, come indicato di seguito:

-   Assegna un nuovo GUID del sottotipo, costruito dal codice FOURCC ' MRLE ', usando la classe [**FOURCCMap**](fourccmap.md) .
-   Chiama il metodo [**CMediaType:: SetVariableSize**](cmediatype-setvariablesize.md) , che imposta il flag **bFixedSizeSamples** su **false** e il membro **lSampleSize** su zero, indicando esempi di dimensioni variabili.
-   Chiama il metodo [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) con il valore **false**, a indicare che ogni frame è un fotogramma chiave. (Questo campo è solo informativo, pertanto è possibile ignorarlo in modo sicuro).
-   Imposta il campo **biCompression** su bi \_ RLE8.
-   Imposta il campo **biSizeImage** sulla dimensione dell'immagine.

[Passaggio 3c: implementare il metodo CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



