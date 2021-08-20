---
description: Il metodo IsDefaultTargetRect determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Metodo CBaseControlVideo.IsDefaultTargetRect (Ctlutil.h)
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
ms.openlocfilehash: c11d5b99610ff88a9e5f4088aa47efdcd8f3d9d676f0b17fad4d8e316324e807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955240"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Metodo CBaseControlVideo.IsDefaultTargetRect

Il `IsDefaultTargetRect` metodo determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il renderer usa la destinazione predefinita; in caso contrario, restituisce S \_ FALSE.

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere implementata nella classe derivata. Viene chiamato dalla funzione membro [**CBaseControlVideo::IsUsingDefaultDestination.**](cbasecontrolvideo-isusingdefaultdestination.md)

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



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo,**](cbasecontrolvideo.md)m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un oggetto \_ [**CDrawImage.**](cdrawimage.md) Il membro dati m mtIn, definito anche nella classe derivata, contiene un oggetto CMediaType con il tipo di supporto \_ del pin di input. [](cmediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




