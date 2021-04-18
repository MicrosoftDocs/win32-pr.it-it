---
description: Metodo virtuale pure che esegue l'override delle classi derivate.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Metodo CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328950"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>CBaseControlVideo. GetStaticImage, metodo

Metodo virtuale pure che esegue l'override delle classi derivate.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Puntatore alla dimensione del buffer di output.

</dd> <dt>

*pDIBImage* 
</dt> <dd>

Puntatore al buffer di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , un'applicazione può richiedere che venga fornita una copia dell'immagine corrente in un buffer di memoria. alcuni renderer possono restituire e \_ NOTIMPL a questo se non lo supportano. La classe derivata determina come recuperare l'immagine. Quando l'applicazione chiama **CBaseControlVideo:: GetStaticImage**, chiama questo metodo virtuale pure che la classe derivata deve eseguire l'override per implementarla. Viene anche chiamato dalla funzione membro [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .

La classe fornisce una funzione membro helper, [**CBaseControlVideo:: CopyImage**](cbasecontrolvideo-copyimage.md), a cui può essere assegnato un esempio che contiene un'immagine e la funzione membro copia la relativa sezione (in base al rettangolo di origine corrente) nel buffer di output fornito dall'applicazione.

Nell'esempio seguente viene illustrata un'implementazione di questa funzione membro in una classe derivata. In questo esempio m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md).


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




