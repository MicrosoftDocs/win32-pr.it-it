---
description: Il metodo SetTargetRect imposta il rettangolo di destinazione corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione cambia.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Metodo CBaseControlVideo.SetTargetRect (Ctlutil.h)
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
ms.openlocfilehash: 3af420d9280d21ccf11bfdc6a23b63b33f10c1bf5a360f1770647dcb51655cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017409"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>Metodo CBaseControlVideo.SetTargetRect

Il `SetTargetRect` metodo imposta il rettangolo di destinazione corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione cambia.

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

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di per sapere quando cambia il rettangolo di destinazione. Viene chiamato dalle funzioni membro seguenti.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo::put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo::put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo::put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo::put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un \_ oggetto [**CDrawImage.**](cdrawimage.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




