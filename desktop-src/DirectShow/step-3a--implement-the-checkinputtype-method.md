---
description: Passaggio 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Passaggio 3A. Implementare il metodo CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692175e0def453f86b618a355044e4a117a4343fed56f029704091134e8bc31f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652141"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Passaggio 3A. Implementare il metodo CheckInputType

Questo è il passaggio 3A dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

Il [**metodo CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) viene chiamato quando il filtro upstream propone un tipo di supporto al filtro di trasformazione. Questo metodo accetta un puntatore a [**un oggetto CMediaType,**](cmediatype.md) che è un thin wrapper per la [**struttura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) In questo metodo è necessario esaminare tutti i campi pertinenti della **struttura AM \_ MEDIA \_ TYPE,** inclusi i campi nel blocco di formato. È possibile usare i metodi della funzione di accesso definiti in **CMediaType** o fare riferimento direttamente ai membri della struttura. Se un campo non è valido, restituire VFW \_ E \_ TYPE NOT \_ \_ ACCEPTED. Se l'intero tipo di supporto è valido, restituire S \_ OK.

Ad esempio, nel filtro del codificatore RLE il tipo di input deve essere un video RGB non compresso a 8 bit o a 4 bit. Non esiste alcun motivo per supportare altri formati di input, ad esempio RGB a 16 o 24 bit, perché il filtro dovrebbe convertirli a una profondità in bit inferiore e DirectShow fornisce già un filtro di [Color Space Converter](color-space-converter-filter.md) a tale scopo. L'esempio seguente presuppone che il codificatore supporti video a 8 bit ma non video a 4 bit:


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



In questo esempio il metodo controlla prima il tipo principale e il sottotipo. Controlla quindi il tipo di formato per assicurarsi che il blocco di formato sia una [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Il filtro potrebbe supportare [**anche VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)ma in questo caso non ci sarebbe alcun vantaggio reale. La **struttura VIDEOINFOHEADER2** aggiunge il supporto per l'interlacciamento e i pixel non quadrati, che probabilmente non saranno rilevanti nei video a 8 bit.

Se il tipo di formato è corretto, l'esempio controlla i membri **biBitCount** e **biCompression** della struttura **VIDEOINFOHEADER** per verificare che il formato sia RGB non compresso a 8 bit. Come illustrato in questo esempio, è necessario forzare


```C++
pbFormat
```



Puntatore alla struttura corretta, in base al tipo di formato. Controllare sempre il GUID del tipo di formato (**formattype**) e le dimensioni del blocco di formato (**cbFormat**) prima di eseguire il cast del puntatore.

L'esempio verifica anche che il numero di voci della tavolozza sia compatibile con la profondità in bit e che il blocco di formato sia sufficientemente grande da contenere le voci della tavolozza. Se tutte queste informazioni sono corrette, il metodo restituisce S \_ OK.

Passaggio successivo: [Passaggio 3B. Implementare il metodo GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



