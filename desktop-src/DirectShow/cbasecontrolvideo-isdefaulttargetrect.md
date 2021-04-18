---
description: Il metodo IsDefaultTargetRect determina se il renderer usa il rettangolo di destinazione predefinito (Virtual pure).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Metodo CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333797"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>CBaseControlVideo. IsDefaultTargetRect, metodo

Il `IsDefaultTargetRect` metodo determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il renderer utilizza la destinazione predefinita; in caso contrario, restituisce \_ false.

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere implementata nella classe derivata. Viene chiamato dalla funzione membro [**CBaseControlVideo:: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
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

 

 




