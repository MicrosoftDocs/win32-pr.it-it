---
description: Il metodo SetDefaultSourceRect imposta il rettangolo del video di origine predefinito (puro virtuale). In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Metodo CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329871"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>CBaseControlVideo. SetDefaultSourceRect, metodo

Il `SetDefaultSourceRect` metodo imposta il rettangolo del video di origine predefinito (puro virtuale). In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di questo per ripristinare il rettangolo di origine. Viene chiamato da [**CBaseControlVideo:: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) . Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con tipo di supporto del PIN di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




