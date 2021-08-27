---
description: Il metodo SetDefaultTargetRect imposta il rettangolo video di destinazione predefinito (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Metodo CBaseControlVideo.SetDefaultTargetRect (Ctlutil.h)
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
ms.openlocfilehash: 1ab9cf310ffc35df07ecd9e332325bb5f20f3cb4884ee17e672294b89c5abc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087481"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>Metodo CBaseControlVideo.SetDefaultTargetRect

Il `SetDefaultTargetRect` metodo imposta il rettangolo video di destinazione predefinito (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di per reimpostare il rettangolo video di destinazione. Viene chiamato dalla funzione membro [**CBaseControlVideo::SetDefaultDestinationPosition.**](cbasecontrolvideo-setdefaultdestinationposition.md)

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



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un \_ oggetto [**CDrawImage.**](cdrawimage.md) Il membro dati m mtIn, definito anche nella classe derivata, contiene un \_ [**oggetto CMediaType**](cmediatype.md) con il tipo di supporto del pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




