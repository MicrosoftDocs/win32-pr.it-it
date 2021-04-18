---
description: Passaggio 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Passaggio 3A. Implementare il metodo CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316327"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Passaggio 3A. Implementare il metodo CheckInputType

Questo è il passaggio 3A dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

Il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) viene chiamato quando il filtro upstream propone un tipo di supporto al filtro di trasformazione. Questo metodo accetta un puntatore a un oggetto [**CMediaType**](cmediatype.md) , che è un wrapper sottile per la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . In questo metodo, è necessario esaminare ogni campo pertinente della struttura del **\_ \_ tipo di supporto am** , inclusi i campi nel blocco di formato. È possibile usare i metodi della funzione di accesso definiti in **CMediaType** o fare riferimento direttamente ai membri della struttura. Se un campo non è valido, restituire il \_ tipo VFW E \_ \_ non \_ accettato. Se l'intero tipo di supporto è valido, restituire S \_ OK.

Nel filtro del codificatore RLE, ad esempio, il tipo di input deve essere un video RGB non compresso a 8 bit o a 4 bit. Non esiste alcun motivo per supportare altri formati di input, ad esempio a 16 o a 24 bit RGB, perché il filtro avrebbe dovuto convertirli in una profondità di bit inferiore e DirectShow fornisce già un filtro del [convertitore dello spazio dei colori](color-space-converter-filter.md) a tale scopo. Nell'esempio seguente si presuppone che il codificatore supporti video a 8 bit, ma non video a 4 bit:


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



In questo esempio, il metodo controlla prima di tutto il tipo principale e il sottotipo. Quindi controlla il tipo di formato, per assicurarsi che il blocco di formato sia una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Il filtro può inoltre supportare [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), ma in questo caso non esiste alcun vantaggio reale. La struttura **VIDEOINFOHEADER2** aggiunge il supporto per l'interlacciamento e i pixel non quadrati, che probabilmente non saranno rilevanti nei video a 8 bit.

Se il tipo di formato è corretto, nell'esempio vengono controllati i membri **biBitCount** e **biCompression** della struttura **VIDEOINFOHEADER** per verificare che il formato sia RGB non compresso a 8 bit. Come illustrato in questo esempio, è necessario forzare il


```C++
pbFormat
```



puntatore alla struttura corretta, in base al tipo di formato. Controllare sempre il tipo di formato GUID (**formatType**) e le dimensioni del blocco di formato (**cbFormat**) prima di eseguire il cast del puntatore.

Nell'esempio viene inoltre verificato che il numero di voci della tavolozza è compatibile con la profondità del bit e il blocco di formato è sufficientemente grande da poter essere utilizzato per le voci della tavolozza. Se tutte le informazioni sono corrette, il metodo restituisce S \_ OK.

[Passaggio 3b. implementare il metodo GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



