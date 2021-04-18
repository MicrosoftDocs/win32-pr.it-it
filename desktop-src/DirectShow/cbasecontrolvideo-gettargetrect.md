---
description: Il metodo GetTargetRect Recupera il rettangolo di destinazione. Si tratta di una funzione membro Helper interna.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Metodo CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327843"
---
# <a name="cbasecontrolvideogettargetrect-method"></a>CBaseControlVideo. GetTargetRect, metodo

Il `GetTargetRect` metodo recupera il rettangolo di destinazione. Si tratta di una funzione membro Helper interna.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntatore al rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere sottoposta a override nella classe derivata per restituire il rettangolo di destinazione utilizzato dal renderer video. Viene chiamato dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.

-   [**CBaseControlVideo::GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)
-   [**CBaseControlVideo::p UT \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo:: Get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)
-   [**CBaseControlVideo::p UT \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo:: Get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)
-   [**CBaseControlVideo::p UT \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo:: Get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)
-   [**CBaseControlVideo::p UT \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)
-   [**CBaseControlVideo:: Get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




