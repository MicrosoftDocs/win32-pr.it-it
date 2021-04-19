---
description: Il metodo SetTargetRect imposta il rettangolo di destinazione corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione viene modificato.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Metodo CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332353"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>CBaseControlVideo. SetTargetRect, metodo

Il `SetTargetRect` metodo imposta il rettangolo di destinazione corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione viene modificato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetTargetRect(
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

Le classi derivate devono eseguire l'override di questo per stabilire quando cambia il rettangolo di destinazione. Viene chiamato dalle funzioni membro seguenti.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo::p UT \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo::p UT \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo::p UT \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo::p UT \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
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

 

 




