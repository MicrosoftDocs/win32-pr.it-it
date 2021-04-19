---
description: Il metodo SetDefaultTargetRect imposta il rettangolo del video di destinazione predefinito (Virtual pure). Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Metodo CBaseControlVideo. SetDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328561"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>CBaseControlVideo. SetDefaultTargetRect, metodo

Il `SetDefaultTargetRect` metodo imposta il rettangolo del video di destinazione predefinito (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di questo per reimpostare il rettangolo video di destinazione Viene chiamato dalla funzione membro [**CBaseControlVideo:: SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) .

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) . Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con il tipo di supporto del PIN di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




